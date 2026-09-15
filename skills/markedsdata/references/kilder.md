# Kilder

Kildene her er hentet fram og kontrollert under utarbeidelsen av skillen (august 2026). Der en kilde bare er lest som
sammendrag, eller ikke lot seg åpne direkte, står det i oppføringen – og da skal tallet behandles som uverifisert.
Oppgi aldri en kilde som ikke står i denne filen, og aldri et tall du ikke kan feste til en av dem. Se listen over
kjente kildehull nederst før du gjengir et tall du er usikker på. Kildestyrke: **Høy** = fagfellevurdert forskning eller
offisiell plattform-/myndighetsdokumentasjon · **Middels** = én primærkilde, bransjerapport med metode, fagbok, eller
sekundærgjengivelse av primærkilde · **Lav** = blogg eller leverandørinnhold.

## Plattformtall vs. faktisk effekt

- **Gordon, Zettelmeyer, Bhargava & Chapsky (2019),** «A Comparison of Approaches to Advertising Measurement»,
  *Marketing Science* 38(2). 15 randomiserte forsøk på Facebook, 500 mill. observasjoner. Feil med faktor tre i
  halvparten av studiene. **Høy.** https://www.kellogg.northwestern.edu/faculty/gordon_b/files/fb_comparison.pdf
- **Blake, Nosko & Tadelis (2015),** «Consumer Heterogeneity and Paid Search Effectiveness», *Econometrica* 83(1).
  eBay-eksperimentet: 99,5 % av merkevareklikk gjenvunnet organisk; ROI naiv +4 173 %, eksperimentelt −63 %.
  **Høy.** https://www.nber.org/system/files/working_papers/w20171/w20171.pdf
- **Simonov, Nosko & Rao (2018),** «Competition and Crowd-Out for Brand Keywords in Sponsored Search»,
  *Marketing Science* 37(2). 2 517 merkevarer; 2–3 % inkrementell trafikk; konkurrent kan hente 15–20 %.
  **Høy.** https://business.columbia.edu/sites/default/files-efs/pubfiles/26238/competition_crowdout.pdf
- **Lewis, Rao & Reiley (2011),** «Here, There, and Everywhere: Correlated Online Behaviors», WWW. Activity bias, med
  **merkevaresøk** som utfallsmål: sann effekt 5,4 %, naiv eksponert-mot-ueksponert 1198 %. **Høy.** http://www.davidreiley.com/papers/HereThereEverywhere.pdf
- **Lewis & Rao (2015),** «The Unfavorable Economics of Measuring the Returns to Advertising», *QJE* 130(4). 25 RCT-er;
  3 av 25 kunne skille 50 % ROI fra null. **Høy.** https://gwern.net/doc/economics/advertising/2015-lewis.pdf
- **Shapiro, Hitsch & Tuchman (2021),** «TV Advertising Effectiveness and Profitability», *Econometrica*. 288
  merkevarer; elastisitet rundt 0,014 i basismodellen (arbeidspapirversjonen; publiserte anslag varierer noe – bruk
  «rundt 0,01–0,02»). **Høy** for funnet, **Middels** for det enkelte desimaltallet. https://www.nber.org/system/files/working_papers/w27684/w27684.pdf
- **Johnson, Lewis & Nubbemeyer (2017),** «Ghost Ads», *Journal of Marketing Research*. Dokumenterer at PSA-tester
  bryter sammen på optimaliserte plattformer. **Høy.** https://journals.sagepub.com/doi/10.1509/jmr.15.0297
- **Vaver & Koehler (Google Research),** «Measuring Ad Effectiveness Using Geo Experiments». **Høy.**
  https://services.google.com/fh/files/blogs/geo_experiments_final_version.pdf

## Statistikk, støy og feilslutninger

- **van Belle, «Statistical Rules of Thumb»** (Lehr-regelen for utvalgsstørrelse: n = 16/Δ²). **Middels** – lest via
  tredjeparts sammendrag av boka, ikke originalen. Tabellen og støybåndene i `tolkningsvern.md` er utregnet fra
  formelen og fra tellestatistikk, og skal oppgis som tommelfingerregler.
  https://rstudio-pubs-static.s3.amazonaws.com/201750_c17bc51d8553452d997ba4d258b0249f.html
