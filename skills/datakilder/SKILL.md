---
name: datakilder
description: Viser hvilke datakilder som er tilgjengelige, hvilke kjeder og selskaper som ligger på hver kilde, hvilken periode de dekker og når de sist ble oppdatert. Bruk denne skillen når brukeren spør hva slags data hun har tilgang til, hvor ferske tallene er, om en kilde er oppdatert, hvorfor noe mangler, hvilken periode det finnes tall for, eller hva som finnes for en bestemt kjede. Trigger på: «hvilke data har vi», «hva har jeg tilgang til», «hvilke kilder», «er dataen oppdatert», «hvor ferske er tallene», «hvor gammel er dataen», «til og med når har vi tall», «mangler det data», «hvorfor ser jeg ikke X», «har vi Meta-data på XL-BYGG», «hva har vi på Fargerike», «datakilder», «datastatus». Bruk den også før et svar som avhenger av at en kilde faktisk er oppdatert.
---

# Datakilder

Svarer på ett spørsmål: **hva har vi data om, for hvem, hvor langt fram går den, og når ble den sist oppdatert.**

Svaret bygges alltid fra spørringene under – aldri fra en liste i denne filen, og aldri fra hukommelsen.
En kilde som var der i går kan ha sluttet å oppdatere seg i natt, og det er nettopp det brukeren spør om.

## Spørring 1 – kilde per selskap

```sql
WITH alt AS (
  SELECT 'Betalt annonsering' AS Omrade, Source, CustomerName, MetricDate AS Dato, CAST(NULL AS datetime2) AS Lastet FROM dbo.fact_paid_media_performance
  UNION ALL SELECT 'Betalt annonsering', 'google_ads_pmax', CustomerName, MetricDate, NULL FROM dbo.fact_paid_media_pmax
  UNION ALL SELECT 'Butikksalg', Source, CustomerName, MetricDate, LoadedAt FROM dbo.fact_pos_sales
  UNION ALL SELECT 'Nettbutikk', Source, CustomerName, MetricDate, LoadedAt FROM dbo.fact_online_commerce
  UNION ALL SELECT 'Henvendelser', Source, CustomerName, MetricDate, LoadedAt FROM dbo.fact_lead_forms
  UNION ALL SELECT 'Nettsidetrafikk', Source, CustomerName, MetricDate, NULL FROM dbo.fact_web_analytics
  UNION ALL SELECT 'Organisk søk', Source, CustomerName, MetricDate, NULL FROM dbo.fact_organic_search
)
SELECT Omrade, Source, CustomerName, MIN(Dato) AS FraDato, MAX(Dato) AS TilDato, MAX(Lastet) AS SistOppdatert
FROM alt WHERE CustomerName IS NOT NULL
GROUP BY Omrade, Source, CustomerName
ORDER BY CustomerName, Omrade, Source
```

`CustomerName IS NOT NULL` skal stå. Rader uten selskap er annonsekontoer som ennå ikke er koblet til et
selskap – de hører ikke til noen, og skal ikke vises som om de gjorde det.

## Spørring 2 – merkevaretracking

Den ligger på undersøkelseskategori, ikke på selskap, og må hentes for seg:

```sql
SELECT Category, MIN(ResponseDate) AS FraDato, MAX(ResponseDate) AS TilDato, MAX(LoadedAt) AS SistOppdatert
FROM dbo.fact_brand_tracking GROUP BY Category ORDER BY Category
```

Kategorinavnene er tekniske. Skriv `byggevare` som «Byggevare», `rorlegger` som «Rørlegger/VVS»,
`baderom` som «Baderom», `maling` som «Maling», `gulv` som «Gulv».

## Navn du bruker i svaret

Kildeverdiene er tekniske. Oversett dem, alltid:

| Fra spørringen | Slik skriver du det |
|---|---|
| `facebook_ads` | Meta (Facebook og Instagram) |
| `google_ads` | Google Ads (søk og display) |
| `google_ads_pmax` | Google Performance Max |
| `google_display_video_360` | Programmatisk display (DV360) |
| `linkedin_ads` | LinkedIn |
| `microsoft_ads` | Microsoft Ads (Bing) |
| `snapchat` | Snapchat |
| `tiktok_ads` | TikTok |
| `readpeak` | Native annonsering (Readpeak) |
| `adnuntius` | Display og banner (Adnuntius) |
| `mestergruppen_pos` | Diveport (kassesystem) |
| `omnium` | Omnium |
| `google_analytics_ga4` | Google Analytics |
| `google_search_console` | Google Search Console |

