---
name: mg-dataviz
description: Use this skill whenever creating data visualizations, charts, graphs, dashboards, or data-driven slides for Mestergruppen. This includes bar charts, line charts, donut charts, scorecards, heatmaps, scatter plots, waterfall charts, and any other visual representation of data. Triggers include requests to visualize data, create dashboards, build reporting artifacts, make chart components, or produce data slides in PowerPoint. Apply this skill alongside the mg-brand skill when creating slides. This skill governs data visualization structure, chart selection, labeling, and the Mestergruppen visualization color palette. Do NOT use for non-data visuals like illustrations, photography, or brand assets.
---

# Mestergruppen Data Visualization Skill

Denne skillen sikrer at alle datavisualiseringer for Mestergruppen følger best practice for klarhet, tilgjengelighet og merkevarekonsistens. Den bygger på Mestergruppens visuelle identitet med en fargepalett tilpasset datavisualisering.

**Les alltid `mg-brand` SKILL.md ved presentasjoner** for typografi (Aptos Display / Aptos Regular), layout og logobruk.

## Default Output Format

| Bruksområde | Default output | Merknader |
|---|---|---|
| Dashboard / interaktiv rapport | React/HTML artifact | Recharts foretrukket. Umiddelbart visbart. |
| Klientpresentasjon | PowerPoint (.pptx) | Bruk med `mg-brand` skill |
| Datatabell / regneark | Excel (.xlsx) | |
| Statisk diagram | Python → PNG/SVG | matplotlib med MG-tema |
| Skriftlig rapport med diagrammer | Word (.docx) + innebygde diagrammer | |

**Power BI er opt-in.** Produser ikke Power BI-output med mindre brukeren eksplisitt ber om det.

---

## Kjerneprinsipper

1. **Ett budskap per diagram.** Hver visualisering formidler én klar innsikt. Flere historier → flere diagrammer.
2. **Data-ink ratio.** Fjern alt som ikke kommuniserer data: 3D-effekter, dekorative skygger, bakgrunnsbilder, overdrevne rutenettlinjer, diagramrammer.
3. **Hierarki: kontekst → data → detaljer.** Bygg hver visualisering i tre lag: deklarativ tittel → diagrammet → kilde og metadata.
4. **WCAG AA.** Ikke-tekstelementer: ≥3:1 kontrast. Tekst: ≥4.5:1 (≥3:1 for stor tekst). Aldri stol på farge alene – legg alltid til form (▲/▼), mønster eller direkte merkelapper.
5. **Norsk som standard.** Bruk norsk tallformatering, datokonvensjoner og etiketter med mindre innholdet er for et internasjonalt publikum eller brukeren spesifiserer engelsk.

---

## Lokalisering

### Norsk formatering (standard)

| Element | Format | Eksempel |
|---|---|---|
| Tusenskilletegn | Mellomrom (thin space U+202F) | 1 234 567 |
| Desimalskilletegn | Komma | 1 234,5 |
| Valuta (NOK) | «kr» foran eller «NOK» etter | kr 1 234 / 1 234 NOK |
| Valuta (stor) | Forkortet | 1,2 mrd. kr / 45,3 mill. kr |
| Prosent | Kommadesimal | 12,3 % |
| Endring (%) | Fortegn + komma | +12,3 % / −5,1 % |
| Dato | DD.MM.YYYY | 19.02.2026 |
| Månedsnavn | Norsk | jan, feb, mar, apr, mai, jun, jul, aug, sep, okt, nov, des |
| Akseforkortelser | t (tusen), mill., mrd. | 45 t / 1,2 mill. |

### Engelsk formatering (internasjonale klienter)

| Element | Format | Eksempel |
|---|---|---|
| Tusenskilletegn | Komma | 1,234,567 |
| Desimalskilletegn | Punktum | 1,234.5 |
| Valuta | NOK-prefiks eller lokal | NOK 1,234 / €1,234 |
| Forkortelser | K, M, B | 45K / 1.2M |

