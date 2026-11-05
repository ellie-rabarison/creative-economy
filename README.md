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

<table>
  <thead>
    <tr><th>CEDM element</th><th>Indicator</th><th>Source</th></tr>
  </thead>
  <tbody>
    <tr><td rowspan="4"><b>Governance</b></td><td>Rule of law, government effectiveness</td><td>World Bank – Worldwide Governance Indicators</td></tr>
    <tr><td>World Press Freedom Index (2022–2026)</td><td>RSF</td></tr>
    <tr><td>Academic freedom, freedom of association</td><td>V-Dem (via Our World in Data)</td></tr>
    <tr><td>Gini index (inverted)</td><td>World Bank – World Development Indicators</td></tr>
    <tr><td rowspan="2"><b>Social &amp; cultural</b></td><td>Gender Inequality Index (inverted)</td><td>UNDP – Human Development Report</td></tr>
    <tr><td>World Heritage sites, Intangible Cultural Heritage entries (compiled manually)</td><td>UNESCO</td></tr>
    <tr><td rowspan="3"><b>Infrastructure</b></td><td>Internet use</td><td>World Bank – World Development Indicators (ITU data)</td></tr>
    <tr><td>Population covered by 4G/LTE</td><td>ITU</td></tr>
    <tr><td>Logistics performance</td><td>World Bank – World Development Indicators</td></tr>
    <tr><td><b>Demand</b></td><td>Creative goods imports and exports (% of merchandise trade)</td><td>UNCTADstat</td></tr>
    <tr><td rowspan="4"><b>Creative value &amp; IP</b></td><td>Creative goods exports by product group</td><td>UNCTADstat</td></tr>
    <tr><td>Creative services trade (experimental estimates)</td><td>UNCTADstat</td></tr>
    <tr><td>Trademark and industrial design applications, resident vs non-resident</td><td>WIPO IP statistics (via World Bank)</td></tr>
    <tr><td>Charges for the use of IP, receipts</td><td>World Bank – World Development Indicators</td></tr>
    <tr><td rowspan="2"><i>Context and helpers</i></td><td>Human Development Index</td><td>UNDP – Human Development Report</td></tr>
    <tr><td>Population, merchandise exports and imports</td><td>World Bank – World Development Indicators</td></tr>
  </tbody>
</table>

Data remain subject to the terms of their original sources.

---

**Author:** Ellie Rabarison

*Independent personal project, based on public data only. Views and any errors are my own.*
