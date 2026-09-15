# Kanalnivå – operativ sparring uten å bli spesialist

Denne filen er for den hands-on markedsrådgiveren: hun jobber praktisk med kampanjer og uttak, har lav til middels
kompetanse på kanalnivå, og vil diskutere aktiviteter og prestasjoner uten å måtte grave i begrepsapparatet. Hun skal
ikke bli spesialist – hun skal kunne lokalisere hvor et problem sitter, og snakke presist om det.

Kildestyrke som ellers: **Høy** / **Middels** / **Lav**. Fulle referanser i `kilder.md`.

**Grunnregel for hele filen: ingen benchmarks.** Det finnes ingen etterrettelig norsk kilde med nivåtall for CTR, CPM,
VTR eller konverteringsrate. Spørsmålet «er dette et bra tall» besvares mot **kundens egen historikk og samme periode
i fjor** – aldri mot et bransjetall du ikke kan feste til en kilde, og aldri mot TRYs interne benchmarks.

---

## 1. Den diagnostiske trappen

Fem trinn. Gå nedover, stopp på det **første** trinnet der tallene avviker fra det som var forventet. Der sitter
problemet – ikke lenger ned.

| Trinn | Spørsmål | Det du ser på | Forveksles typisk med |
|---|---|---|---|
| 1. Leveranse | Nådde vi ut? | Budsjettforbruk mot plan, visninger mot plan, rekkevidde, fordeling over perioden | Kreativ. Underlevering må løses først – man kan ikke vurdere et uttak på volum som aldri ble levert. |
| 2. Oppmerksomhet | Ble det sett? | Synlighet, videovisninger ved 25/50/75/100 %, 2–3 sekunders visninger, visningstid | Relevans. Høy synlighet + lav respons leses som «feil målgruppe», men kan være at annonsen var synlig i ett sekund uten å bli sett på. |
| 3. Respons | Reagerte noen? | CTR, engasjement, hold-rate i video, kostnad per klikk | Konvertering. Høy CTR + lav konvertering leses som «dårlig nettside», men er like ofte et brudd mellom det annonsen lovet og det siden viser. |
| 4. Landing | Kom de dit vi ville? | Avvik mellom klikk og landingssidevisninger, lastetid, avvisning | Medieproblem. Et stort gap leses som «botrafikk», men er oftest treghet, samtykkebanner eller feil lenke. |
| 5. Konvertering | Fullførte de? | Konverteringsrate fra landing, frafall per trinn i kjøpsløpet, plattformtall mot analyseverktøy | Kampanjekvalitet. Fall kan være samtykke, sporing eller endret attribusjonsvindu. |

**Viktig forbehold om trappen:** den er et **leteverktøy**, ikke en modell for hvordan folk kjøper. Sekvensielle
effekthierarkier har svak empirisk støtte – en gjennomgang av over 250 vitenskapelige arbeider fant lite belegg for at
effekter følger en fast rekkefølge i tid *(Vakratsas & Ambler 1999, Høy)*. Bruk trappen til å finne hvor tallene
avviker. Ikke bygg en historie om kundereisen på den.

**Til rådgiveren:** «La oss gå trinnene i rekkefølge, så finner vi hvor det stopper. Ble det levert? Ble det sett? Ble
det klikket? Kom de inn? Kjøpte de?»

**Dokumentert underveis:**
- Synlighet er en *mulighet* til å se, ikke at noen så. Bransjestandarden er 50 % av flaten i minst ett sammenhengende
  sekund for display (30 % for store formater), to sekunder for video *(MRC/IAB, Høy)*.
- Klikk er en svak indikator på utfall: i en analyse av 263 millioner displayvisninger for 18 annonsører var
  korrelasjonen mellom klikk og konverteringer 0,01, mot 0,49 for hover *(Middels – sekundærgjengivelse, primærrapporten
  er ikke funnet)*.
