# Measuring the Creative Ecosystem of Indian Ocean Island States

**What can public data tell us about the creative economies of Madagascar, Mauritius, Seychelles and Comoros, and what can it not?**

An independent data project applying the structure of WIPO's **Creative Economy Data Model (CEDM)** to four island economies of the Western Indian Ocean, using only publicly available international data.

> **Status: work in progress (started November 2026).** Data collection, documentation and the data availability audit are complete; the cleaning pipeline is being built source by source; benchmarking and charts come next.

---

## Why this project

The creative economy (crafts, music, design, audiovisual and digital content) is a growing source of income and exports, but it is poorly measured, especially in small and low-income economies where much creative activity is informal. WIPO's CEDM assesses a country's creative ecosystem across its **enabling environment** (governance, social and cultural context, IP), its **resources** (skills, infrastructure, finance, demand) and the **creative value** it produces.

National CEDM diagnostics rely on rich national data. This project asks a simpler question: **how far can public, cross-country data go for small island economies**, and where are the gaps?

## Approach

- **Countries:** Madagascar, Mauritius, Seychelles and Comoros, the four island states of the Indian Ocean Commission (Réunion and Mayotte, as French departments, are absent from country-level international data).
- **Framework:** indicators grouped by CEDM element, following the indicator tables of WIPO's first national CEDM report (Philippines, 2026).
- **Benchmarks:** each island is compared with World Bank, UNCTAD, ITU and UNDP aggregates (World, Sub-Saharan Africa, least developed countries, small states) rather than standardised across all countries, given the four-country focus.
- **Latest available year:** for each country and indicator, the most recent value since 2015, with the year recorded, as in the CEDM methodology. No imputation of missing values.

## Data

Ten public datasets, all documented in [`data/raw/SOURCES.md`](data/raw/SOURCES.md):

| Source | Indicators | CEDM element |
|---|---|---|
| World Bank – Worldwide Governance Indicators | Rule of law, government effectiveness | Governance |
| World Bank – World Development Indicators | Internet use, logistics performance, Gini, IP receipts, population, merchandise trade | Infrastructure, governance, helpers |
| WIPO IP statistics (via World Bank) | Trademark and industrial design applications, resident vs non-resident | Creative value & IP |
| UNCTADstat | Creative goods trade by product group; creative services trade (experimental) | Demand, creative value |
| ITU | Population covered by 4G/LTE | Infrastructure |
| RSF | World Press Freedom Index (2022–2026) | Governance |
| V-Dem (via Our World in Data) | Academic freedom, freedom of association | Governance |
| UNESCO | World Heritage sites, Intangible Cultural Heritage entries (compiled manually) | Social & cultural |
| UNDP – Human Development Report | Gender Inequality Index, Human Development Index | Social & cultural, context |

Data remain subject to the terms of their original sources.

## Data availability audit

The audit table [`outputs/cedm_data_audit.csv`](outputs/cedm_data_audit.csv) checks all **49 indicators** used in WIPO's Philippines report (plus a few additions) against the four islands: is the indicator available, for which latest year, and from which source.

**So far, for Madagascar: 22 indicators confirmed available, 11 confirmed unavailable, 16 still to be checked.**

The gaps cluster where the creative economy is hardest to see:
- **Creative employment:** no published data on employment, self-employment or gender in the creative industries for any of the four islands.
- **Creative services:** UNCTAD's estimates are experimental (only about a third of values are official statistics); Madagascar's series stops in 2018.
- **Survey-based indicators** (World Values Survey, PISA): none of the four islands appears to be covered.
- **Comoros** is the least covered: no IP filing data, and 2024 creative trade data are not publishable.

## Early findings

*Preliminary: to be confirmed in the analysis stage.*

- **Madagascar's creators increasingly use IP.** Residents filed 98% of Madagascar's industrial design applications in 2024, and their share of trademark applications rose from 41% (2015) to 60% (2024) (WIPO data).
- **Crafts dominate Madagascar's creative exports.** Wickerware (mostly raffia products) grew from US$6.3 million in 2015 to US$35.4 million in 2024, about two-thirds of all creative goods exports (UNCTAD).
- **A widening digital gap.** In 2015, 4G networks covered 21% of Madagascar's population, more than the African average (11%). By 2024, Madagascar had reached 35%, against 74% for Africa and 70% for least developed countries (ITU).
- **Four very different islands.** They span all four World Bank income groups, from low (Madagascar) to high (Seychelles), and governance indicators split them into two pairs: Mauritius and Seychelles above the world average, Madagascar and Comoros below.

## Repository structure

```
├── data/
│   ├── raw/            # Downloaded data, unedited, with metadata and SOURCES.md
│   └── processed/      # Cleaned, harmonised data (generated by the scripts)
├── src/
│   └── clean_data.py   # Turns each raw source into one tidy table
├── notebooks/          # Step-by-step exploration
├── outputs/
│   ├── cedm_data_audit.csv
│   └── figures/
└── requirements.txt
```

## Reproduce

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python src/clean_data.py
```

## Next steps

- Extend the cleaning pipeline to all sources (currently: World Bank WDI and WGI)
- Complete the audit for the remaining "to check" indicators
- Benchmark each island against regional and income-group aggregates, by CEDM element
- Charts: Madagascar creative exports treemap, regional comparisons, trends
- Explore alternative data (e.g. online platforms) for the creative activity official statistics miss

---

**Author:** Ellie Rabarison, economist, Geneva

*Independent personal project, based on public data only. Views and any errors are my own.*
