# Metrikker – hva de sier, hva de ikke sier, og hva folk tror

Bruk denne når en metrikk skal forklares, eller når kunden bygger en konklusjon på den. Kolonnen «typisk
feilslutning» er den du skal fange. Kilder i `kilder.md`.

---

## Leveranse

**Visninger (impressions)** – antall ganger annonsen ble levert.
*Sier ikke:* om noen så den, husket den, eller brydde seg. En levert annonse er en faktura, ikke en effekt.
*Feilslutning:* «Vi nådde 3 millioner» – dette er visninger, ikke mennesker.

**Rekkevidde (reach)** – antall unike enheter eller kontoer plattformen tror er unike personer.
*Sier ikke:* antall mennesker.

**Rekkevidde kan ikke legges sammen. Ikke over dager, ikke over uker, ikke over annonser eller kampanjer, ikke
over plattformer.** Dette er den viktigste enkeltregelen i denne filen, og den brytes oftest fordi tallet ser
summerbart ut.

*Begrunnelsen, og den skal du kunne si høyt:* rekkevidde er en telling av **unike** personer innenfor en
avgrenset periode. Skal to perioder legges sammen, må man vite hvem som er den samme personen i begge – og den
informasjonen finnes bare hos plattformen, aldri i tallene vi får ut. Summerer du sju dager, teller du personen
som så annonsen alle sju dagene sju ganger. Det er ikke en unøyaktighet, det er en annen størrelse: du har regnet
ut noe som ligner visninger, og kalt det mennesker.

*Hvor stort blir avviket:* målt august 2026 på en kundekampanje ga summert daglig rekkevidde over et år
16,7 millioner personer – tre ganger Norges befolkning. Det åpenbart gale tallet er det ufarlige. Summering av
tre månedstall overdrev det sanne tremånederstallet med 15–23 %, og *det* er den farlige feilen, fordi svaret
fortsatt ser troverdig ut. Samme mekanisme rammer frekvens: for en alltid-på-kampanje var riktig frekvens for
august 4,3, mens summerte dagstall impliserte 1,75.

*Feilslutning 1:* «Vi nådde 340 000 i august» – regnet av dagstall. Det er ikke rekkevidde.
*Feilslutning 2:* «Vi nådde 2 millioner nordmenn» – summert på tvers av plattformer. Riktig: «Meta rapporterer X
unike, Google Y – de overlapper, og vi vet ikke hvor mye.»

**Hvilket rekkevidde-tall som får brukes.** Bare det avdupliserte tallet **per kampanje**, fra den kilden som er
laget for det. Det er det eneste nivået der tallet er en reell telling av mennesker. Er ikke det tilgjengelig for
kunden, finnes ikke rekkevidde for dem – si det, og bruk visninger, som *er* summerbart. Se punkt 6 i
`plattformforbehold.md` før du oppgir noe rekkevidde- eller frekvenstall.

**Frekvens** – gjennomsnittlig antall visninger per nådd person.
*Sier ikke:* fordelingen. Frekvens 4 kan bety at noen fikk 40 og de fleste fikk 1.
*Må regnes på samme nivå som rekkevidden:* visninger delt på rekkevidde for **samme kampanje og samme periode**.
Regnet av dagstall blir den systematisk for lav, fordi nevneren er blåst opp.
*Feilslutning:* «Alle så den fire ganger.»

**CPM** – innkjøpspris per tusen visninger.
*Sier ikke:* om oppmerksomheten var verdt noe. Rå CPM-sammenligning mellom kanaler er meningsløs når
gjennomføringsgrad og synlighet er ulik.
*Feilslutning:* «Lav CPM = effektivt.» Billig oppmerksomhet er ofte oppmerksomhet ingen ga.

**Viewability / synlighet** – bransjestandard (MRC/IAB): minst 50 % av annonsearealet synlig i minst 1 sekund
(30 % for store formater), 2 sekunder for video.
*Sier ikke:* at noen så på skjermen. Googles egen formulering: «Active View can tell you when ads are viewable, but
it can't guarantee that a user is looking at the screen.»
*Feilslutning:* «100 % synlighet betyr at annonsen ble sett.»

**VTR / VCR (gjennomføringsgrad video)** – andel som spilte gjennom.
*Sier ikke:* om budskapet nådde fram. Autoplay uten lyd gjør høye tall billige.
*Feilslutning:* «Høy gjennomføring = høy oppmerksomhet.»

---

## Atferd

**CTR – klikkrate** – andel av visninger som ble klikk.
*Sier ikke:* om annonsen virket. En bransjestudie av 60+ kampanjer (Flashtalking, 2018) fant at kreativer i
øverste kvartil på faktisk ytelse hadde **lavere** CTR enn de i nederste – altså negativt korrelert. *(Middels –
én bransjestudie.)*
*Feilslutning:* «Høy CTR = god annonse.» Ofte betyr det bare at annonsen lurte noen til å klikke.