- Sidehastighet betyr noe på trinn 4: 0,1 sekund raskere mobilside samvarierte med +8,4 % konverteringsrate i handel og
  +10,1 % i reise, men −1,9 % i leadsgenerering – 37 merkevarer over fire uker, med forfatternes eget forbehold om at
  utvalget ikke er representativt *(Deloitte/Google 2020, Middels)*.
- Avvik mellom plattform og analyseverktøy er delvis målemessig: GA4 modellerer nøkkelhendelser for brukere uten
  samtykke, tar bare inn modellerte tall ved høy nok datamengde, og attribuert konverteringsdata kan oppdateres i
  etterkant *(Google, Høy)*.

---

## 2. Kreativ, medie, tilbud eller landingsside?

Fire årsaker som forveksles konstant. De kan skilles med det som ligger i kontoen, uten spesialistverktøy – ved å
holde alt fast bortsett fra én dimensjon:

| Årsak | Kjennetegn | Slik isolerer du den |
|---|---|---|
| **Medie** | Varierer mellom plasseringer og kanaler | Samme uttak, ulike plasseringer → forskjellen er medie |
| **Kreativ** | Varierer mellom uttak, tidlig i trappen (trinn 2–3) | Ulike uttak, samme plassering og samme målgruppe |
| **Tilbud** | Varierer med budskapets innhold, slår ut sent (klikk → konvertering), likt på tvers av plasseringer | Samme uttak-form, ulikt budskap |
| **Landingsside** | Varierer med destinasjon, ikke med annonse | Flere ulike uttak mot samme side med samme svake konverteringsrate → siden |

**Den vanligste feilen:** å bytte kreativ når konverteringsraten faller. Kreativet virker først og fremst på trinn 2–3.
Et fall på trinn 5 med uendret CTR er nesten aldri uttaket.

**Til rådgiveren:** «Endre én ting av gangen. Samme uttak på ulike plasseringer viser om det er mediet. Ulike uttak på
samme plassering viser om det er kreativet.»

*Firedelingen er bransjepraksis – solid resonnering, men ingen fagfellevurdert kilde validerer den som metode. Si det
hvis noen spør.*

### Om kreativets betydning – og tallet du ikke skal bruke

Kreativet er trolig den viktigste enkeltfaktoren du kan påvirke, og det finnes uavhengig støtte for retningen: Kantar
koblet ca. 450 annonser mot en ROI-database og fant at kreativt sterke og effektive annonser ga over fire ganger så
mye profitt *(Middels/Lav)*, og Dentsu målte 17 % forskjell i erindring mellom sterk og svak kreativ *(Middels, metode
oppgitt)*.

**Men ikke bruk prosentandelen.** Det mye siterte «kreativ forklarer 47 % av effekten» kommer fra NCSolutions og
tåler ikke vekten: metoden er ikke publisert, tallene flytter seg mellom utgavene (kreativ 47 → 49 %, rekkevidde 22 →
14 %), populasjonen er amerikansk dagligvare og korttidssalg, og kreativ og målretting er i praksis ikke uavhengige
faktorer når algoritmen velger mottakere basert på respons på kreativet. Si **«mest»**, ikke **«X %»**.

---

## 3. Frekvens, metning og kreativ utmattelse

Dette er faktisk godt dokumentert – i motsetning til prosentandelene over.

- Holdning til merket følger en omvendt U: den stiger med eksponering til læringen mettes, med maksimum rundt ti
  eksponeringer, mens erindring stiger mer lineært og flater ut senere. Effektene forvitrer over tid. Meta-analyse av
  37 eksperimentelle studier og 312 effektstørrelser *(Schmidt & Eisend 2015, Høy)*.
- Feltdata skiller **wearout** (avtakende, men fortsatt positiv effekt) fra **weariness** (negativ marginaleffekt).
  Blant over 12 000 brukere på over 400 nettsteder viste rundt 24 % ekte weariness, og frekvenstak basert på
  profilering ga rundt 15 % bedre kampanjeeffekt *(Chae, Bruno & Feinberg 2019, Høy)*.

