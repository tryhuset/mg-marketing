---
name: kunderapport
description: "Bygger rapporter, oppsummeringer og enkle dashboards av kundens egen markedsdata – i kundens egen visuelle profil. Bruk ALLTID når noen ber om en rapport, presentasjon, oppsummering, statusdokument eller dashboard basert på markedsdata. Trigger på: «lag en rapport», «lag en månedsrapport», «oppsummer kvartalet», «jeg skal presentere for ledelsen», «lag noe jeg kan sende til styret», «lag et dashboard», «kan du lage en PowerPoint av dette», «lag en PDF», «lag en oppsummering av kampanjen», «rapporter resultatene». Forutsetter at markedsdata-skillen har gjort tolkningen først, og bruker kundens profil-skill i samme pakke for farger, fonter og tone."
---

# Kunderapport

Du bygger rapporten. Tolkningen skjer i `markedsdata`-skillen – den er ikke valgfri, og den kommer først.

## Rekkefølge – ikke bytt om

1. **Tolk først.** Kjør `markedsdata`-skillen på innholdet: kundekontekst, tolkningsvern, forbehold, forretningsbetydning. En rapport som viser tall som ikke har vært gjennom filteret, sprer feilslutninger med finere typografi.
2. **Hent profilen.** Les `mg-brand` i denne pakken for farger, fonter, logo, tone og formatregler. Finnes den ikke, si det, og bygg nøytralt og rent – aldri i TRYs profil, og aldri med gjettede merkevarefarger.
3. **Avklar mottaker og format** med ett spørsmål hvis det er uklart. Ledelse, styre, eget team og eier trenger ulik rapport.
4. **Bygg.** Deretter verifiser. Deretter lever.

## Hva rapporten alltid inneholder

| Del | Innhold |
|---|---|
| Hovedbudskap | Én tallfestet påstand som tåler tolkningsvernet. Ingen spørsmål, ingen metafor. |
| Perioden | Tydelig avgrenset, med sammenligningsgrunnlag (forrige periode og samme periode i fjor der det finnes). |
| Måloppnåelse | Mot kundens egne KPI-er og terskler fra `kundekontekst.md`. Aldri mot generiske bransjetall alene. Er lønnsomhet tema: bruk nullpunkt-ROAS fra `references/forretningsramme.md`, ikke ROAS alene. |
| Nøkkeltall | 3–5, ikke 15. Hvert med retning, størrelse (absolutt **og** relativt) og støybånd der volumet er lavt. |
| Kanalbilde | Hva som ble levert, til hvilken kostnad. Rollen kanalen har, ikke bare tallet. |
| Hva vi ikke vet | Egen, synlig seksjon. Hva som ikke er i dataene, hvilke tall som er modellerte, hvilke forbehold som gjelder. Aldri fotnote i 7 pt. |
| Vurdering | Hva dette betyr for virksomheten. Hva som er verdt oppmerksomhet, hva som er normal variasjon. |
| Neste steg | Konkrete, forsiktige forslag – med hvem som bør involveres. |

**«Hva vi ikke vet» er ikke en ansvarsfraskrivelse.** Det er delen som gjør resten troverdig. Kutt den aldri for å spare plass. Den skal peke i begge retninger: både hvor tallene overdriver (plattformkreditering, merkevaresøk, retargeting) og hvor de undervurderer (butikksalg, manglende samtykke, langtidseffekt).

**Skal rapporten svare på «hva bidro markedsføringen med i kroner»:** følg oppskriften i «Tallet til styret» i `references/forretningsramme.md`. Gulv, anslag og tak – aldri ett tall alene, og bidragsmargin, ikke omsetning.

**Tall som avviker fra forrige rapport** skal forklares i rapporten, ikke i en e-post etterpå. Endret attribusjonsvindu, etterregistrering eller ny kanalmerking er legitime grunner – uforklarte avvik er den vanligste kilden til tapt tillit.

## Tallverifikasjon – før levering, hver gang

Hvert synlig tall skal beregnes på nytt fra kilden og sammenlignes med det som står i filen. Ikke stikkprøver – alle tall leseren ser: nøkkeltallskort, tabellceller, etiketter i grafer, tall i brødtekst og i hovedbudskapet.

For hvert tall dokumenterer du: verdi i rapporten, beregnet verdi, kilde, periode, attribusjonsmodell og vindu, differanse, status.

- **Rekkevidde og frekvens** → tas bare med hvis tallet er totalrekkevidde per kampanje fra den avdupliserte kilden, med periode oppgitt. Summerte dagstall, tall summert over kampanjer og tall summert over plattformer skal ut av rapporten, ikke forklares i en fotnote. Mangler kilden for kunden, bruk visninger og si at rekkevidde ikke måles for dem.
- **Avvik i beregning** → må rettes før levering.
- **Metodisk avvik** (f.eks. ulik attribusjonsmodell i hovedbudskap og graf, rapportert vs. inkrementell omsetning) → rettes eller forklares eksplisitt i rapporten.
- **Endres rapporten etterpå** → verifiser alle tall som er endret, og alle tall som avhenger av dem, på nytt. Delvis verifisering er ikke verifisering.

Bruk en subagent til verifikasjonen når rapporten har mer enn omtrent ti tall – den skal regne uavhengig, ikke lese etter.

## Grafregler

- Y-akse fra null på alt som handler om størrelse. Avkuttet akse får normal variasjon til å se dramatisk ut, og å merke den hjelper ikke.
- Absolutt og relativ endring sammen, alltid.
- Vis støybånd på tidsserier der volumet er lavt.
- Ett budskap per graf; tittelen sier hva man skal se.
- Ingen doble y-akser. Ingen kakediagram med mer enn tre deler. Ingen 3D.
- Er tallet lettere å forstå som setning enn som graf: skriv setningen.

## Formater

- **Selvstendig HTML** er standard for rapporter som skal leses og deles. Alt i én fil.
- **PowerPoint / Word / PDF / Excel:** bruk de tilgjengelige dokumentskillene for formatet, og les kundens profil-skill for utseende.
- **Dashboard:** bare når kunden faktisk skal komme tilbake til det jevnlig. Ellers er en rapport bedre.

Ved større leveranser (rapport *og* dashboard, eller mange kilder): planlegg arbeidet først, kjør datainnhenting og bygging i parallelle subagenter der det er mulig, og legg verifikasjonen sist – alltid.

## Tone

Rapporten skrives i kundens tone, ikke i TRYs og ikke i plattformenes. Klarspråk. Engelske termer forklart ved første bruk. Ingen tabellnavn, kolonnenavn eller annen datamodell-sjargong – kilder oppgis som system og menneske: «hentet fra Meta, gjennom TRY Data».

Symmetriregelen gjelder også i rapport: det som ikke virket står like tydelig som det som virket.
