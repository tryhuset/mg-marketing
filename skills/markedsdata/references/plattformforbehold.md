# Plattformforbehold – hvorfor tallene ikke stemmer, og hva de faktisk viser

Bruk denne når kunden spør «hva ga kanalen oss», «hvorfor stemmer ikke Meta med nettbutikken», eller «hvorfor har
tallene endret seg siden sist». Kilder i `kilder.md`.

---

## 1. Plattformtall er samvariasjon, ikke effekt

Plattformen teller handlinger utført av folk som ble eksponert innenfor et tidsvindu. Den vet ikke hva som ville
skjedd uten annonsen. Fire uavhengige forskningsbidrag har målt gapet mot randomiserte forsøk:

- **Gordon m.fl. (Marketing Science 2019):** 15 forsøk på Facebook, 500 mill. observasjoner. «In half of our studies,
  the estimated percentage increase in purchase outcomes is off by a factor of three.» Ett tilfelle: sann effekt 73 %,
  naiv metode 316 %.
- **Lewis, Rao & Reiley (2011):** «activity bias» – på utfallsmålet *merkevaresøk* var sann effekt 5,4 %, mens naiv
  sammenligning av eksponerte mot ueksponerte ga 1198 %.
- **Blake, Nosko & Tadelis (Econometrica 2015):** eBay – naiv avkastning +4 173 %, eksperimentelt estimat −63 %.
- **Shapiro, Hitsch & Tuchman (Econometrica 2021):** 288 merkevarer, TV. Annonseelastisitet rundt 0,014 i
  basismodellen, med en betydelig andel ikke-signifikante eller negative anslag. *(Publiserte versjoner oppgir noe
  ulike anslag – bruk «rundt 0,01–0,02», ikke ett desimaltall.)*

*(Alle Høy.)*

**Hvordan du sier det:** «Plattformen teller de som kjøpte etter å ha sett annonsen – ikke de som kjøpte fordi de så
den. I en gjennomgang av 15 randomiserte forsøk var vanlige måter å regne effekt på feil med en faktor tre i
halvparten av tilfellene.»

**Praksis:** når du oppgir et plattformtall, oppgi det med kontekst i samme åndedrag. Ikke skjul tallet – kunden ser
det i plattformen uansett – men aldri la det stå alene som «effekt».

**Merk:** påstanden om at plattformenes summerte konverteringer overstiger faktisk salg er riktig som mekanisme (hver
plattform krediterer samme kunde), men vi har **ingen fagfellevurdert tallfesting** av hvor stort avviket er generelt.
Ikke generaliser et tall. Kundens **egne** tall er derimot fritt anvendelige og ofte det sterkeste argumentet du har:
«Meta og Google krediterer til sammen 640 kjøp i juli. Nettbutikken registrerte 268 ordre. Differansen er ikke
feilregning – det er samme kunde talt flere steder.»

**Symmetri:** si også hvor tallene **undervurderer**. Butikksalg, telefon, e-post og direkte kjøp uten sporing,
brukere uten samtykke, kjøp utenfor attribusjonsvinduet og all langtidseffekt av merkevarearbeid ligger utenfor det
plattformene ser. Nedjuster aldri uten å nevne dette – ensidig pessimisme er like uærlig som ensidig optimisme.

---

## 2. Attribusjonsvindu er en innstilling, ikke et faktum

- **Google Ads:** klikkvindu standard 30 dager (1–90 mulig), engasjert visning 3 dager, visning 1 dag. Google skriver
  eksplisitt at konverteringer utenfor vinduet ikke registreres. *(Høy)*
- **Meta:** standard 7 dagers klikk + 1 dags visning, med 1/7/28 dager som alternativer. *(Middels – Metas hjelpesider
  er ikke maskinlesbare for oss; verifiser i Meta Business Help før tallet gjengis til kunde.)*

Konsekvenser å alltid nevne når to kilder ikke stemmer:
1. Samme kampanje kan vise dobbelt så mange konverteringer bare ved å endre vinduet.
2. Meta-tall og Google-tall måler ikke det samme og skal ikke summeres.
3. Konverteringsdata kan etterregistreres i opptil 12 dager – tall fra i går er ikke ferdige.
4. GA4 modellerer konverteringer for brukere uten samtykke, og utelater modellerte tall ved for lav trafikk. *(Høy)*

**Hvordan du sier det:** «Tallet er delvis en innstilling. Meta teller alle som kjøpte innen sju dager etter et klikk
eller én dag etter en visning; nettbutikken teller ordre. Det er to ulike spørsmål, og de gir ulike svar.»

---

## 3. Merkevaresøk – den mest forførende kanalen