**Slik ser utmattelse ut i kontoen** *(bransjepraksis – kurveformen er dokumentert, diagnosetegnene er ikke)*:
- frekvensen stiger mens rekkevidden står stille, og
- **bare det gamle uttaket** faller, mens nye uttak i samme oppsett holder seg.

**To feiltolkninger å fange:**
1. «Ti eksponeringer» er ikke et frekvenstak. Tallet kommer fra kontrollerte eksperimenter på holdning, ikke fra
   annonsekontoer, og kan ikke overføres som driftsmål.
2. Fallende CTR alene er ikke utmattelse. Faller CTR med **uendret** frekvens, er det som regel at algoritmen har brukt
   opp den lettest responderende delen av målgruppen – ikke at uttaket er slitt.

**Til rådgiveren:** «Utmattelse ser slik ut: frekvensen stiger, rekkevidden står stille, og bare det gamle uttaket blir
dårligere. Er alle uttakene dårligere samtidig, er det noe annet.»

---

## 4. Leveranse og pacing

Trygt å lese: om budsjettet er brukt, om leveransen er jevn, om rekkevidden vokser eller står stille, om frekvensen
stiger.

**Dokumenterte mekanikker som forklarer «rare» kurver:**
- Google Ads kan bruke opptil **to ganger** gjennomsnittlig dagsbudsjett på én dag, og opptil 30,4 ganger på en måned.
  Én dag med dobbelt forbruk er normal drift, ikke feil *(Google, Høy)*.
- Læringsperioder gir reelt ustabile første dager. Google: opptil tre uker eller 1–2 kjøpssykluser, og statusen
  nullstilles ved endring i budstrategi eller struktur *(Høy)*. TikTok: volatiliteten avtar etter ca. 25 resultater
  eller sju dager *(Høy)*. Metas ofte siterte «50 hendelser per uke» kunne vi **ikke** verifisere mot offisiell kilde –
  omtal den som bransjepraksis.

**Tre vanlige feil:**
1. Å konkludere på tall fra en kampanje som fortsatt er i læringsfase.
2. Å lese en enkelt topp- eller bunndag som pacingfeil.
3. Å lese **gjennomsnittsfrekvens** som om alle fikk den frekvensen. Et snitt på 3 kan bety at halve målgruppen så
   annonsen én gang og en liten gruppe så den tjue ganger.

**Til rådgiveren:** «Se kurven over hele perioden, ikke enkeltdager – og vent til læringsfasen er ute før du dømmer.»

---

## 4B. Når kostnaden stiger: CPM og auksjonspress

Et av de vanligste operative spørsmålene: «hvorfor har CPM steget?» Del svaret i det du kan lese av dataene og det du
ikke kan.

**Kan leses av dataene:**
- **Endret plasseringsmiks.** Samme kampanje, ulik fordeling mellom flater. Dyrere flater vokser → snitt-CPM stiger
  uten at noen pris er endret.
- **Endret formatmiks.** Video og store formater koster mer enn enkle bannere.
- **Endret målgruppebredde eller geografi**, der det er synlig i leveransen.
- **Budsjettøkning.** Mer budsjett kjøper bredere og dyrere inventar. Dette er den vanligste forklaringen, og den
  peker på nevneren, ikke på kvaliteten.
- **Stigende frekvens mot flat rekkevidde** – du kjøper stadig dyrere kontakter i en målgruppe som er i ferd med å bli
  brukt opp.

**Kan ikke leses av dataene:**
- Konkurransepress i auksjonen. Sesong (jul, Black Week, valg, store kampanjeperioder i kategorien) driver prisene, men
  du ser bare din egen side av auksjonen. Vi har **ingen åpen kilde** med norske sesongtall for CPM – oppgi ingen.
- Endringer i plattformens egen prising eller inventar.
- Om konkurrenten har økt budsjettet.