**Engasjementsrate** – andel som likte, kommenterte eller delte.
*Sier ikke:* noe om salg. Vi fant **ingen** fagfellevurdert kilde som knytter engasjement til inkrementelt salg – si
det eksplisitt hvis kunden bygger på det.
*Feilslutning:* «Engasjement = effekt.»

**Konverteringsrate** – andel av besøk eller klikk som konverterte.
*Sier ikke:* om volumet vokste. Faller ofte når man skalerer riktig, fordi man kjøper bredere trafikk.
*Feilslutning:* «Konverteringsraten falt, altså ble noe dårligere.»

---

## Forretning

**Konverteringer (plattformens tall)** – handlinger utført av folk som ble eksponert innenfor et tidsvindu.
*Sier ikke:* hvem som handlet *fordi* de ble eksponert. Randomiserte forsøk viser at plattformnære anslag var feil med
en faktor tre i halvparten av de undersøkte tilfellene.
*Feilslutning:* «Meta ga oss 412 kjøp.» Riktig: «412 av kjøperne hadde sett Meta-annonsen først. Noen av dem hadde
kjøpt uansett.»

**ROAS (rapportert)** – omsetning plattformen tilskriver seg, delt på kostnad.
*Sier ikke:* inkrementell avkastning. eBay-forsøket: naiv beregning ga +4 173 %, eksperimentet −63 %.
*Feilslutning:* «ROAS 8 betyr 8 kroner tilbake per krone.» Riktig: «8 kroner ble registrert etter kontakt med
annonsen. Hvor mye som kom *på grunn av* den, vet vi ikke uten forsøk.»

**CPA – kostnad per konvertering** – forbruk delt på tilskrevne konverteringer.
*Sier ikke:* kostnad per *ny* kunde. Laveste CPA finnes systematisk der du høster egen etterspørsel.
*Feilslutning:* «Lav CPA = effektiv kanal.»

**Blandet CPA / blandet ROAS** – totalt forbruk mot totale konverteringer.
*Sier ikke:* noe som helst om enkeltkanaler, og påvirkes av miksendringer (Simpsons paradoks) og av
merkevaresøkets andel.
*Feilslutning:* å styre etter blandet CPA og tro at man styrer kanalene.

**CAC – kundeanskaffelseskostnad**
Holdbart bare når det måles på **nye** kunder og på inkrementelt tilkomne. Ellers er det CPA med finere navn.

**LTV / CAC**
Selve regnestykket er nyttig – forholdstallet «3» er ikke et forskningsfunn. Det stammer fra en
venturekapital-blogg (Skok, *SaaS Metrics 2.0*, 2013) uten studie eller datasett bak. Bruk det som varsellampe over
tid, aldri som karakter. LTV skal bygges på bidragsmargin, ikke omsetning, og diskonteres. *(Se `kilder.md`.)*

---

## Merkevare

**Kjennskap, vurdering, førstevalg (fra undersøkelser)**
Ledende indikatorer, ikke resultater. Nyttige, men: forbrukerbaserte merkevaremål samsvarer bare delvis med
salgsbasert merkevareverdi (Datta, Ailawadi & van Heerde, 290 merker, 25 kategorier, 10 år). Høy korrelasjon mellom
merkevarescore og markedsandel skyldes i stor grad at store merker skårer høyt fordi de er store. *(Høy)*
*Feilslutning:* «Kjennskapen økte, altså virket kampanjen kommersielt.»

**Share of voice** – andel av kategoriens reklamestøy.
Nyttigst i forhold til markedsandel (se `forretningsramme.md`).
*Feilslutning:* «Vi økte budsjettet 20 %, da bør vi vokse.» Konkurrenten kan ha økt 40 %.

---

## Regler for hvordan du bruker denne filen

1. Forklar metrikken **før** du bruker den i en konklusjon – men bare når mottakeren ikke har vist at hun kan den. I
   operativt modus, der rådgiveren selv bruker begrepet riktig, hopper du over forklaringen. Og heng ikke på et
   forbehold om metrikken (f.eks. at CTR er en svak indikator på salg) med mindre det faktisk endrer svaret hun ba om.
2. Aldri sammenlign samme metrikk på tvers av plattformer uten å nevne at definisjonene er ulike.
3. Møter du en metrikk som ikke står her: forklar hva den måler, og si eksplisitt hva den *ikke* måler.
4. Ingen metrikk er «dårlig» i seg selv. Rekkevidde er riktig KPI for et kjennskapsmål. Spør hvilken beslutning
   tallet skal informere før du avviser det.