**Regel:** Hvis diagramtittel, etiketter og kildetekst er på norsk, bruk norsk tallformatering. Hvis på engelsk, bruk engelsk. Aldri bland konvensjoner i ett diagram.

---

## Fargesystem

### Kategorisk palett (bruk i denne rekkefølgen)

| Rang | Navn | Hex | Bruk |
|---|---|---|---|
| 1 | Mestergruppen Blå | `#0003BD` | Viktigste serie – signaturfargen leder alltid |
| 2 | Rødbrun Glød | `#AF4D47` | Sekundær serie – varm kontrast til blå |
| 3 | Skinnbrun | `#A86F52` | Tredje serie |
| 4 | Burgunder | `#641A2F` | Fjerde serie |
| 5 | Skoggrønn | `#24392C` | Femte serie |
| 6 | Støvet Terracotta | `#BC6B5B` | Sjette serie |
| 7 | Marineblå | `#000066` | Syvende serie (sjelden brukt) |
| 8 | Mørk Nøytral | `#6B6B6B` | «Andre» / gruppert rest |

**Regler:**
- Maks 6 kategorier per diagram. Grupper resten i «Andre» (Mørk Nøytral).
- Mestergruppen Blå er alltid den viktigste serien – la signaturfargen lede.
- Hold farge-til-kategori-kobling konsistent på tvers av alle diagrammer i en rapport/presentasjon.
- For 2 serier: rang 1+2. For 3: rang 1+2+3. Og så videre.

```python
# Kategorisk palett – Python
MG_CATEGORICAL = [
    "#0003BD",  # Mestergruppen Blå
    "#AF4D47",  # Rødbrun Glød
    "#A86F52",  # Skinnbrun
    "#641A2F",  # Burgunder
    "#24392C",  # Skoggrønn
    "#BC6B5B",  # Støvet Terracotta
    "#000066",  # Marineblå
    "#6B6B6B",  # Mørk Nøytral
]
```

```javascript
// Kategorisk palett – JavaScript / Recharts
const MG_CATEGORICAL = [
  "#0003BD", // Mestergruppen Blå
  "#AF4D47", // Rødbrun Glød
  "#A86F52", // Skinnbrun
  "#641A2F", // Burgunder
  "#24392C", // Skoggrønn
  "#BC6B5B", // Støvet Terracotta
  "#000066", // Marineblå
  "#6B6B6B", // Mørk Nøytral
];
```

### Sekvensiell palett (lav → høy)

5-trinns blå rampe for heatmaps og intensitet:

| Trinn | Hex | Bruk |
|---|---|---|
| 1 (lysest) | `#E6EEF9` | Laveste verdi |
| 2 | `#B3C7E8` | |
| 3 | `#6680D0` | Midtverdi |
| 4 | `#0003BD` | |
| 5 (mørkest) | `#000066` | Høyeste verdi |

```python
MG_SEQUENTIAL = ["#E6EEF9", "#B3C7E8", "#6680D0", "#0003BD", "#000066"]
```

### Divergerende palett (negativ ← nøytral → positiv)

Rødbrun ← Nøytral → Blå. Bruk for avvik fra referanseverdi.

| Verdi | Hex |
|---|---|
| Sterkt negativ | `#AF4D47` |
| Svakt negativ | `#D2A98B` |
| Nøytral | `#F6F6F6` |
| Svakt positiv | `#B3C7E8` |
| Sterkt positiv | `#0003BD` |

```python
MG_DIVERGING = ["#AF4D47", "#D2A98B", "#F6F6F6", "#B3C7E8", "#0003BD"]
```

### Highlight-palett (fokus + dempet)

| Rolle | Hex | Navn |
|---|---|---|
| Fokus | `#0003BD` | Mestergruppen Blå |
| Dempet | `#D9D9D9` | Lys Nøytral |