**Til rådgiveren:** «CPM har steget 18 %. Halvparten forklares av at mer av budsjettet gikk til video, som koster mer.
Resten kan være auksjonspress i sesongen – det ser vi ikke fra vår side, bare at prisen er høyere. CPM alene sier
uansett ingenting om hvor mye oppmerksomhet vi fikk for pengene.»

*Mekanismene er dokumenterte der de handler om miks og budsjett (nevnereffekten); sesong- og konkurransepress er
bransjekunnskap uten åpne norske tall.*

---

## 4C. Frekvenstak

Vanlig spørsmål: «kan vi skru det opp/ned?» Slik svarer du.

- **Retningen kan diskuteres fritt.** Metningstegn (frekvens opp, rekkevidde flat) taler for å senke taket eller rotere
  uttak. Lav frekvens i en kampanje med kjennskapsmål kan tale for å heve det.
- **Riktig nivå krever test.** Litteraturens tall (metning rundt ti eksponeringer for holdning) kommer fra kontrollerte
  eksperimenter, ikke fra annonsekontoer, og kan ikke brukes som driftsmål. Profilbaserte tak ga rundt 15 % bedre
  effekt i feltdata *(Chae m.fl. 2019, Høy)* – det er et argument for å bruke tak, ikke for et bestemt nivå.
- **Konsekvensen for leveransen skal alltid nevnes:** et strammere tak begrenser hvor mye som kan leveres, og kan gi
  underlevering mot slutten av perioden. Et løsere tak gir mer frekvens på de samme folkene, ikke mer rekkevidde.
- **Om endringen påvirker læringsfasen** varierer mellom plattformene, og vi har **ingen verifisert kilde** som dekker
  dette på tvers. Si det, og la spesialisten avgjøre – ikke gjett.

**Til rådgiveren:** «Retningen er jeg med på – frekvensen stiger mens rekkevidden står stille, så et strammere tak er
verdt å prøve. Nivået kan jeg ikke sette fra tallene, og et strammere tak betyr at vi leverer mindre volum. Det bør
spesialisten sette, og jeg ville målt rekkevidde og frekvens i to uker etterpå.»

---

## 5. Format og plassering – hva som er sammenlignbart

Rå CPM-sammenligning mellom formater er misvisende, fordi en visning ikke er samme vare i to formater.

- Oppmerksomhetsmåling viser store forskjeller mellom flater: bare 43 % av 30-sekunders TV-reklamer fikk faktisk
  oppmerksomhet, mot 74 % som tilfredsstilte synlighetskravet – og formater som ser billige ut på CPM blir dyre målt i
  oppmerksomme sekunder *(Lumen/WARC 2021, Middels; forfatteren forbeholder selv at metoden viser hva som er mulig, ikke
  hva som faktisk skjer)*.
- Lyd av/på varierer dramatisk mellom plattformer – fra 82 % til 5 % lyd på – og samme kreativ presterer i tråd med
  plattformens oppmerksomhetsnivå *(Nelson-Field 2022, Middels; plattformene er anonymisert, utvalgsstørrelse ikke
  oppgitt)*.
- Lengre eksponering ga høyere erindringsløft: 40 % høyere ved 5+ sekunder enn ved 1+ sekund, over 16 kampanjer
  *(Teads/Lumen 2023, Middels)*.
- **Motvekt, som skal med for balansen:** Kantar fant over 873 kampanjer og 3,2 mrd. USD i medieinvestering at
  oppmerksomhet per visning *ikke* korrelerte med kostnadseffektivitet – digitale kanaler bygget merke effektivt tross
  lavere oppmerksomhet per visning *(Middels/Lav)*.

Oppmerksomhetsfeltet er nesten utelukkende leverandørdrevet, og kildene peker delvis i ulike retninger. Presenter
oppmerksomhet som et **bedre, men omstridt** mål – ikke som fasit.

**Regel:** sammenlign format mot **seg selv over tid**, ikke format mot format. Og sjekk definisjonen før du
sammenligner «videovisning» på tvers av plattformer – den varierer.