- **Kohavi, Henne & Sommerfield (2007),** «Practical Guide to Controlled Experiments on the Web», KDD. **Høy.**
  http://ai.stanford.edu/~ronnyk/2007GuideControlledExperiments.pdf
- **Kohavi, Deng, Longbotham & Xu (2014),** «Seven Rules of Thumb for Web Site Experimenters», KDD. Twymans lov,
  nevnerfeller, familiewise feilrate. **Høy.** https://exp-platform.com/Documents/2014-08-27ExperimentersRulesOfthumbKDD.pdf
- **Granger, Hyung & Jeon,** «Spurious Regressions with Stationary Series». 76 % falske funn mellom uavhengige serier.
  **Høy.** https://economia.uc3m.es/jgonzalo/teaching/timeseriesMA/spuriousregressiongranger-reading.pdf
- **Barnett, van der Pols & Dobson (2005),** «Regression to the mean», *Int J Epidemiol* 34(1). **Høy.**
  https://academic.oup.com/ije/article/34/1/215/638499
- **Stanford Encyclopedia of Philosophy,** «Simpson's Paradox». **Middels–Høy.**
  https://plato.stanford.edu/entries/paradox-simpson/
- **Georgiev (2014),** Analytics-Toolkit: Simpsons paradoks i webanalyse. **Middels.**
  https://blog.analytics-toolkit.com/2014/segmenting-data-web-analytics-simpsons-paradox/
- **Wasserstein & Lazar (2016),** ASA Statement on p-Values, *The American Statistician* 70(2). **Høy.**
  https://www.stat.berkeley.edu/~aldous/Real_World/ASA_statement.pdf
- **NIST/SEMATECH e-Handbook,** Shewhart-kontrollkart. **Høy.**
  https://www.itl.nist.gov/div898/handbook/pmc/section3/pmc31.htm
- **Sadeghi m.fl. (2021),** «Novelty and Primacy», arXiv:2102.12893 (Microsoft). **Høy.**
  https://ar5iv.labs.arxiv.org/html/2102.12893

## Plattformdokumentasjon

- **Google Ads Help,** konverteringsvinduer (klikk 30 dager standard, engasjert visning 3 dager, visning 1 dag).
  **Høy.** https://support.google.com/google-ads/answer/3123169
- **Google Ads Help, «Set up Smart Bidding for a Display campaign»** – volumtabellen (under 30 konverteringer: opp til
  100 % svingning; 50 → 50 %; 100 → 20 %; 500 → under 20 %) og «minst 2 uker uten endringer». **Høy** for teksten, men
  merk at den gjelder automatiske budstrategier på Display og blander tilfeldig variasjon med systemets kalibrering.
  https://support.google.com/google-ads/answer/10285843
- **Google Ads Help, «About Target ROAS bidding»** – kravet om minst 15 konverteringer per 30 dager, og anbefalingen om
  å vurdere verdier over fire uker eller 1–2 kjøpssykluser. Inneholder **ikke** volumtabellen over. **Høy.**
  https://support.google.com/google-ads/answer/6268637
- **Google Ads Help,** Active View: «can't guarantee that a user is looking at the screen». **Høy.**
  https://support.google.com/google-ads/answer/7029393
- **Google Analytics Help,** atferds- og konverteringsmodellering ved manglende samtykke. **Høy.**
  https://support.google.com/analytics/answer/10710245
- **MRC/IAB (2014),** Viewable Ad Impression Measurement Guidelines: minst 50 % av arealet i minst 1 sekund for
  display (30 % for formater over 242 500 piksler), 2 sekunder for video. **Høy.**
  https://www.iab.com/wp-content/uploads/2015/06/MRC-Viewable-Ad-Impression-Measurement-Guideline.pdf
- **Meta:** attribusjonsinnstillinger (7 dagers klikk + 1 dags visning som standard) – **Middels**, gjengitt via
  sekundærkilde fordi Metas hjelpesider ikke er maskinlesbare. Verifiser i Meta Business Help før tall gjengis.

## Markedsføringsfag og forretningsnivå

- **Jones (1990),** «Ad Spending: Maintaining Market Share», *HBR* 68(1). **Middels.**
  https://pubmed.ncbi.nlm.nih.gov/10106403/
