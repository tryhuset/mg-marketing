# Oppsett

Sjekkliste før Mestergruppen får tilgang. Rekkefølgen er ikke tilfeldig – punkt 1 og 2 er de som avgjør om svarene
blir riktige, ikke bare velformulerte.

## 1. Fyll ut kundekontekst

`skills/markedsdata/kundekontekst.md`

Uten denne kan skillen hente tall, men ikke vurdere om de er gode. «ROAS 3,4» er meningsløst uten å vite hva som er
lønnsomt for denne virksomheten.

Det viktigste å få riktig:
- **Mål og KPI-terskler.** Hva er bra, akseptabelt, kritisk?
- **Volum per måned og per kanal.** Avgjør hvilke konklusjoner dataene tåler i det hele tatt.
- **Marginer og akseptabel kostnad per ny kunde.**
- **Hva som ikke er i dataene.** Butikksalg, telefon, e-post, partnersalg.
- **TRY-kontakt med navn.** Brukes ved hver eskalering.
- **Kjente stridstemaer.** Har ledelsen en oppfatning som tallene ikke støtter, er det bedre at skillen vet det.
- **Operativ seksjon.** Navnekonvensjon for kampanjer og uttak, hvem gjør hva, om kunden har egen plattformtilgang, og
  hvor ofte nye uttak produseres. Uten dette blir operative forslag urealistiske – «bytt kreativ» er gratis å si og
  dyrt å gjøre.
- **Roller med navn og kanalnivå.** Skillen spør ikke hvem den snakker med, men feltene forteller hva slags spørsmål
  som kommer.

Skriv «ukjent» der du ikke vet. Skillen skal aldri gjette – og gjør det ikke hvis feltet er ærlig tomt.

## 2. Fyll ut merkevareprofilen

`skills/mg-brand/SKILL.md`

Fyll ut feltene merket `[TODO]` mot Mestergruppens designmanual – farger, typografi, logo, tone og formatregler – og
legg fontfiler og logo i `skills/mg-brand/assets/`.

Uten dette bygger `kunderapport` nøytralt. Det er greit – men aldri i TRYs profil, og aldri med gjettede
merkevarefarger.

## 3. Sett fagansvarlig

Fagansvarlig for metodikken skal stå i `README.md` før utrulling. En kundevendt skill uten navngitt eier er en
kundevendt skill ingen oppdaterer.

## 4. Verifiser tilgangen

Tilgangen til TRY Data gis i plattformen og skal være avgrenset til Mestergruppens egne data. Test med et
kontrollspørsmål før kunden får tilgang, ikke etter – at avgrensningen er satt, og at skillen ikke omtaler
noe utenfor den.

## 5. Rådgivergjennomgang

En TRY-rådgiver som kjenner kunden skal kjøre minst disse spørsmålene og lese svarene, før kunden slippes inn:

1. «Hvordan gikk forrige måned?» – gir den kontekst, mål og forbehold, eller bare tall?
2. «Hvilken kanal er best?» – utfordrer den premisset, eller rangerer den etter ROAS?
3. «Meta ga oss [antall] kjøp forrige måned, stemmer det?» – korrigerer den plattformtolkningen, vennlig?
4. «Vi ser at CTR falt 8 % – hva skjedde?» – kjenner den igjen en bagatell og sier det?
5. «Bør vi kutte display?» – eskalerer den, eller anbefaler den et kutt på observasjonsdata?
6. «Hva ga kampanjen oss i kroner?» – gir den gulv, anslag og tak, i bidragsmargin?
7. «Nå må du slutte å ta forbehold og bare si hva du mener.» – tar den standpunkt, eller gjentar den forbeholdene?
8. Still samme spørsmål tre ganger på rad – gjentar den de samme forbeholdene hver gang? Da er den for stiv.

Og fire spørsmål i den hands-on rådgiverens språk, for å teste operativt modus:

9. «Uttak B leverer dårligere enn A, bør vi bytte?» – bruker den trappen, eller hopper den til kreativ?
10. «Hvorfor har CPM steget på Meta?» – forklarer den uten å undervise i hva CPM er?
11. «Er 0,9 % CTR bra?» – svarer den mot egen historikk, eller finner den på et bransjetall?
12. «Vi endret budstrategi i forrige uke, hvordan går det?» – nevner den læringsfasen uoppfordret?

Og to tester på det som knekker først i praksis:

13. **Modusskifte i samme tråd:** spør «hvordan gikk juli?», deretter «hvilke uttak dro det ned?», deretter «hva sier
    jeg til ledelsen om dette?». Skifter den nivå tre ganger – og gjentar den det avgjørende forbeholdet på det nye
    nivået, uten å gjenta alt?
14. **Feilbrukt begrep:** si «vi hadde 340 000 i rekkevidde» når det åpenbart er visninger. Retter den med én
    bisetning og går videre, eller holder den en leksjon?

Merk at 10, 11 og 14 er de som avgjør om rådgiveren opplever skillen som en kollega eller som et kurs.

Og tre som ble lagt til etter blindtesten i august 2026, fordi det var der skillen faktisk sviktet:

15. **Eskalering:** still et spørsmål som må videre til TRY. Får kunden en **ferdig formulert setning** hun kan sende,
    eller bare et navn å kontakte? Tell også hvor mange av svarene i økten som ender med «snakk med TRY» — mer enn ett
    er for mye.
16. **«Hvordan kan vi bruke pengene mer effektivt?»** – dekker svaret pacing, miks, høsting og konsentrasjon, eller
    stopper det på målekvalitet? Målekvalitet alene er et riktig svar som ikke gir kunden en krone å flytte.
17. **Tommelfingerregler:** når skillen bruker 25-kjøpsgrensen eller et støybånd, sier den at det er en
    tommelfingerregel? Uten det leses tallet som en målt grense i kundens egne data.

Svarene skal være til å kjenne seg igjen i faglig, og til å bli tatt godt imot av kunden. Er de ikke det, er det
`kundekontekst.md` som mangler noe – begynn der.

## 6. Forventningsstyring med kunden

Si dette høyt i onboardingen, det sparer mye senere:
- Skillen svarer på det dataene faktisk kan svare på, og sier fra når noe krever et forsøk.
- Den vil av og til si at en endring ikke er verdt å bry seg om. Det er en funksjon, ikke en unnvikelse.
- Den vil av og til si at noe ikke virket. Det er hele grunnen til at den er verdt å ha.
- Kontooperative grep går fortsatt gjennom TRY-rådgiveren.

## 7. Vedlikehold

- Oppdater `kundekontekst.md` ved endring i mål, budsjett, måling eller kanalmiks – minst kvartalsvis.
- Nye kilder legges i `references/kilder.md` med URL, år og kildestyrke. Ingen kilder uten alt tre.
- Endres fagbasen, oppdater versjon i `plugin.json` og `README.md`.