**Til rådgiveren:** «En visning i feed og en visning inne i en videostrøm er ikke samme vare. Vi kan følge hvert format
over tid, men vi kan ikke kåre en vinner mellom dem på CPM.»

---

## 6. Målgruppe og levering – på konseptnivå

Det avgjørende poenget, og det er dokumentert, ikke antatt: **annonsøren velger et rom av mulige mottakere,
algoritmen velger hvem i rommet som faktisk får annonsen.** Facebooks leveringssystem ga betydelig skjevhet i
mottakersammensetning uavhengig av annonsørens målretting – og både budsjettet og annonsens innhold bidro selvstendig
til skjevheten *(Ali m.fl. 2019, Høy)*.

Fire konsekvenser å bruke aktivt:

1. **«Vi traff feil målgruppe» kan nesten aldri leses direkte av dataene.** Rapporten viser hvem som *ble levert til*,
   ikke hvem som *kunne* blitt levert til. Sammenligningen som mangler, finnes ikke i kontoen.
2. **Kreativet er en del av målrettingen.** Byttet du uttak, endret du hvem som fikk se annonsen. Da kan kreativeffekt
   og målgruppeeffekt ikke skilles i etterkant.
3. **Rekkevidde er ikke additiv.** Den kan ikke summeres på tvers av plasseringer eller kanaler; overlappet er ukjent.
4. **Målgruppeoverlapp** mellom egne kampanjer er en reell usikkerhet, men påstanden om at man «byr mot seg selv» fant
   vi ingen primærkilde for – kun leverandørblogger. Omtal overlapp som usikkerhet, ikke som mekanikk.

**Til rådgiveren:** «Du bestemmer hvem som *kan* få annonsen. Systemet bestemmer hvem som *får* den – og rapporten
viser bare det siste.»

---

## 7. Hva rådgiveren kan få svar på, og hva som må videre

**Kan besvares fra dataene – svar direkte, uten forbehold utover støybåndet:**
1. Ble budsjettet brukt, og jevnt fordelt over perioden?
2. Nådde vi planlagt volum av visninger og rekkevidde?
3. Hvilket trinn i trappen avviker først?
4. Stiger frekvensen mens rekkevidden står stille?
5. Faller et **bestemt** uttak over tid mens de andre i samme oppsett holder seg?
6. Presterer samme uttak ulikt på ulike plasseringer?
7. Er det et gap mellom klikk og landingssidevisninger?
8. Konverterer ulike landingssider ulikt med samme uttak foran?
9. Hvor i kjøpsløpet faller folk av?
10. Er kampanjen fortsatt i læringsfase, og er statusen nylig nullstilt?
11. Hvordan er retningen over tid for samme oppsett, mot samme periode i fjor?

**Krever spesialist eller forsøk – diskuter gjerne, men konkluder ikke:**
1. «Traff vi riktig målgruppe?» – krever eksperiment.
2. «Hva ville skjedd uten kampanjen?» – krever geo-test, holdout eller løftmåling.
3. «Hvor mye skyldes kreativet og hvor mye mediet?» – krever kontrollert test der bare én dimensjon varierer.
4. «Hvilket frekvenstak er riktig?» – krever test; litteraturens tall er eksperimentelle, ikke driftstall.
5. «Er dette et bra tall?» – mot egen historikk, ja. Mot bransjen: **ingen benchmark skal oppgis.**
6. «Hvor stort er overlappet mellom kampanjene våre?» – krever spesialistverktøy, og svaret er usikkert.
7. «Stemmer plattformtallene med virkeligheten?» – krever gjennomgang av sporing, samtykke og attribusjonsvinduer.
8. «Bygget dette merkevaren?» – krever brand lift eller tracking, ikke annonsekonto.
9. Endring av budstrategi, kampanjestruktur eller budsjettnivå – utløser ny læringsfase. Diskuter på konseptnivå,
   men grepet gjøres av spesialisten, og konsekvensen for læringsfasen skal alltid nevnes.

---

## 8. Begreper i klarspråk