- **Binet & Field, IPA:** «Les and Peter: The Greatest Hits» (samler *The Long and the Short of It* 2013 og
  *Media in Focus* 2017). **Middels** – innsendte, prisbelønte case; seleksjonsskjevhet erkjent av IPA selv.
  **PDF-en lot seg ikke åpne direkte under utarbeidelsen.** Retningene fra dette materialet kan brukes; de konkrete
  prosenttallene som sirkulerer fra det skal ikke gjengis til kunde uten at noen i TRY har verifisert dem mot
  sidereferanse. https://ipa.co.uk/media/7163/les_and_peter_the_greatest_hits.pdf
- **Riebe, Wright, Stern & Sharp (2014),** «How to grow a brand: Retain or acquire customers?»,
  *Journal of Business Research* 67(5). Kundetilgang om lag dobbelt så viktig som redusert frafall. **Middels** –
  innholdet er lest via Ehrenberg-Bass' egen gjengivelse, ikke artikkelen.
  https://marketingscience.info/effective-brand-growth-acquisition-or-retention/
- **Vaughan, Corsi, Beal & Sharp (2021),** «Measuring advertising's effect on mental availability»,
  *International Journal of Market Research* 63(5). **Høy.** https://journals.sagepub.com/doi/abs/10.1177/1470785320955095
- **Romaniuk (2013),** «Modeling mental market share», *Journal of Business Research* 66(2). **Høy.**
  https://isiarticles.com/bundles/Article/pre/pdf/14452.pdf
- **Datta, Ailawadi & van Heerde (2017),** «How Well Does Consumer-Based Brand Equity Align with Sales-Based Brand
  Equity?», *Journal of Marketing* 81(3). **Høy.** https://journals.sagepub.com/doi/10.1509/jm.15.0340
- **Sethuraman, Tellis & Briesch (2011),** «How Well Does Advertising Work? Generalizations from a Meta-Analysis»,
  *JMR* 48(3). Elastisitet 0,12 / 0,24. **Høy.** https://journals.sagepub.com/doi/abs/10.1509/jmkr.48.3.457
- **Köhler, Mantrala, Albers & Kanuri (2017),** «A Meta-Analysis of Marketing Communication Carryover Effects»,
  *JMR* 54(6). 52,3 % langtidseffekt; 3,4 mnd. median varighet. **Høy.**
  https://journals.sagepub.com/doi/10.1509/jmr.13.0580
- **Bijmolt, van Heerde & Pieters (2005),** «New Empirical Generalizations on the Determinants of Price Elasticity»,
  *JMR* 42(2). Snitt −2,62. **Høy.** https://journals.sagepub.com/doi/10.1509/jmkr.42.2.141.62296
- **Ambler & Roberts (2008),** «Assessing marketing performance: don't settle for a silver metric»,
  *Journal of Marketing Management* 24(7–8). **Høy.**
  https://www.ingentaconnect.com/content/routledg/jmm/2008/00000024/f0020007/art00005
- **Locke & Latham (2002),** «Building a Practically Useful Theory of Goal Setting», *American Psychologist* 57(9).
  **Høy.** https://pubmed.ncbi.nlm.nih.gov/12237980/
- **Choi, Hecht & Tayler (2013),** «Strategy Selection, Surrogation, and Strategic Performance Measurement Systems»,
  *Journal of Accounting Research* 51(1). **Høy.** https://papers.ssrn.com/sol3/papers.cfm?abstract_id=1910383
- **Goodhart (1975) / Campbell (1979):** ordlyd verifisert via sekundærgjengivelse. **Middels.**
  https://en.wikipedia.org/wiki/Goodhart%27s_law · https://en.wikipedia.org/wiki/Campbell%27s_law
- **Skok, «SaaS Metrics 2.0»** (2013) – opphavet til «LTV/CAC = 3». **Lav** (investorblogg, ingen studie).
  https://www.forentrepreneurs.com/saas-metrics-2/
- **Flashtalking (2018),** 60+ kampanjer: CTR negativt korrelert med kreativ ytelse, gjengitt av MediaPost.
  **Middels.** https://www.mediapost.com/publications/article/326861/

## Kommunikasjon, korreksjon og tolkningsfeil