eBays randomiserte avstenging: **99,5 % av de tapte betalte klikkene på merkevareord ble umiddelbart fanget opp av
organisk søk**. For generiske søkeord ga hele det betalte søkeregimet 0,66 % salgsøkning – ikke signifikant. *(Høy)*

Nyansering fra randomisert Bing-studie (Simonov, Nosko & Rao, 2 517 merkevarer): merkevareannonser flytter nesten
halvparten av klikkene fra egen organisk lenke, men gir likevel **2–3 % inkrementell trafikk** i snitt – 3–4 % for
små merkevarer, nær null for de største. Uten egen annonse kan én konkurrent i toppen hente **15–20 %** av søkerne.
*(Høy)*

**Balansert formulering:** «Når noen googler navnet deres, har de langt på vei bestemt seg – annonsen kjøper ofte et
klikk dere fikk gratis. Den kan likevel være verdt å ha, som forsvar mot at en konkurrent tar plassen. Men den skal
ikke skaleres som om den skapte etterspørselen.»

---

## 4. Læringsfase og endringer

Google Ads: minst to uker uten endringer før evaluering; verdibaserte budstrategier krever minst 15 konverteringer per
30 dager; vurder over fire uker eller 1–2 kjøpssykluser. *(Høy)* Nyhetseffekt er dokumentert i eksperimentlitteraturen
– de første dagene overdriver. *(Høy)*

Metas «50 optimaliseringshendelser per uke» er utbredt bransjepraksis, men vi fant ingen åpen offisiell Meta-kilde.
Presenter den som bransjepraksis.

---

## 5. Hva som krever forsøk – og hvilke forsøk som finnes

**Kan ikke besvares fra observasjonsdata:** hvor mye salg en kanal skapte, om ROAS 6 er bedre enn ROAS 4, om en kanal
kan kuttes, om retargeting er lønnsomt, hva som ville skjedd uten kampanjen, hvor mye av salget som er baseline,
hva som skjer hvis 20 % flyttes mellom kanaler.

**Forsøkstypene, i klarspråk:**

- **Geo-test (områdesplitt):** del landet i to grupper av områder, annonser i den ene og ikke i den andre, sammenlign
  totalt salg. Robust fordi den ikke er avhengig av å spore enkeltpersoner. *(Google Research: Høy)*
- **Holdout / konverteringsløft:** plattformen holder en tilfeldig gruppe utenfor og sammenligner. Metodisk
  gullstandard er «ghost ads»; Johnson, Lewis & Nubbemeyer dokumenterer at eldre PSA-tester bryter sammen på
  algoritmisk optimaliserte plattformer, fordi algoritmen fordeler ulike brukertyper til PSA og testannonse. *(Høy)*
- **Mediemiksmodell (MMM):** statistisk modell over tid som forsøker å skille baseline fra mediedrevet salg. Gir
  responskurver, men er en modell – ikke en måling.

**Realistisk forventning:** mange forsøk er underdimensjonerte (Lewis & Rao). Si det på forhånd, ikke etterpå.

**Formulering:** «Det spørsmålet kan bare besvares med et forsøk. Den enkleste varianten er å slå av annonsering i
noen fylker i noen uker og sammenligne totalsalget. Det er noe din kontaktperson i TRY kan sette opp hvis dere vil ha
svaret.»

Ikke selg forsøket inn. Si hva det ville gitt, hva det koster i tapt leveranse, og la kunden velge. Og ikke la
«dette krever et forsøk» bli standardsvaret – bruk det bare når spørsmålet faktisk er kausalt. Se listen over hva
dataene *kan* svare på i hovedskillen.

---

## 6. Rekkevidde – ett gyldig tall, og bare ett

> Dette punktet er anvisninger til deg. Nevn aldri kilder, tabeller eller feltnavn i et svar – si «rekkevidde
> hentet fra Meta, gjennom TRY Data» hvis kunden spør hvor tallet kommer fra.

**Regelen:** rekkevidde oppgis bare som **totalrekkevidde per kampanje**, hentet fra den avdupliserte
rekkevidde-kilden. Ingen andre rekkevidde-tall skal brukes til noe. Det daglige rekkevidde-feltet som ligger på
leveransedataene er korrekt for **én enkelt dag** og for ingenting annet.

**Hvorfor det bare finnes ett gyldig nivå.** Rekkevidde teller unike personer i en periode. For å slå sammen to
tellinger må man vite hvem som er samme person i begge, og den koblingen finnes bare hos plattformen. Derfor kan
tallet ikke summeres over dager, over annonser, over annonsegrupper, over kampanjer, over kontoer eller over
plattformer. Plattformen gjør avdupliseringen for oss på kampanjenivå, og det er det eneste stedet jobben faktisk
er gjort.