Merkevaretrackingen kommer fra **Norstat**. Den har ingen kildekolonne i dataen, så navnet står her.

**Navngi alltid systemet dataen kommer fra, ikke bare hva den handler om.** Brukeren spør hvilke kilder hun
har – «Omnium» og «Norstat» er svaret, «nettbutikk» og «merkevaretracking» er hva de inneholder. Skriv
begge: «Omnium – nettbutikk», «Omnium – henvendelser», «Norstat – merkevaretracking». Dette er kundens
egne systemer; de vet hva de heter, og et forretningsord i stedet for systemnavnet skjuler det de spurte om.

Google Ads og Performance Max er to kilder i dataen. Nevn begge, og si at et samlet Google-tall må ha begge.

## Hva hvert område inneholder

Én linje per område – nok til at brukeren vet om spørsmålet hennes kan besvares:

- **Betalt annonsering** – kostnad, visninger, klikk og konverteringer per dag, per kampanje og annonse.
  Rekkevidde og frekvens finnes bare for Meta og Snapchat. Demografi bare for Meta.
  Konverteringsverdi mangler for TikTok, native og display.
- **Butikksalg** – salg, dekningsbidrag og antall ordrer per dag per kjede, fordelt på kundesegment,
  fylke og varegruppe. Returer og kreditnotaer ligger som negative beløp.
- **Nettbutikk** – ordrer og handlekurver per dag per butikk. Åpne handlekurver er en telling på siste
  oppdatering, ikke et beløp som kan summeres over en periode.
- **Henvendelser** – skjemahenvendelser fra nettsidene per dag per butikk, med status i salgsløpet.
- **Merkevaretracking** – spørreundersøkelse blant sluttkunder: kjennskap, preferanse og kjøpsdrivere.
  Løpende svar gjennom måneden, ikke bølger.
- **Nettsidetrafikk** – besøkende, sesjoner, trafikkilder, landingssider og netthandel.
- **Organisk søk** – søkeord, visninger, klikk og posisjon i Google uten annonsering.

Ikke si at en kjede mangler en kilde fordi du tror det. Kommer kombinasjonen ikke tilbake fra spørringen,
finnes den ikke – og det er svaret.

## Slik ser svaret ut

**Gruppér på selskap, ikke på kilde.** Brukeren tenker i kjeder: hun vil vite hva som finnes på Fargerike,
ikke hvilke kjeder som er på Snapchat. Én seksjon per selskap, og under hver en tabell med tre kolonner:
**Kilde · Periode · Sist oppdatert**.

Spør hun om én kjede eller én kilde, svar bare på det. Ikke lever hele matrisen når hun ba om ett felt.

- **Periode:** «jan 2023 – 14. sep 2026». Norsk datoformat, norske månedsnavn.
- **Sist oppdatert:** har kilden et oppdateringstidspunkt, oppgi dato. Mangler det, skriv «–» og la
  periodekolonnen svare. **Finn aldri på et oppdateringstidspunkt** fra siste datadato – det er to
  forskjellige ting, og en kilde kan være oppdatert i natt uten å ha fått nye tall.

**Det viktigste du gjør:** si fra når en kombinasjon har sluttet å komme inn. Har en kilde ingen tall de
siste to ukene, løft den ut av tabellen og si det i prosaen først – «Nettbutikken for Blink Hus har ingen
tall etter 3. august». Det er hele grunnen til at noen spør om dette, og en tabell alene skjuler det.
Er alt ferskt, si det i én setning.

Avslutt med en påminnelse: dette er tall fra annonseplattformene og egne systemer, gjennom TRY Data.
Hva de tåler å tolkes som, er `markedsdata` sin jobb – ikke denne skillens.

## Regler du ikke bryter

- Ingen tabellnavn, kolonnenavn, spørringer eller radantall i svaret. Brukeren spurte om kilder, ikke om
  hvordan de er lagret. Spørringene over er dine, ikke hennes.
- Aldri antyde hva TRY Data ellers inneholder, eller at andre virksomheters data finnes der.
  **Kommer det et selskap tilbake som ikke hører til kunden, er det en feil i tilgangsstyringen – ikke
  vis det, og si at du ikke kan liste kilder nå.** Det er den ene feilen i denne skillen som ikke kan
  repareres i etterkant.
- Aldri sammenlign mot andre virksomheter, og aldri oppgi bransjetall som om de kom fra data.
- Tolk ikke tallene her. Dette er en innholdsfortegnelse, ikke en analyse.
