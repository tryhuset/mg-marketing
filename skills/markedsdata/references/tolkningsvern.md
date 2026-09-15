# Tolkningsvern – hva tallene tåler å bli tolket som

Dette er filteret mellom et tall og en konklusjon. Alle tall og terskler her har kilde; kildestyrke er merket
(**Høy** = fagfellevurdert eller offisiell plattformdokumentasjon, **Middels** = én primærkilde eller sterk
sekundær, **Lav** = kun bransjepraksis). Fulle referanser i `kilder.md`.

---

## 1. Volum bestemmer hva du kan se

Hvor liten forskjell du kan oppdage styres nesten utelukkende av **antall konverteringer**, ikke av budsjett eller
visninger. Tommelfingerregelen, utledet fra Lehr/van Belles utvalgsregel (α=0,05, 80 % styrke):

> minste påvisbare relative forskjell ≈ 4 / √(antall konverteringer per gruppe)

| Konverteringer per gruppe | Minste forskjell som er mulig å påvise |
|---|---|
| 25 | ~80 % |
| 100 | ~40 % |
| 400 | ~20 % |
| 1 600 | ~10 % |
| 6 400 | ~5 % |

**Hva som er normal svingning.** Tellinger svinger av seg selv. Regnet fra tellestatistikk (Poisson), som egen
utregning og ikke som studiefunn:

- Én periode mot sitt eget snitt: ca. **±2 / √C** (95 %). Med 100 kjøp: ±20 %.
- To perioder sammenlignet med hverandre: ca. **±2,8 / √C** (95 %). Med 100 kjøp i hver: ±28 %.

Det er den siste som gjelder når kunden spør «hvorfor falt kostnaden per kjøp fra juni til juli». *(Utregning fra
tellestatistikk – oppgi som tommelfingerregel, aldri som forskningsfunn.)*

**Google Ads' egen volumtabell** peker samme vei: under 30 konverteringer i perioden gir CPA/ROAS-svingning «opp
til 100 %»; ved 50 opp til 50 %; ved 100 opp til 20 %; ved 500 under 20 %. *(Høy, men merk konteksten: tabellen står i
Googles veiledning for automatiske budstrategier på Display og blander tilfeldig variasjon med systemets kalibrering.
Bruk den som støtte for at lavt volum er ustabilt – ikke som ren støymåling.)*

Terskelen 25 (fra formelen over) og Googles 30 måler litt ulike ting. Bruk 25 som grense for «kan ikke konkludere om
forskjeller», og Googles tabell som argument for at lave volumer er ustabile i seg selv.

**Praktiske regler:**
- Under 25 konverteringer: ingen konklusjon om forskjeller. **Si at det er en tommelfingerregel når du bruker den** –
  «som tommelfingerregel klarer vi ikke å skille forskjeller under rundt 25 kjøp». Sagt uten det forbeholdet leses 25
  som en målt grense i kundens egne data, og det er den ikke.
- 25–100: bare forskjeller over 40–80 % er reelle.
- Sammenlign alltid hele uker, i multipler av sju dager (ukedagseffekter). *(Middels–Høy)*

**Til kunden:** «Med rundt 100 kjøp i måneden kan kostnad per kjøp svinge rundt 30 % fra måned til måned helt av seg
selv. Vi kan ikke se forskjeller mindre enn det.»

---

## 2. Medieeffekt er ekstremt vanskelig å måle – også for de store

Lewis & Rao gjennomgikk 25 store randomiserte annonseforsøk (2,8 mill. USD mediebudsjett, de fleste over én million
brukere). Median standardfeil på avkastning var 26 % for handel og 115 % for finans; **bare 3 av 25** forsøk kunne
skille 50 % avkastning fra null. Medianforsøket måtte være **9× større** for å klare det, og **62× større** for å
påvise 10 prosentpoengs forskjell. Grunnen er at salg per person varierer 10–15× mer enn annonseeffekten. *(Høy)*

**Til kunden:** «Selv de største plattformene, med millioner av brukere, klarer ofte ikke å måle om en kampanje ga
0 eller 50 % avkastning. Da kan ikke vi gjøre det på én måneds tall.»

Bruk dette som ydmykhetsanker – ikke som argument for å slutte å måle.

---

