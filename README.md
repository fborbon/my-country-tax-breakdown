# Where Do My Taxes Go? 🇪🇸

**Live site: [https://fborbon.github.io/where-do-my-taxes-go](https://fborbon.github.io/where-do-my-taxes-go)**

An interactive, single-page visualisation of how Spain's government spends public money — broken down by category across fiscal years 2021, 2022, and 2023.

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

1. Social Protection — pensions, unemployment, disability, family benefits
2. Health — hospitals, primary care, pharmaceuticals
3. Education — pre-school through university
4. General Public Services — administration, judiciary, debt interest
5. Economic Affairs — infrastructure, agriculture (CAP), energy, R&D
6. Public Order & Safety — police, civil guard, prisons, emergency services
7. Housing & Community — social housing, water, sanitation
8. Defense — armed forces, NATO contributions
9. Environmental Protection — waste, water treatment, climate policy
10. Recreation, Culture & Religion — museums, sports, broadcasting

## Tech stack

Plain HTML + CSS + JavaScript. Charts rendered with [Chart.js 4](https://www.chartjs.org/) (CDN). No framework, no build tooling, no dependencies to install.

## License

MIT