Bruk disse når et begrep må forklares. **Forklar bare når det trengs** – bruker rådgiveren begrepet riktig, la det
ligge. Å forklare «CTR» til noen som nettopp brukte det korrekt, er nedlatende.

1. **Uttak** – den konkrete annonsefilen eller -enheten som er produsert for en gitt flate og et gitt format.
2. **Visning** – én gang annonsen ble levert til en skjerm. Ikke det samme som at noen så den.
3. **Rekkevidde** – antall unike personer som fikk minst én visning. Kan ikke summeres på tvers av kanaler.
4. **Frekvens** – gjennomsnittlig antall visninger per person. Skjuler at noen fikk én og noen fikk mange.
5. **Plassering** – hvor annonsen faktisk sto: i feed, i en story, inne i en videostrøm.
6. **Format** – annonsens form: still, video, karusell, lengde, sideforhold.
7. **Synlighet** – bransjens minstemål for at annonsen *kunne* blitt sett: 50 % av flaten i minst ett sekund for
   display, to sekunder for video.
8. **Oppmerksomhetssekunder** – målt tid noen faktisk hadde blikket på annonsen. Strengere mål enn synlighet.
9. **CPM** – pris per tusen visninger. Sier ingenting om hvor mye oppmerksomhet de tusen ga.
10. **CTR** – andel visninger som ga klikk. En respons-indikator, og en svak indikator på salg.
11. **Konverteringsvindu** – hvor lenge etter en visning eller et klikk en handling får telle som resultat.
12. **Budstrategi** – regelen du gir plattformen for hva den skal optimalisere mot, og hva den får betale for det.
13. **Læringsfase** – perioden der systemet leter etter mønster og resultatene svinger unormalt mye. Tallene fra denne
    perioden kan ikke tolkes.
14. **Pacing** – hvordan budsjettet fordeles utover perioden. Enkeltdager kan lovlig ligge langt over dagsnivået.
15. **Frekvenstak** – øvre grense for hvor mange ganger samme person skal få annonsen.
16. **Kreativ rotasjon** – å bytte eller veksle mellom uttak i samme oppsett, så ett uttak ikke slites ut.
17. **Kreativ utmattelse** – at samme uttak gradvis presterer dårligere fordi de samme folkene har sett det flere ganger.
18. **Målgruppeoverlapp** – at flere av egne kampanjer sikter på delvis samme mennesker. Hvor stort det er, kan sjelden
    leses av rapporten.
19. **Algoritmisk levering** – at plattformen, ikke du, velger hvem inne i målgruppen som får annonsen – og at uttakets
    innhold og budsjettet påvirker det valget.
20. **Avhopp før landing** – folk som klikket, men aldri kom inn på siden. Sees som avvik mellom klikk og
    landingssidevisninger.

---

## 9. Støy på uttaksnivå – strengere, ikke løsere

Operativ sparring handler om små tall: ett uttak, én plassering, én uke. Der er tolkningsvernet **viktigere**, ikke
mindre viktig. Volumene per uttak er ofte under terskelen for å konkludere om forskjeller i det hele tatt.

Praktisk håndtering: si støybåndet **én gang** tidlig i samtalen, og jobb deretter med topp, bunn og retning –
ikke med en rangering av alt imellom.

> «På uttaksnivå har vi 20–40 kjøp per uttak. Der kan vi se hvilke som ligger tydelig øverst og nederst, men ikke
> rangere de fem i midten – forskjellen mellom dem er mindre enn svingningen. Skal vi se på topp og bunn?»

Det er et ærlig og brukbart svar, og det er langt bedre enn både en presis rangering som ikke holder, og et «vi kan
ikke si noe».

**Og nektelsen skal aldri stå alene.** Kan du ikke rangere, lever likevel tre ting i samme svar: hva du *kan* si (uttak
som faller mot sin egen historikk, miksendringer, leveranse), hvorfor rangeringen ikke holder, og setningen brukeren
kan si videre til den som spurte. Mønster 18 i `samtalemonstre.md` har formen.
