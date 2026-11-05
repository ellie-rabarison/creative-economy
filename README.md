# Measuring the Creative Ecosystem of Indian Ocean Island States

**What can public data tell us about the creative economies of Madagascar, Mauritius, Seychelles and Comoros, and what can it not?**

An independent data project applying the structure of WIPO's **Creative Economy Data Model (CEDM)** to four island economies of the Western Indian Ocean, using only publicly available international data.

> **Status: work in progress (started November 2026).** Data collection, documentation and the data availability audit are complete; the cleaning pipeline is being built source by source; benchmarking and charts come next.

---

## Why this project

The creative economy (crafts, music, design, audiovisual and digital content) is a growing source of income and exports, but it is poorly measured, especially in small and low-income economies where much creative activity is informal. WIPO's CEDM assesses a country's creative ecosystem across its **enabling environment** (governance, social and cultural context, IP), its **resources** (skills, infrastructure, finance, demand) and the **creative value** it produces.

National CEDM diagnostics rely on rich national data. This project asks a simpler question: **how far can public, cross-country data go for (small) island economies**, and where are the gaps?

## Approach

- **Countries:** Comoros, Madagascar, Mauritius and Seychelles, the four island states of the Indian Ocean Commission (Réunion and Mayotte, as French departments, are absent from country-level international data).
- **Framework:** indicators grouped by CEDM element, following the indicator tables of WIPO's first national CEDM report (Philippines, 2026).
- **Benchmarks:** each island is compared with World Bank, UNCTAD, ITU and UNDP aggregates (World, Sub-Saharan Africa, least developed countries, small states) rather than standardised across all countries, given the four-country focus.
- **Latest available year:** for each country and indicator, the most recent value since 2015, with the year recorded, as in the CEDM methodology. No imputation of missing values.

## Data

Ten public datasets, all documented in [`data/raw/SOURCES.md`](data/raw/SOURCES.md):

| CEDM element | Indicator | Source |
|---|---|---|
| **Governance** | Rule of law, government effectiveness | World Bank – Worldwide Governance Indicators |
| | World Press Freedom Index (2022–2026) | RSF |
| | Academic freedom, freedom of association | V-Dem (via Our World in Data) |
| | Gini index (inverted) | World Bank – World Development Indicators |
| **Social & cultural** | Gender Inequality Index (inverted) | UNDP – Human Development Report |
| | World Heritage sites, Intangible Cultural Heritage entries (compiled manually) | UNESCO |
| **Infrastructure** | Internet use | World Bank – World Development Indicators (ITU data) |
| | Population covered by 4G/LTE | ITU |
| | Logistics performance | World Bank – World Development Indicators |
| **Demand** | Creative goods imports and exports (% of merchandise trade) | UNCTADstat |
| **Creative value & IP** | Creative goods exports by product group | UNCTADstat |
| | Creative services trade (experimental estimates) | UNCTADstat |
| | Trademark and industrial design applications, resident vs non-resident | WIPO IP statistics (via World Bank) |
| | Charges for the use of IP, receipts | World Bank – World Development Indicators |
| *Context and helpers* | Human Development Index | UNDP – Human Development Report |
| | Population, merchandise exports and imports | World Bank – World Development Indicators |

Data remain subject to the terms of their original sources.

---

**Author:** Ellie Rabarison

*Independent personal project, based on public data only. Views and any errors are my own.*