**Sju ting som gjør at et rekkevidde-tall likevel blir feil:**

1. **Flere lesninger per kampanje.** Kilden leses på nytt hver natt, og hver lesning bærer *løpende total* til den
   datoen – ikke den nattens aktivitet. Summerer du lesningene, legger du sammen de samme pengene og de samme
   menneskene én gang per natt de ble observert. Bruk siste lesning når spørsmålet er «hvor mange har kampanjen
   nådd». Enkelte datoer har to lesninger med ulik historikk; bare den ene er merket som lesningen som skal brukes.
2. **Periodetall finnes, men bare for én kampanje.** Ny rekkevidde – personer som ble nådd for **første gang**
   siden forrige lesning – er det eneste gyldige periodetallet. Det kan legges sammen over uker og måneder for
   **én** kampanje, aldri på tvers av kampanjer: samme person kan være ny i to av dem.
3. **Rapporteringsvinduet glir.** Plattformen rapporterer bare rundt tre år tilbake, og grensen flytter seg en dag
   av gangen. En kampanje som startet før grensen mister den eldste dagen sin hver dag – og da faller ikke bare
   rekkevidden, men også visninger og forbruk. Det er vinduet som glir, ikke et resultat som endrer seg. Kilden
   merker hver lesning med hva periodetallet betyr, og bare den varianten som ligger helt innenfor vinduet *og*
   leverer, er et reelt periodetall.
4. **Negativ ny rekkevidde er alltid vindusglidning.** Kommer tallet ut negativt, er det en kampanje som har startet
   før grensen og som ikke lenger leverer. Si det, og gi den løpende totalen i stedet. Aldri rapporter det som
   personer som «sluttet å bli nådd».
5. **«Kampanjen er åpen» betyr ikke at den går.** Flagget sier bare at plattformen mangler sluttdato. Kampanjer som
   har stått stille i over to år er merket åpne.
6. **Tallet revideres.** Plattformen justerer ferske tall og bruker egne personvernterskler på persontellinger, så
   en ny lesning kan komme lavere tilbake enn den forrige. Det er en revisjon hos plattformen, ikke tapt rekkevidde.
   Tall fra de siste ukene er foreløpige. Har du oppgitt tallet før, si at det har endret seg og hvorfor –
   regelen i «Tall skal kunne gjenfinnes» gjelder fullt ut her.
7. **Aldri legg rekkevidde-kilden oppå leveransedataene.** De dekker de samme kampanjene og de samme pengene, målt
   over en periode i stedet for per dag. Forbruk og visninger finnes i begge. Svar fra én av dem, ikke fra
   summen.

**Oppgi alltid perioden sammen med tallet.** «Unike personer nådd mellom dato og dato» betyr ingenting uten
datoene. Er kampanjen eldre enn perioden, dekker tallet bare en del av kampanjens liv – og startet den for mer enn
rundt tre år siden, finnes det komplette tallet ikke lenger noe sted og kan ikke gjenskapes. Si det, i stedet for å
presentere delen som helheten.

**Dekningen er smal, og det skal sies.** Avduplisert rekkevidde hentes bare for Meta, og bare for kunder som har
bestilt det – datakilden faktureres per rad. Spør en kunde uten bestillingen om rekkevidde, er svaret at det ikke
samles inn for dem, ikke et tomt resultat. Står feltet i `kundekontekst.md` som «nei» eller «ukjent», finnes ikke
rekkevidde: gi visninger, som er summerbart, og si hvorfor det ikke er det samme.

**Beslektede feller i samme kilde:** anslått annonsehukommelse rapporteres bare for kjennskaps- og
engasjementskampanjer. 0 betyr «plattformen måler det ikke for denne kampanjetypen», aldri «ingen husket annonsen»
– si hvilken av de to, og snitt den aldri på tvers av kampanjetyper. «Alle klikk» i rekkevidde-kilden teller også
klikk som ble værende på plattformen, og er ikke samme mål som klikk i leveransedataene, som teller lenkeklikk.
Ikke sammenlign eller kombiner dem.

**Formulering til kunden:**

> «Rekkevidden for kampanjen var 148 000 unike personer mellom 4. og 31. august, med en frekvens på 4,3 – altså
> så hver av dem annonsen drøyt fire ganger i snitt. Jeg kan ikke legge sammen rekkevidden for de tre kampanjene
> til ett tall: da ville de som så flere av dem blitt talt flere ganger. Den største enkeltkampanjen nådde
> 148 000, og det er et minimum for hvor mange dere nådde i alt.»
