---
name: datakilder
description: Viser hvilke datakilder som er tilgjengelige, hva hver av dem inneholder, hvilken periode de dekker og når de sist ble oppdatert. Bruk denne skillen når brukeren spør hva slags data hun har tilgang til, hvor ferske tallene er, om en kilde er oppdatert, hvorfor noe mangler, eller hvilken periode det finnes tall for. Trigger på: «hvilke data har vi», «hva har jeg tilgang til», «hvilke kilder», «er dataen oppdatert», «hvor ferske er tallene», «hvor gammel er dataen», «til og med når har vi tall», «mangler det data», «hvorfor ser jeg ikke X», «datakilder», «datastatus», «hva ligger i TRY Data». Bruk den også før et svar som avhenger av at en kilde faktisk er oppdatert.
---

# Datakilder

Svarer på ett spørsmål: **hva har vi data om, hvor langt fram går den, og når ble den sist oppdatert.**

Svaret bygges alltid fra to live-spørringer – aldri fra en liste i denne filen, og aldri fra hukommelsen.
En kilde som var der i går kan ha sluttet å oppdatere seg i natt, og det er nettopp det brukeren spør om.

## Slik gjør du det

Kjør begge spørringene. Én runde hver, ingen oppfølging nødvendig.

**1. Betalt annonsering – én rad per plattform:**

```sql
SELECT Source, MIN(MetricDate) AS FraDato, MAX(MetricDate) AS TilDato
FROM dbo.fact_paid_media_performance GROUP BY Source ORDER BY Source
```

**2. Alt det andre:**

```sql
SELECT 'Butikksalg' AS Omrade, MIN(MetricDate) AS FraDato, MAX(MetricDate) AS TilDato, MAX(LoadedAt) AS SistOppdatert FROM dbo.fact_pos_sales
UNION ALL SELECT 'Nettbutikk', MIN(MetricDate), MAX(MetricDate), MAX(LoadedAt) FROM dbo.fact_online_commerce
UNION ALL SELECT 'Henvendelser', MIN(MetricDate), MAX(MetricDate), MAX(LoadedAt) FROM dbo.fact_lead_forms
UNION ALL SELECT 'Merkevaretracking', MIN(ResponseDate), MAX(ResponseDate), MAX(LoadedAt) FROM dbo.fact_brand_tracking
UNION ALL SELECT 'Nettsidetrafikk', MIN(MetricDate), MAX(MetricDate), NULL FROM dbo.fact_web_analytics
UNION ALL SELECT 'Organisk søk', MIN(MetricDate), MAX(MetricDate), NULL FROM dbo.fact_organic_search
UNION ALL SELECT 'Google Performance Max', MIN(MetricDate), MAX(MetricDate), NULL FROM dbo.fact_paid_media_pmax
```

Kommer et område tilbake uten rader, **utelat det**. Skriv aldri «ingen data» for noe – da forteller du hva
som finnes andre steder enn her. Tilgangen er avgrenset, og det brukeren ser er det hun har.

## Navn du bruker i svaret

Plattformverdiene er tekniske. Oversett dem, alltid:

| Fra spørringen | Slik skriver du det |
|---|---|
| `facebook_ads` | Meta (Facebook og Instagram) |
| `google_ads` | Google Ads (søk og display) |
| `google_display_video_360` | Programmatisk display (DV360) |
| `linkedin_ads` | LinkedIn |
| `microsoft_ads` | Microsoft Ads (Bing) |
| `snapchat` | Snapchat |
| `tiktok_ads` | TikTok |
| `readpeak` | Native annonsering (Readpeak) |
| `adnuntius` | Display og banner (Adnuntius) |

Google Performance Max slås sammen med Google Ads i svaret, med en merknad om at den ligger separat –
et «totalt Google»-tall må ha begge.

## Hva hvert område inneholder

Én linje per område, ikke mer. Dette er det brukeren trenger for å vite om spørsmålet hennes kan besvares:

- **Betalt annonsering** – kostnad, visninger, klikk og konverteringer per dag, per kampanje og annonse.
  Rekkevidde og frekvens finnes bare for Meta og Snapchat. Demografi bare for Meta.
  Konverteringsverdi mangler for TikTok, native og display.
- **Butikksalg** – salg, dekningsbidrag og antall ordrer per dag per kjede, fordelt på kundesegment, fylke
  og varegruppe. Kjedene XL-BYGG, Byggtorget, Fargerike og Mal Proff.
- **Nettbutikk** – ordrer og handlekurver per dag per butikk. Bare XL-BYGG og Byggtorget selger denne veien.
- **Henvendelser** – skjemahenvendelser fra kjedenes nettsider per dag per butikk, med status i salgsløpet.
  Fargerike har ingen skjemaer og finnes derfor ikke her.
- **Merkevaretracking** – spørreundersøkelse blant sluttkunder: kjennskap, preferanse og kjøpsdrivere.
  Løpende svar gjennom måneden, ikke bølger.
- **Nettsidetrafikk** – besøkende, sesjoner, trafikkilder, landingssider og netthandel.
- **Organisk søk** – søkeord, visninger, klikk og posisjon i Google uten annonsering.

## Slik ser svaret ut

En tabell med fire kolonner: **Kilde · Hva det er · Periode · Sist oppdatert**.
Deretter maks tre linjer prosa. Ikke HTML, ikke dashboard – med mindre brukeren ber om det.

- **Periode:** «jan 2023 – 14. sep 2026». Norsk datoformat, norske månedsnavn.
- **Sist oppdatert:** har området et oppdateringstidspunkt, oppgi dato. Mangler det, skriv «–» og la
  periodekolonnen svare. **Finn aldri på et oppdateringstidspunkt** fra siste datadato – det er to
  forskjellige ting, og en kilde kan være oppdatert i natt uten å ha fått nye tall.

**Det viktigste du gjør:** si fra når en kilde har sluttet å komme inn. Har et område ingen tall de siste
to ukene, løft det ut av tabellen og si det i prosaen – «Programmatisk display har ingen tall etter
8. februar». Det er hele grunnen til at noen spør om dette, og en tabell alene skjuler det.

Slutter du med en påminnelse: dette er tall fra annonseplattformene og kundens egne systemer, gjennom
TRY Data. Hva de tåler å tolkes som, er `markedsdata` sin jobb – ikke denne skillens.

## Regler du ikke bryter

- Ingen tabellnavn, kolonnenavn, spørringer eller radantall i svaret. Brukeren spurte om kilder, ikke om
  hvordan de er lagret. Spørringene over er dine, ikke hennes.
- Aldri antyde hva TRY Data ellers inneholder, eller at andre virksomheters data finnes der.
- Aldri sammenlign mot andre virksomheter, og aldri oppgi bransjetall som om de kom fra data.
- Tolk ikke tallene her. Dette er en innholdsfortegnelse, ikke en analyse.