Bruk Mestergruppen Blå for nøkkelserien, dempet grå for alt annet.

### Semantisk palett (fast betydning)

| Betydning | Hex | Navn | Symbol |
|---|---|---|---|
| Positiv | `#24392C` | Skoggrønn | ▲ |
| Negativ | `#AF4D47` | Rødbrun Glød | ▼ |

**Alltid kombiner med ▲/▼** – aldri stol på farge alene.

### Fossefallsdiagram (waterfall)

| Rolle | Hex | Navn |
|---|---|---|
| Positiv | `#24392C` | Skoggrønn |
| Negativ | `#AF4D47` | Rødbrun Glød |
| Total / subtotal | `#0003BD` | Mestergruppen Blå |
| Startverdi | `#6B6B6B` | Mørk Nøytral |

### Nøytrale farger (bakgrunn, rutenett, metadata)

| Rolle | Hex | Navn |
|---|---|---|
| Sidebakgrunn | `#F6F6F6` | Base Nøytral |
| Diagrambakgrunn | `#FFFFFF` | Hvit |
| Dempet element / forrige periode | `#D9D9D9` | Lys Nøytral |
| Rutenettlinjer | `#D9D9D9` | Lys Nøytral (stiplet) |
| Akselinjer | `#6B6B6B` | Mørk Nøytral (tynn) |
| Kildetekst / metadata | `#6B6B6B` | Mørk Nøytral |
| Skeleton / loading | `#F6F6F6` → `#D9D9D9` | Pulserende |

---

## Diagramvalg

### Hurtigguide

| Mål | Bruk | Unngå |
|---|---|---|
| Trend over tid | Linjediagram | Kakediagram, stolper med >8 perioder |
| Sammenligne kategorier | Horisontalt stolpediagram (sortert) | Kakediagram, 3D-stolper |
| Del av helhet | Donut (maks 5 segmenter) | Kakediagram med >6 segmenter |
| Rangering | Horisontalt stolpediagram (sortert etter verdi) | Usorterte stolper |
| Korrelasjon | Punktdiagram | Dobbel y-akse |
| KPI / enkelttall | Scorecard (stort tall) | Diagram der ett tall holder |
| Dekomponering / bro | Fossefallsdiagram | Stablet stolpediagram |
| Volum + rate sammen | Side-ved-side-paneler eller indeksert | Dobbel y-akse |
| Periodesammenligning (ÅoÅ, MoM) | Linje: hel (nåværende) + stiplet (forrige) | Overlappende stolper |
| Avvik fra mål | Bullet chart / avviksstolpe | Kakediagram |

### Alltid unngå
- 3D-effekter, dobbel y-akse, kakediagrammer (bruk donut), avkuttet y-akse på stolper, bakgrunnsbilder bak diagrammer, tunge rutenettlinjer

---

## Sammenligningsoppsett

### Periode-over-periode (ÅoÅ, QoQ, MoM)

- **Linjediagrammer:** Nåværende periode = hel linje i Mestergruppen Blå (2–3px). Forrige periode = stiplet linje i `#D9D9D9` (1.5px). Merk begge endepunkter direkte.
- **Stolpediagrammer:** Nåværende periode = Mestergruppen Blå. Forrige periode = `#D9D9D9` (side-ved-side, ikke overlappende).
- **Tabeller:** Vis absolutt verdi, endring (Δ) og endringsprosent (Δ%). Bruk semantiske farger + ▲/▼ for endringskolonnene.
- **KPI-kort:** Hovednummer = nåværende periode. Under: «vs. forrige periode» med Δ% og pil.

### Versus mål / benchmark

- **Bullet chart:** Grå stolpe = faktisk, tynn markør = mål. Best for enkeltmetrikk.
- **Avviksstolpe:** Horisontale stolper som viser +/− avvik fra mål. Skoggrønn høyre, Rødbrun venstre.
- **Referanselinje:** Stiplet `#6B6B6B` linje merket «Mål: 100K» på stolpe- eller linjediagram.