- **Lewandowsky, Cook, Ecker m.fl. (2020),** *The Debunking Handbook 2020*. Faktum–myte–mekanisme–faktum;
  alternativ forklaring må fylle hullet. **Høy** (forskerkonsensus, syntese).
  https://digitalcommons.unl.edu/context/scholcom/article/1247/viewcontent/DebunkingHandbook2020.pdf
- **van der Bles, van der Linden, Freeman & Spiegelhalter (2020),** «The effects of communicating uncertainty on
  public trust», *PNAS* 117(14). Numeriske intervaller koster nesten ingen tillit; vage ord gjør. **Høy.**
  https://research.rug.nl/en/publications/the-effects-of-communicating-uncertainty-on-public-trust-in-facts/
- **Collins & Mandel (2019),** «Cultivating credibility with probability words and numbers»,
  *Judgment and Decision Making*. **Høy.**
  https://www.cambridge.org/core/journals/judgment-and-decision-making/article/3CD3BC3EC009661BB60C22F527FC7FC8
- **Correll, Bertini & Franconeri (2020),** «Truncating the Y-Axis: Threat or Menace?», CHI. Avkuttet akse øker
  opplevd alvorlighet; varsler hjelper ikke. **Høy.** https://arxiv.org/pdf/1907.02035
- **Steyvers m.fl. (2025),** «What large language models know and what people think they know»,
  *Nature Machine Intelligence* 7. Kalibrerings- og diskrimineringsgap; lange forklaringer øker tillit uten å bedre
  skjønn. **Høy.** https://www.nature.com/articles/s42256-024-00976-7
- **Saparina & Lapata (2024),** AMBROSIA, NeurIPS. Flertydighet i naturlig språk mot data: 31 % vs. 66 % recall.
  **Høy.** https://proceedings.neurips.cc/paper_files/paper/2024/file/a4c942a8405cc910f0a833d28d2573cc-Paper-Datasets_and_Benchmarks_Track.pdf
- **Kahan, Peters, Dawson & Slovic (2017),** «Motivated Numeracy and Enlightened Self-Government»,
  *Behavioural Public Policy*. Høy tallforståelse forsterker motivert resonnering. **Høy.**
  https://rcgd.isr.umich.edu/wp-content/uploads/2018/07/motivated_numeracy_and_enlightened_selfgovernment.pdf
- **Cain, Loewenstein & Moore (2005),** «The Dirt on Coming Clean», *Journal of Legal Studies* 34(1). Å opplyse om
  interessekonflikt er ikke nok. **Høy** (lest som sammendrag).
  https://papers.ssrn.com/sol3/papers.cfm?abstract_id=480121
- **Hjelle, Mikalef, Altwaijry & Parida (2024),** dashboard-format og beslutningskvalitet, *Information & Management*
  61(6). **Høy** (lest som sammendrag). https://osuva.uwasa.fi/items/76b8c883-a991-4901-8cac-82ac65eb3f3b
- **Ries (2009),** «Vanity metrics vs. actionable metrics». **Middels** som begrepskilde, **Lav** som evidens.
  https://tim.blog/2009/05/19/vanity-metrics-vs-actionable-metrics/

## Kanalnivå: diagnostikk, kreativ, frekvens, oppmerksomhet, levering

- **Vakratsas & Ambler (1999),** «How Advertising Works: What Do We Really Know?», *Journal of Marketing* 63(1).
  Gjennomgang av over 250 arbeider; lite belegg for at effekter følger en fast rekkefølge i tid. **Høy.**
  https://journals.sagepub.com/doi/10.1177/002224299906300103
- **Schmidt & Eisend (2015),** «Advertising Repetition: A Meta-Analysis», *Journal of Advertising* 44(4). 37 studier,
  312 effektstørrelser; omvendt U for holdning med maksimum rundt ti eksponeringer, mer lineær erindring, forvitring
  over tid. **Høy.** https://www.tandfonline.com/doi/abs/10.1080/00913367.2015.1018460
- **Chae, Bruno & Feinberg (2019),** «Wearout or Weariness?», *Journal of Marketing Research* 56(1). Over 12 000
  brukere, over 400 nettsteder; ca. 24 % viste ekte weariness, profilbasert frekvenstak ga ca. 15 % bedre effekt.
  **Høy.** https://journals.sagepub.com/doi/abs/10.1177/0022243718820587