## 3. Falske korrelasjoner mellom kurver

To tidsserier som begge har trend eller treghet korrelerer «tydelig» selv når de er helt uavhengige. Granger &
Newbold viste at regresjon mellom to uavhengige tilfeldige serier ga **76 % falske signifikante sammenhenger**;
også stasjonære serier med treghet gir 30–60 % falske funn. Mediedata er tunge på treghet: kampanjeflighter,
budsjettkurver, sesong. *(Høy)*

**Til kunden:** «To kurver som følger hverandre er hverdagen, ikke et bevis. I simuleringer med tall som er garantert
uten sammenheng, ser tre av fire ut som en tydelig sammenheng.»

**Regel:** nevn alltid minst én alternativ forklaring når to serier beveger seg likt.

---

## 4. Samtidighet – standardlisten over alternative forklaringer

Gå gjennom denne før du tilskriver en endring til markedsføringen:

sesong · pris og rabatt · distribusjon og lagerstatus · konkurrentaktivitet og CPM-press · kampanjetiming ·
budsjettendring · endring på nettsiden · PR og omtale · vær · makro · **og endring i selve målingen**

Det siste er reelt og undervurdert: konverteringer etterregistreres i dagene etter at de skjedde (Googles
dokumentasjon oppgir at attribuerte konverteringsdata kan oppdateres i opptil 12 dager – *verifiser tallet i Googles
hjelpesider før det gjengis til kunde*), og GA4 modellerer konverteringer for brukere uten samtykke, og utelater
modellerte tall når trafikken er for lav. Tall endrer seg altså i etterkant uten at noe skjedde i markedet.
*(Modelleringen: Høy. 12-dagersgrensen: Middels – uverifisert.)*

**Twymans lov** er den nyttigste enkeltregelen: *«Any figure that looks interesting or different is usually wrong.»*
Ser et tall spennende ut, sjekk målingen før du sjekker markedet. *(Høy)*

---

## 5. Algoritmen velger de kjøpsklare (utvalgsskjevhet)

Eksponering er ikke tilfeldig. Leveringsalgoritmen viser annonsen til dem den tror er mest tilbøyelige til å
konvertere, brukeren er selv aktiv på nett, og konkurrentene byr. Gordon m.fl. (15 randomiserte forsøk på Facebook,
500 mill. observasjoner) fant at «i halvparten av studiene er anslått effekt feil med en faktor tre». I ett tilfelle
var sann effekt 73 % løft, mens naiv eksponert-mot-ueksponert ga 316 %. Lewis, Rao & Reiley fant «activity bias» der
sann effekt var 5,4 % og naiv sammenligning ga 1198 %. *(Høy)*

**Til kunden:** «Algoritmen viser annonsen til dem som var mest kjøpsklare uansett. Tallene måler derfor delvis hvem
vi traff, ikke hva annonsen gjorde.»

---

## 6. Høsting: merkevaresøk og retargeting ser alltid best ut

eBay slo av betalte søkeannonser i et randomisert forsøk. På merkevareord ble **99,5 % av de tapte klikkene fanget
opp av organisk søk umiddelbart**. Beregnet avkastning: naiv analyse +4 173 %, med kontrollvariabler +1 632 %,
eksperimentelt estimat **−63 %**. En randomisert Bing-studie (Simonov, Nosko & Rao, 2 517 merkevarer) nyanserer:
merkevareannonser gir likevel **2–3 % inkrementell trafikk** i snitt, mest for små merkevarer – og en konkurrent i
toppposisjon kan hente en betydelig andel av klikkene når merkevaren *ikke* annonserer selv (i kildens eksempel rundt
18 %), en andel som faller markant når merkevaren annonserer. *(Begge Høy. Det siste tallet gjelder ett eksempel i
studien, ikke et snitt – ikke generaliser det.)*

**Regel:** anta høy kannibalisering i merkevaresøk og retargeting til det er testet. Men ikke anbefal å kutte
merkevaresøk – forsvarsverdien er reell og dokumentert.

---

## 7. Nevnerfeller

CTR, konverteringsrate, CPA og ROAS er brøker. En endring kan komme fra teller, nevner eller miks.

