# Mestergruppen marketing

Plugin som lar Mestergruppen spørre sin egen markedsdata i samtale, med faglige rammer som holder – og bygge rapporter
og dashboards i Mestergruppens eget uttrykk.

**Avsender: TRY. Mottaker: Mestergruppen.** Pakken er bygget for å stå i Mestergruppens hender, hos deres egne ansatte,
uten en TRY-rådgiver i rommet. Alt i den er skrevet med det for øye.

## Hva den løser

Brukeren får spørre fritt: «hvordan gikk kampanjen», «hvorfor falt trafikken», «får vi noe igjen for pengene». Det er
nyttig – og risikabelt. En sluttbruker med lav teknisk forståelse kan ikke selv se når et tall ikke tåler vekten hun
legger på det, og en samtalepartner som svarer på alt hun spør om, bekrefter feilslutninger i stedet for å hindre dem.

**To brukergrupper**, og skillen kjenner dem igjen underveis uten å spørre:

- **Markedssjefen** – forretningsnivå. Resultater, måloppnåelse, hva det betyr for virksomheten. Korte svar.
- **Den hands-on markedsrådgiveren** – operativt nivå, lav til middels kanalkompetanse. Kampanjer, uttak, formater,
  leveranse. Full operativ sparring, uten å bli undervist i begreper hun alt bruker.

Pakken løser tre ting:

1. **Nivå.** Den tolker på markedssjefsnivå – forretning, ikke kanaloperasjon.
2. **Vern.** Den filtrerer støy, falske årsakssammenhenger og bagateller før tallet blir en konklusjon.
3. **Motstand.** Den korrigerer feilslutninger hver gang – vennlig, pedagogisk, og alltid med en alternativ
   forklaring, fordi en korreksjon uten alternativ forklaring ikke fester seg.

## Innhold

| Skill | Rolle |
|---|---|
| `markedsdata` | Hovedskillen. Samtaleprotokoll, modusgjenkjenning, tolkningsvern, forretningsramme, kanalnivå, korreksjonsmønstre. Utløses av alle spørsmål om data. |
| `datakilder` | Viser hvilke kilder som er tilgjengelige, hva de inneholder, hvilken periode de dekker og når de sist ble oppdatert. Slås opp live – aldri fra en liste. |
| `kunderapport` | Bygger rapporter og dashboards i Mestergruppens profil, med obligatorisk tallverifikasjon. |
| `mg-brand` | Mestergruppens visuelle identitet og tone: farger, typografi, logo, språk, formatregler. |
| `mg-dataviz` | Regler for datavisualisering: diagramvalg, merking, fargesystem og tilgjengelighet. |

Fagbasen ligger i `skills/markedsdata/references/`: tolkningsvern (statistikk og feilkilder), metrikker,
plattformforbehold, forretningsramme (forretningsnivået), kanalnivå (operativ diagnostikk), samtalemønstre og en
kildeliste med styrkegradering og kjente kildehull.

## Slik henger det sammen

```
                  TRY Data (connector – Mestergruppens egne data)
                                │
                          markedsdata
              (tolkning, vern, forretningsnivå, motstand)
                     │                        │
              kundekontekst.md          references/
              (mål, KPI-er,             forretningsramme  ← markedssjefen
               marginer, roller,        kanalniva         ← rådgiveren
               forbehold)               tolkningsvern + metrikker + kilder (felles)
                                │
                          kunderapport
                                │
                     mg-brand + mg-dataviz
                    (Mestergruppens uttrykk)
```

## Datakilde

Connectoren **TRY Data** følger ikke med i pakken. Tilgangen styres i plattformen og er avgrenset til Mestergruppens
egne data. Se `CONNECTORS.md`.

## Distribusjon

Pakken deles til Mestergruppens Claude Enterprise og brukes av deres ansatte. `OPPSETT.md` er sjekklista som skal være
gjennomgått før tilgang gis.

## Versjon

0.1.0 – september 2026. Bygget på TRYs kundepakke `try-analytics-kunde` 0.3.1 av Kristoffer Semelenge, TRY.

Kundepakken ble blindtestet mot Mestergruppens egne XL-BYGG-data i august 2026, mot Claude uten skill og mot
TRYs interne fagpakke. Den vant begge dommerrunder (25,0 av 28, mot 21,5 uten skill). Forspranget lå i
kildedisiplin og tolkningsvern – nøyaktig de feilene en sluttbruker uten rådgiver ikke kan oppdage selv.

**Fagansvarlig for metodikken: [TODO].** Pakken skal ikke deles til Mestergruppen før dette feltet har et navn. Den
gjengir over 40 forskningsfunn til en ekstern mottaker; en kundevendt skill uten navngitt eier er en skill ingen
oppdaterer og ingen svarer for.