- **Ali, Sapiezynski, Bogen, Korolova, Mislove & Rieke (2019),** «Discrimination through Optimization», *PACM HCI
  (CSCW)*. Leveringsskjevhet uavhengig av annonsørens målretting; både budsjett og annonseinnhold bidrar. **Høy.**
  https://arxiv.org/abs/1904.02095
- **Google Ads Hjelp,** dagsbudsjett og overforbruk (opptil 2× dagsbudsjett på én dag, 30,4× per måned). **Høy.**
  https://support.google.com/google-ads/answer/6385083 · https://support.google.com/google-ads/answer/2375420
- **Google Ads Hjelp,** læringsstatus: opptil tre uker eller 1–2 kjøpssykluser, nullstilles ved endring. **Høy.**
  https://support.google.com/google-ads/answer/13020501
- **TikTok Ads Hjelp,** læringsfase: volatiliteten avtar etter ca. 25 resultater eller sju dager. **Høy.**
  https://ads.tiktok.com/help/article/learning-phase
- **Deloitte/Google (2020),** «Milliseconds Make Millions». 37 merkevarer, fire uker; 0,1 sek raskere mobilside gav
  +8,4 % konverteringsrate i handel, −1,9 % i leadsgenerering. **Middels** – forfatternes eget forbehold om
  representativitet. https://www.thinkwithgoogle.com/_qs/documents/9757/Milliseconds_Make_Millions_report_hQYAbZJ.pdf
- **Follett / Lumen (2021),** «The true cost of advertising attention», WARC. Oppmerksomhet vs. synlighet per format;
  oppmerksomhetsjustert CPM. **Middels** – forfatteren forbeholder metoden selv.
  https://srh.agency/assets/documents/The-true-cost-of-advertising-attention-_-WARC.pdf
- **Nelson-Field (2022),** «State of Attention», Screenforce NL. Lyd av/på fra 82 % til 5 %; oppmerksomhet 6,1 til
  2,7 sekunder. **Middels** – plattformene anonymisert, utvalgsstørrelse ikke oppgitt.
  https://screenforce.nl/wp-content/uploads/2022/05/Nelson-Field-State-of-Attention-for-Screenforce-NL.pdf
- **Teads x Lumen (2023),** IAB Europe. 40 % høyere erindringsløft ved 5+ sek enn 1+ sek, 16 kampanjer. **Middels.**
  https://iabeurope.eu/wp-content/uploads/2023/07/Teads-x-Lumen-Attention-Whitepaper.pdf
- **Dentsu (2021),** Attention Economy Phase 2. 17 % forskjell i erindring mellom sterk og svak kreativ; metode oppgitt
  (Lumen, TVision, Amplified Intelligence). **Middels.**
  https://assets-eu-01.kc-usercontent.com/27bd3334-62dd-01a3-d049-720ae980f906/887ba048-d8e4-4b28-9836-9b0ce45fa9e4/dentsu%20Attention%20Economy%20Phase%202%202021.pdf
- **Kantar (2024),** «How attention impacts media and creative effectiveness». 873 kampanjer, 3,2 mrd. USD;
  oppmerksomhet per visning korrelerte **ikke** med kostnadseffektivitet. **Middels/Lav** – motvekt til kildene over.
  https://www.kantar.com/inspiration/advertising-media/how-attention-impacts-media-and-creative-effectiveness
- **Kantar (2023),** «The art of proof». Ca. 450 annonser mot WARCs ROI-database; kreativt sterke annonser gav over
  fire ganger profitt. **Middels/Lav.**
  https://www.kantar.com/uki/inspiration/advertising-media/the-art-of-proof-how-creative-quality-drives-profit
- **NCSolutions, «Five Keys to Advertising Effectiveness» (2023)** og **IAB Australia (2018)** – opphavet til «kreativ
  forklarer 47/49 %». **Middels for eksistensen av tallet, ikke brukbart som funn:** metoden er ikke publisert,
  andelene flytter seg mellom utgaver, populasjonen er amerikansk dagligvare og korttidssalg.
  https://info.ncsolutions.com/hubfs/2023%20Five%20Keys%20to%20Advertising%20Effectiveness/NCS_Five_Keys_to_Advertising_Effectiveness_E-Book_08-23.pdf
  · https://iabaustralia.com.au/wp-content/uploads/2018/07/Role-of-Creative-in-Digital-Ad-Effectiveness.pdf