### Indeksering (base = 100)

- Bruk når du sammenligner serier med ulike enheter eller skalaer.
- Merk alltid basisperioden tydelig: «Indeks, jan 2025 = 100».
- Mestergruppen Blå for primærserien, kategorisk palett for resten.

---

## Tekst og merkelapper

**Deklarative titler** – Oppsummer innsikten, ikke beskriv diagrammet:
- ❌ «Kostnad per lead over tid»
- ✅ «Kostnad per lead falt 23 % etter kampanjejustering»

**Direkte merking** – Merk dataserier direkte på diagrammet. Bruk forklaring (legend) kun når direkte merking gir overlapp. Plasser forklaringer over eller til høyre – aldri under.

**Akser** – Merk begge akser med enheter. Bruk forkortelser: t, mill., mrd. (norsk) eller K, M, B (engelsk). Rutenettlinjer: lett stiplet `#D9D9D9` eller ingen. Akselinjer: tynn `#6B6B6B`.

**Kilde** – Hvert diagram må vise kilde og tidsperiode nederst i `#6B6B6B`. Format: «Kilde: [kilde] | Periode: [periode]».

**Annoteringer** – Legg til korte notater direkte på diagrammet for anomalier eller vendepunkter. Tekst i `#6B6B6B`, koblet til data med en tynn `#D9D9D9` linje. Maks 2–3 per diagram.

### Typografi i diagrammer

| Element | Font | Størrelse |
|---|---|---|
| Diagramtittel (i presentasjon) | Aptos Display | 28–32pt |
| Diagramtittel (i dashboard) | System / sans-serif | 16–20px |
| Aksetiketter | Aptos Regular / sans-serif | 10–12pt |
| Direkte merkelapper | Aptos Regular / sans-serif | 10–12pt |
| Kildetekst | Aptos Regular / sans-serif | 9–10pt |

**Aldri bruk bold (`bold: true`)** – følg Mestergruppens typografiregel. Bruk Aptos Display for vekt/hierarki.

---

## Målgruppetipassning

| Publikum | Fokus | Detalj | Maks diagrammer/visning |
|---|---|---|---|
| Ledelse / styre | KPIer, trender | Overordnet | 1–2 |
| Klienter | Resultater, ROI | Middels | 2–3 |
| Interne team | Drill-down, detalj | Høy | 3–4 |

---

## Datafortelling

Følg denne buen når du bygger en serie visualiseringer:
1. **Kontekst** – Hva er situasjonen? (Scorecard)
2. **Komplikasjon** – Hva endret seg? (Trend + annotering)
3. **Innsikt** – Hva forklarer det? (Sammenligning, nedbrytning)
4. **Handling** – Hva bør vi gjøre? (Anbefaling)

Bruk **highlight-paletten** for å styre oppmerksomhet: Mestergruppen Blå på nøkkelserien, grå på resten. Gi alltid kontekst for tall (vs. forrige periode, vs. benchmark, vs. mål).

---

## Tomme, lastende og feiltilstander

For interaktive dashboards og React-artefakter:

| Tilstand | Behandling |
|---|---|
| **Laster** | Skeleton-plassholdere som matcher diagramdimensjoner. Pulserende animasjon i `#F6F6F6` → `#D9D9D9`. Aldri vis spinner alene. |
| **Tom / ingen data** | Grått ikon (diagramomriss) + tekst: «Ingen data for valgt periode». Sentrert i diagramområdet. `#6B6B6B` tekst. |
| **Feil** | Rødbrun ikon (`#AF4D47`) + tekst: «Kunne ikke laste data. Prøv igjen.» Valgfri retry-knapp i `#6B6B6B`. |
| **Delvis data** | Vis tilgjengelig data med annotering: «Data ufullstendig for [periode]». Stiplet linje/stolpemønster for ufullstendige segmenter. |

