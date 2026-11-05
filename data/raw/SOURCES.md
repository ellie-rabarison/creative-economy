# Data sources

All files are in `data/raw/`, unedited as downloaded (except the manually compiled UNESCO file). Downloaded on 2026-11-04 unless stated otherwise.

## World Bank – World Development Indicators (WDI)
- URL: https://databank.worldbank.org/source/world-development-indicators
- Series: Individuals using the Internet (% of population); Logistics performance index: Overall; Gini index; Charges for the use of intellectual property, receipts (BoP, current US$); Trademark applications, resident and nonresident, by count; Industrial design applications, resident and nonresident, by count (WIPO data); Population, total; Merchandise exports and imports (current US$)
- Countries: Madagascar, Mauritius, Seychelles, Comoros + aggregates: World, Sub-Saharan Africa, Small states, Least developed countries (UN classification)
- Years: 2015–2025
- Files: `wdi_data.csv`, `wdi_metadata.csv`
- Notes: missing values coded "..". Last rows of the file are notes ("Data from database", "Last Updated"). LPI is not annual (latest edition shown as 2022) and is missing for Seychelles; Gini years vary widely (2017–2024); Comoros has no IP filing data and IP receipts only to 2015.

## World Bank – Worldwide Governance Indicators (WGI)
- URL: https://databank.worldbank.org/source/worldwide-governance-indicators
- Series: Rule of Law and Government Effectiveness, both as "Governance estimate" and "Governance score (0–100)"
- Countries: the four islands (no aggregates needed: estimates are centred on a world average of 0)
- Years: 2015–2025
- Files: `wgi_data.csv`, `wgi_metadata.csv`
- Notes: the analysis uses the governance estimate (approx. −2.5 to +2.5), as in the CEDM methodology (WIPO Philippines report, p. 83). The 0–100 scores are in the file but not used.

## UNCTADstat – Creative goods: bilateral trade by product group (annual)
- URL: https://unctadstat.unctad.org/datacentre/dataviewer/US.CreativeGoodsValue
- Selection: exports and imports; partner = World; all creative goods + product groups and sub-groups
- Measures: US$ at current prices (thousands); % of world; % of total merchandise trade
- Economies: the four islands + World, Sub-Saharan Africa, LDCs, SIDS and SIDS sub-regions
- Years: 2015–2024
- Files: `unctad_creative_goods_data.csv`, `unctad_creative_goods_metadata.txt`
- Notes: hierarchical products (sub-groups sum to "Manufacturing of crafts and design goods": never add a group and its sub-groups). Comoros: 25 values "not publishable", no 2024. LDCs 2024 not publishable. Most aggregate values flagged "Estimated". The SIDS aggregate is dominated by "SIDS: Pacific" and is not a good benchmark.

## UNCTADstat – Creative services: trade, estimates for individual economies
- URL: https://unctadstat.unctad.org/datacentre/dataviewer/US.CreativeServ_Indiv_Tot
- Selection: exports and imports; total creative services (no breakdown available)
- Measures: US$ (thousands); % of total trade in services; growth rate
- Economies: the four islands · Years: 2015–2024
- Files: `unctad_creative_services_data.csv`, `unctad_creative_services_metadata.txt`
- Notes: EXPERIMENTAL dataset: only 32% of values are official statistics, the rest are interpolated or extrapolated (UNCTAD); no per-value flag. Creative services are defined through 10 EBOPS 2010 items (SH2, SH3, SH4, SI21, SI3, SJ1, SJ22, SJ311, SK1, SK23), including software, R&D and computer services. Madagascar: exports only 2015, 2017, 2018; imports not publishable. Comoros: exports not publishable; imports 2015–2022. Unusual jumps: Mauritius exports +169% (2024); Seychelles imports −89% (2020).

## ITU DataHub – Population coverage by at least LTE/WiMAX
- URL: https://datahub.itu.int
- Indicator: i271GA, % of population covered by at least an LTE/WiMAX mobile network
- Economies: the four islands + ITU aggregates (World, regions, LDC, SIDS, LLDC, income groups; included automatically)
- Years: 2015–2025
- File: `itu_mobile_coverage_data.csv`
- Notes: island values mostly from national regulators; ITU estimates for Madagascar and Comoros (2024) and for Comoros and Seychelles (2015). All aggregates are ITU estimates. Comoros 2023: one operator (Telma) did not report. Internet users taken from WDI (same ITU source).

## RSF – World Press Freedom Index
- URL: https://rsf.org/en/index
- Files: `rsf_press_freedom_2022_data.csv` to `rsf_press_freedom_2026_data.csv` (one file per year, all 180 countries)
- Notes: only 2022 onwards, because RSF changed its methodology in 2022 (earlier scores not comparable). Semicolon-separated, decimal commas. Column names change between years ("Score" until 2024, then "Score 2025", "Score 2026"; extra "Situation" column in 2024). 2025–2026 files have encoding issues in country names: match on ISO code.

## V-Dem – Academic Freedom Index and Freedom of Association Index (via Our World in Data)
- URLs:
  - https://ourworldindata.org/grapher/academic-freedom-index.csv?v=1&csvType=full&useColumnShortNames=true
  - Freedom of association: OWID grapher page "Freedom of Association Index" (V-Dem), full data CSV
- Files: `vdem_academic_freedom_data.csv`, `vdem_academic_freedom_metadata.json`, `vdem_association_freedom_data.csv`, `vdem_association_freedom_metadata.json`
- Coverage: all countries, full historical series (to 2025); scale 0–1 (1 = most free)
- Notes: academic freedom file has no regional aggregates: the Africa benchmark is computed as the unweighted mean of African countries. The freedom of association file includes "Africa" and "Africa (population-weighted)".

## UNESCO – World Heritage sites and Intangible Cultural Heritage (manual compilation)
- File: `unesco_heritage_data.csv` (one row per entry), documented in `unesco_heritage_metadata.txt`
- Sources: whc.unesco.org (States Parties pages) and ich.unesco.org, checked 2026-11-04
- Notes: compiled by hand; shared (multinational) entries counted for each country; tentative lists not included.

## UNDP – Human Development Report, composite indices time series
- URL: https://hdr.undp.org/data-center/documentation-and-downloads (HDR 2025)
- Technical notes: https://hdr.undp.org/sites/default/files/2025_HDR/HDR25_Technical_Notes.pdf
- File: `undp_hdr_data.csv`, documented in `undp_hdr_metadata.txt`
- Coverage: all countries + aggregates (World, regions, HDI groups; no LDC/SIDS), 1990–2023
- Notes: file is Latin-1 encoded. Wide format (`gii_2023`, `hdi_2023`…). GII: Mauritius and Comoros 2015–2023; Madagascar 2021–2023 only; Seychelles not covered. Higher GII = more inequality (inverted in the analysis). Do not mix values from different HDR editions.