- **comScore/Pretarget,** 263 mill. displayvisninger: korrelasjon klikk–konvertering 0,01, hover 0,49. **Middels** –
  sekundærgjengivelse, primærrapport ikke funnet.
  https://martech.org/study-for-display-ads-clicks-have-nearly-zero-correlation-with-conversion/

## Norske forhold

- **Mediebyråforeningen (23.01.2026):** medieomsetning via norske mediebyråer 10,19 mrd. kr i 2025, +3,4 %.
  **Middels–Høy** (dekker kun byråformidlet omsetning).
  https://mediebyraaforeningen.no/medieomsetningen-over-10-milliarder-kroner-i-2025/
- **SSB, Norsk mediebarometer 2025** (publ. 12.05.2026, n=3 012): 82 % bruker sosiale medier daglig, 61 % leser
  nettaviser daglig. **Høy.** https://www.ssb.no/kultur-og-fritid/tids-og-mediebruk/artikler/norsk-mediebarometer-2025
- **ANFO Effektprosjektet:** ca. 1 300 case over 12 år. Detaljerte funn er forbeholdt ANFO-medlemmer og **ikke** åpent
  tilgjengelige – oppgi derfor ingen tall fra prosjektet. **Middels** for datagrunnlaget.
  https://anfo.no/2025/06/23/markedsforing-som-virker/

## Kjente kildehull – ikke fyll dem med tall

1. **ESOV-koeffisienten** («ca. 0,5 prosentpoeng markedsandel per 10 ESOV-poeng») – ingen åpen primærkilde funnet.
2. **Metas læringsfase** (50 hendelser per 7 dager) – kun sekundærkilder.
3. **Dobbelttelling på tvers av plattformer** – mekanismen er sikker, omfanget er ikke tallfestet i forskning.
4. **Engasjementsrate mot salg** – ingen fagfellevurdert kobling funnet.
5. **Rapporteringsfrekvens** – ingen studie tester direkte hvor ofte man bør evaluere markedsføring.
6. **CEP-mål som prediktor for framtidig vekst** – ingen åpen fagfellevurdert studie funnet.
7. **Norske inkrementalitets- eller geo-lift-studier** – ingen åpent publisert. Norske eksempler må komme fra TRYs egne.
8. **60/40-fordelingen** for en enkelt kategori eller et enkelt marked – IPA sier selv at forholdet varierer og at
   datasettet har seleksjonsskjevhet. Ikke presenter det som en regel for denne kunden.
9. **IPA-ens enkelttall** (57 merker, −16 %/−25 %, 22 % mot 7 %, 2,0 → 1,3) – ikke verifisert mot sidereferanse.
   Bruk retningen, ikke tallet.
10. **Støybåndene ±2/√C og ±2,8/√C** – utregnet fra tellestatistikk, ikke hentet fra en publisert kilde. Oppgi som
    tommelfingerregel.
11. **«Attribuerte konverteringsdata kan oppdateres i opptil 12 dager»** – gjengitt fra Googles hjelpesider, ikke
    verifisert på nytt. Bruk «i dagene etter» hvis du er i tvil.
12. **Simonovs 18 %** – gjelder ett eksempel i studien, ikke et snitt. Ikke generaliser.
13. **Benchmarks for CTR, CPM, VTR og konverteringsrate** – ingen etterrettelig norsk eller nordisk kilde funnet.
    Oppgi ingen. Svar mot kundens egen historikk.
14. **«Kreativ forklarer 47 %»** – ikke etterprøvbart (metode ikke publisert, tallene flytter seg mellom utgaver:
    kreativ 47 → 49 %, rekkevidde 22 → 14 %). Si «mest», ikke en prosentandel.
15. **Diagnosetegn på kreativ utmattelse i annonsekontoen** – bransjepraksis. Kurveformen og weariness er dokumentert.
16. **Målgruppeoverlapp som auksjonsmekanikk** («du byr mot deg selv») – ingen primærkilde funnet, kun
    leverandørblogger. Omtal som usikkerhet.
17. **Den diagnostiske trappen** som modell for kundeatferd – ikke dokumentert, og kritisert som kausalmodell.
    Bruk den som leteverktøy.