---

## Tilgjengelighet

Utover fargekontrast (WCAG AA):

- **Alt-tekst:** Hvert diagrambilde (PNG, PPTX) må ha beskrivende alt-tekst som oppsummerer innsikten, ikke diagramtypen. Eksempel: `alt="Omsetning økte 50 % år-over-år fra 130K til 195K NOK"`, ikke `alt="Linjediagram"`.
- **Aria-etiketter:** Interaktive React-diagrammer trenger `aria-label` på diagramcontaineren og `role="img"` eller `role="figure"`.
- **Tastaturnavigasjon:** Tooltips i React-dashboards må være tilgjengelige via tastatur (Tab / Enter).
- **Skjermleserrekkefølge:** DOM-rekkefølge i dashboards bør følge datafortellingsbuen: KPIer først, deretter detaljdiagrammer, deretter kilde/metadata.
- **Form + farge:** Aldri stol på farge alene. Positiv/negativ får alltid ▲/▼. Kategorier i linjediagrammer får distinkte stiplingsmønstre ved gråtoneprint.

---

## Print og PDF-eksport

- **Fargesikkerhet:** Test alle diagrammer i gråtoner. Den kategoriske paletten har distinkte lyshetsaverdier, men legg til stiplingsmønstre på linjediagrammer og direkte merkelapper på stolper for sikkerhet.
- **Sideformat:** A4 portrett for rapporter, A4 landskap for dashboard-eksporter.
- **Marginer:** Min 20mm alle sider.
- **Oppløsning:** 150 DPI minimum for innebygde diagrambilder, 300 DPI for trykk.
- **Fontinnbygging:** Sørg for at fonter er innebygd i PDF. Bruk Aptos eller fall tilbake til Helvetica/Arial.
- **Bakgrunn:** Bruk `#FFFFFF` for print (ikke `#F6F6F6`).

---

## Formatspesifikke retningslinjer

### React / HTML (standard for dashboards)

- Biblioteker: Recharts (foretrukket), D3.js, Chart.js
- Tooltip: Mestergruppen Blå bg `#0003BD`, hvit tekst, 4px border-radius
- Hover: 80% opacity på ikke-hovrede elementer
- Dashboard: KPI-scorecards øverst, detaljdiagrammer i 2–3 kolonner under

```javascript
// Recharts tooltip-styling
const MG_TOOLTIP_STYLE = {
  backgroundColor: "#0003BD",
  color: "#FFFFFF",
  borderRadius: "4px",
  border: "none",
  padding: "8px 12px",
  fontSize: "12px",
};
```

### PowerPoint (.pptx)

- Tittel: 28–32pt Aptos Display, Mestergruppen Blå (`#0003BD`) på lys bakgrunn, hvit på mørk
- Diagrammet fyller ~70 % av slidehøyden
- Kilde: nederst til venstre, 9–10pt Aptos Regular, `#6B6B6B`
- Kun solid fill – ingen gradienter i stolper
- Følg `mg-brand` skill for layout, logo og rutenett

### Excel (.xlsx)

- Fjern standard Excel-rutenettlinjer og rammer
- Header-rad: Mestergruppen Blå bakgrunn, hvit tekst
- Alternerende rader: `#F6F6F6`
- Betinget formatering: bruk sekvensiell palett for heatmaps, semantiske farger + ▲/▼ for pos/neg

```python
# openpyxl header-styling
from openpyxl.styles import Font, PatternFill

MG_HEADER_FONT = Font(name="Aptos Regular", color="FFFFFF", size=11)
MG_HEADER_FILL = PatternFill(start_color="0003BD", end_color="0003BD", fill_type="solid")
MG_ALT_ROW_FILL = PatternFill(start_color="F6F6F6", end_color="F6F6F6", fill_type="solid")
```

### Python / Matplotlib