Vanligste mekanisme: skalert budsjett kjøper bredere og dyrere inventar → nevneren vokser → CTR og konverteringsrate
faller uten at noe er blitt dårligere. Motsatt ved innsnevring. *(Mekanismen: Middels – godt dokumentert i
eksperimentlitteraturen, den spesifikke budsjettkoblingen er bransjeerfaring.)*

**Regel:** se aldri på en brøk uten å ha sett teller og nevner hver for seg.

**Til kunden:** «Konverteringsraten kan falle bare fordi vi kjøpte mer trafikk – ikke fordi noe ble dårligere. Vi må
se på antall salg og antall besøk hver for seg.»

---

## 8. Simpsons paradoks – totalen kan lyve

En sammenheng kan snu når du deler opp – eller når du slår sammen. Dokumentert i webanalyse: én landingsside vant
aggregert med 95 % sikkerhet, mens den andre vant **for hver enkelt trafikkilde** – fordi trafikkfordelingen var
ulik. *(Middels–Høy)*

Samme mekanisme i mediemiks: flytt budsjett mot en billigere kanal med lavere kjøpsintensjon, og total
konverteringsrate faller selv om ingen kanal ble dårligere.

**Til kunden:** «Totaltallet kan falle samtidig som hver enkelt kanal ble bedre – fordi vi flyttet budsjett, ikke
fordi noe ble dårligere.»

---

## 9. Mange sammenligninger gir garantert en «vinner»

Sannsynligheten for minst ett falskt funn er 1 − 0,95^m: 20 sammenligninger → 64 %, 40 → 87 %, 100 → ca. 99 %.
Et dashboard med alder × kjønn × enhet × plassering gir nesten alltid en «vinner». *(Høy)*

**Regel:** funn som er plukket ut av mange segmenter skal merkes som hypotese, ikke funn. Bestem hva du ser etter
før du ser.

**Til kunden:** «Ser vi på 40 segmenter, finner vi nesten alltid en vinner. Det er matematisk garantert – også når
ingenting virker.»

---

## 10. Regresjon mot gjennomsnittet

Ekstremverdier følges av verdier nærmere snittet. Effekten er sterkest når man **velger ut** noe basert på at det
var dårligst – som er presis beskrivelsen av optimaliseringsarbeid. Deler av forbedringen kommer gratis. *(Høy)*

**Til kunden:** «Når vi plukker ut det som gikk dårligst og fikser det, blir en del av forbedringen bare at
ekstremtallet var tilfeldig lavt – ikke at grepet virket.»

---

## 11. Læringsfase og nyhetseffekt

De første dagene etter en endring er ikke sammenlignbare med normaltilstand. Google Ads: «Wait at least 2 weeks
without changes for the initial learning period»; tROAS krever minst 15 konverteringer per 30 dager, og verdier bør
vurderes over fire uker eller 1–2 kjøpssykluser. Nyhetseffekt er dokumentert: et Microsoft-forsøk viste +28 % initielt
som falt raskt dag for dag. *(Høy. Metas ofte siterte «50 hendelser per 7 dager» finner vi ikke i åpen offisiell
dokumentasjon – oppgi den som bransjepraksis, ikke som Meta-krav.)*

---

## 12. Signifikans er feil verktøy i daglig oppfølging

Den amerikanske statistikerforeningen: en p-verdi «does not measure the size of an effect or the importance of a
result», og beslutninger «should not be based only on whether a p-value passes a specific threshold». I daglig
kampanjeoppfølging er p-verdier meningsløse uansett: ingen forhåndsdefinert hypotese, kontinuerlig kikking, hundrevis
av implisitte sammenligninger. *(Høy)*

Bruk i stedet, i denne rekkefølgen:
1. **Støybånd fra historikk.** Reager på signaler, ikke på punkter: verdi utenfor båndet, eller åtte målinger på
   samme side av snittet. *(Kontrollkart-logikk: Høy for metoden, Middels anvendt på mediemetrikker.)*
2. **Usikkerhetsspenn, ikke punkttall.** «ROAS 3,1 – spennet er 2,2 til 4,3.»
3. **Praktisk terskel.** «Er forskjellen stor nok i kroner til å gjøre noe med?»

**Til kunden:** «Vi spør ikke «er dette signifikant», men «hvor sikkert er tallet, og er forskjellen stor nok til at
vi bør gjøre noe».»
