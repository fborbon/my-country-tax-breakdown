# My Country Tax Breakdown

**Live site: [https://fborbon.github.io/where-do-my-taxes-go](https://fborbon.github.io/where-do-my-taxes-go)**

An interactive, single-page dashboard that shows how Spain's consolidated general government spends public money — broken down into 11 COFOG spending categories across fiscal years 2021, 2022, and 2023. The tool helps citizens see where their taxes go, compare Spain's spending mix against the EU-27 average as a share of GDP, and explore year-on-year budget evolution — all sourced from official IGAE and Eurostat data with no backend, no build step, and no installation required.

**Main technologies:** Vanilla HTML · CSS · JavaScript · Chart.js 4 (CDN) · GitHub Pages

**Monthly cost:** $0. The site is a single static HTML file. Hosting is provided free by GitHub Pages. There are no servers, no databases, and no runtime dependencies to pay for.

---

## Table of Contents

1. [Live Demo](#live-demo)
2. [Features](#features)
3. [Data Sources](#data-sources)
4. [Spending Categories (COFOG)](#spending-categories-cofog)
5. [Tech Stack](#tech-stack)
6. [License](#license)

---

## Live demo

Visit **[https://fborbon.github.io/where-do-my-taxes-go](https://fborbon.github.io/where-do-my-taxes-go)** or open `index.html` directly in any browser — no server or build step required.

## Features

- **Year selector** — switch between 2021, 2022 and 2023 data with animated chart transitions
- **Donut chart** — proportional breakdown of all 10 spending categories; click any slice for a detailed sub-item breakdown
- **Horizontal bar chart** — categories ranked by absolute spending (€ billion)
- **EU-27 comparison chart** — Spain vs EU-27 average expressed as % of GDP for a fair cross-country comparison
- **Summary cards** — total spending, % of GDP, per-capita figure, and year-on-year delta
- **Official source links** — every figure is attributed to a primary source

## Data sources

All figures are approximate, rounded to the nearest €1 billion, and represent **consolidated general government expenditure** (Estado + Comunidades Autónomas + Entidades Locales + Seguridad Social). Intra-governmental transfers are netted out.

| Source | Used for |
|--------|----------|
| [IGAE — Intervención General de la Administración del Estado](https://www.igae.pap.hacienda.gob.es) | Spain consolidated accounts, COFOG classification |
| [Ministerio de Hacienda — Presupuestos Generales del Estado](https://www.hacienda.gob.es) | Central government budget detail |
| [Eurostat — Government Finance Statistics](https://ec.europa.eu/eurostat/web/government-finance-statistics/data/database) | Spain & EU-27 average spending by COFOG function |
| [Portal de Transparencia](https://transparencia.gob.es) | Budget execution and investment breakdown |
| [AIReF](https://www.airef.es) | Independent fiscal analysis |
| [Seguridad Social](https://www.seg-social.es) | Pension, unemployment and social benefit detail |

## Spending categories (COFOG)

Pensions are shown as a **separate category** (split from Social Protection) because they alone account for ~29% of all public spending — the largest single budget item by far.

1. **Pensions** — old-age (jubilación), widow/widower, disability pensions, Clases Pasivas (~29% of total)
2. Other Social Protection — unemployment, sick-leave pay, family benefits, Ingreso Mínimo Vital
3. Health — hospitals, primary care, pharmaceuticals
4. Education — pre-school through university
5. General Public Services — administration, judiciary, debt interest
6. Economic Affairs — infrastructure, agriculture (CAP), energy, R&D
7. Public Order & Safety — police, civil guard, prisons, emergency services
8. Housing & Community — social housing, water, sanitation
9. Defense — armed forces, NATO contributions
10. Environmental Protection — waste, water treatment, climate policy
11. Recreation, Culture & Religion — museums, sports, broadcasting

## Tech stack

Plain HTML + CSS + JavaScript. Charts rendered with [Chart.js 4](https://www.chartjs.org/) (CDN). No framework, no build tooling, no dependencies to install.

## License

MIT

---

## Auditing

This section provides a structured checklist for review by an IT expert and a public-finance / civic-data subject-matter expert.

### Audit Items

- **Cost & resource minimization** — The project costs $0. A single static HTML file is hosted on GitHub Pages for free. No servers, databases, or runtime dependencies exist.
- **IT architecture** — Single-file, no-build static site. Minimalist and appropriate for a civic data visualization that does not require real-time data or user interaction beyond chart navigation. Zero infrastructure to maintain.
- **Code efficiency** — All spending data is hardcoded in JavaScript arrays. Chart.js is loaded from a CDN. There is no build step, which eliminates toolchain maintenance entirely. Adding future years means manual updates to the data arrays.
- **Cybersecurity** — No backend, no user data, no cookies, and no user authentication. The only external dependency is the Chart.js CDN; a compromised CDN could inject malicious scripts (supply-chain risk). Hosting the Chart.js bundle locally would eliminate this vector.
- **Readability & maintainability** — A single HTML file is easy to audit and modify for small datasets. As data years accumulate, the file will grow and may benefit from splitting data into a separate JSON file.
- **AI / ML** — No AI or ML is used, which is appropriate for a deterministic data visualization.
- **Data accuracy & freshness** — Values are rounded to the nearest €1B. Only 2021–2023 data is available. There is no automated mechanism to refresh figures when IGAE or Eurostat publishes new data. The EU-27 comparison relies on Eurostat definitions that may change.
- **Other** — Mobile responsiveness and cross-browser compatibility are not documented. The COFOG classification and data sources are cited, which is good practice for civic transparency.

### Summary Table

| Audit Item | Claude's Assessment | Human Expert Assessment |
|---|---|---|
| Cost & resource minimization | $0/month. GitHub Pages hosting at no cost. Zero infrastructure overhead. | |
| IT architecture | Single-file no-build static site. Minimal and appropriate for this use case. | |
| Code efficiency | Hardcoded JS data arrays are simple and fast. Chart.js CDN avoids local bundling at the cost of a CDN dependency. | |
| Cybersecurity | No user data or backend. Chart.js CDN is the only external dependency and a potential supply-chain risk. | |
| Readability & maintainability | Easy to audit now; will require refactoring (data → separate JSON) as more years are added. | |
| AI / ML | Not applicable. No AI used; appropriate for deterministic visualization. | |
| Data accuracy & freshness | 2021–2023 data; rounded to €1B. No automated refresh. IGAE/Eurostat definitions may evolve. | |
| Other | Mobile responsiveness and cross-browser testing not documented. Data sourcing is transparent and cited. | |