```python
import matplotlib.pyplot as plt
from matplotlib.colors import LinearSegmentedColormap

def apply_mg_theme(ax):
    """Appliser Mestergruppen-tema på matplotlib-akser."""
    ax.set_facecolor("#FFFFFF")
    ax.figure.set_facecolor("#F6F6F6")
    ax.spines["top"].set_visible(False)
    ax.spines["right"].set_visible(False)
    ax.spines["left"].set_color("#6B6B6B")
    ax.spines["bottom"].set_color("#6B6B6B")
    ax.tick_params(colors="#6B6B6B", labelsize=10)
    ax.grid(axis="y", color="#D9D9D9", linestyle="--", linewidth=0.5)
    ax.set_axisbelow(True)

def clean_axes(ax):
    """Fjern unødvendige visuelle elementer."""
    ax.spines["top"].set_visible(False)
    ax.spines["right"].set_visible(False)

# Sekvensiell colormap for heatmaps
MG_CMAP = LinearSegmentedColormap.from_list(
    "mg_blue", ["#E6EEF9", "#B3C7E8", "#6680D0", "#0003BD", "#000066"]
)
```

### Dark Mode (React/HTML)

- Bakgrunn: `#1A1A2E` eller `#000066` (Marineblå)
- Tekst: `#FFFFFF`
- Rutenettlinjer: `#333366` (stiplet)
- Mestergruppen Blå fungerer på både lys og mørk bakgrunn
- Juster lyse palettfarger (Karamellbeige, Kremhvit) opp i metning for mørke bakgrunner

---

## Vanlige feil

| Feil | Løsning |
|---|---|
| Kakediagram | Bruk donut (maks 5) eller horisontalt stolpediagram |
| Y-akse ikke ved 0 (stolper) | Start alltid stolper ved 0 |
| For mange farger (>6) | Grupper i «Andre» |
| Generisk tittel | Skriv deklarativt: oppgi hovedfunnet |
| Kun rød/grønn | Legg til ▲/▼ eller mønstre i tillegg til farge |
| Ingen kilde | Vis alltid kilde + periode nederst |
| Engelsk tallformat i norsk kontekst | Bruk mellomrom + komma (1 234,5) |
| Dobbel y-akse | To separate paneler eller indekser til 100 |
| Bold/italic i tekst | Aldri – bruk Aptos Display for hierarki |
| Sort tekst på mørk bakgrunn | Alltid hvit tekst på MG Blå, Marineblå, Burgunder, Skoggrønn |

---

## Sjekkliste før levering

- [ ] Deklarativ tittel som oppsummerer innsikten
- [ ] Riktig diagramtype for data og budskap
- [ ] Y-akse starter ved 0 for stolpediagrammer
- [ ] Farger i korrekt kategorisk rekkefølge
- [ ] Fargetildeling konsistent på tvers av alle diagrammer
- [ ] Direkte merking brukt der mulig
- [ ] Akser merket med enheter
- [ ] Rutenettlinjer minimale eller fjernet
- [ ] Kilde og tidsperiode synlig
- [ ] WCAG AA: ≥3:1 ikke-tekst, ≥4.5:1 tekst
- [ ] Diagram fungerer uten farge (form/merkelapp-backup)
- [ ] Ingen dekorative elementer (3D, skygger, rammer)
- [ ] Maks 6 kategorier (resten gruppert som «Andre»)
- [ ] Ett klart budskap per diagram
- [ ] Tallformatering matcher språkkontekst (NO/EN)
- [ ] Tomme/lastende/feiltilstander håndtert (interaktive artefakter)
- [ ] Alt-tekst oppgitt for diagrambilder
- [ ] Sammenligningskontekst til stede (vs. periode, vs. mål, vs. benchmark)
- [ ] Ingen bold/italic – Aptos Display for vekt
- [ ] Riktig tekstfarge for bakgrunn (hvit på mørk, sort på lys)
