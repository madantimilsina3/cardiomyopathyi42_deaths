# The Silent Burden of Heart Disease in Young America

**Project by:** Madan Timilsina <br>
**Date:** 23 August, 2026

---

## Background & Objectives

This project is a data-driven investigation into an overlooked condition where cardiomyopathy silently causes premature deaths among young people, demanding immediate attention. The core objective of this study is to challenge the prevailing assumption that heart disease is strictly an older adult's affliction. By analyzing mortality rates rather than misleading raw counts, this project aims to answer how cardiomyopathy quietly drives mortality rates among America's youth compared to broader heart disease trends.

---

## Data Source & Methodology

- **Data Provenance:** The primary numerator data was sourced from the CDC NCHS microdata, containing individual death records by ICD-10 code. The denominator data was sourced from U.S. Census Bureau population estimates organized by state, age, race, and sex.
- **Timeframe:** The dataset covers a 7-year timeline from 2018 to 2024.
- **Scope & Parameters:** The data focus was on the broad NCHS "Diseases of Heart" category (including Cardiomyopathy, Heart Failure, Chronic Ischemic Heart Disease, and Heart Attack), specifically isolating the subcategory of Cardiomyopathy. The demographic target was individuals aged 0–44 across all 50 US states and Washington DC.
- **Tools Used:** Pandas was used for parsing the 15GB raw FWF data, DuckDB was utilized as the staging database, and CDC WONDER alongside Census data were used for data integration. Interactive HTML dashboards were generated with the assistance of Claude.

---

## Data Processing Summary

- Aggregated and parsed **22,043,274** total mortality records spanning the 7-year timeline.
- Tracked **4,774,283** deaths attributed broadly to heart disease.
- Isolated **139,810** deaths driven specifically by Cardiomyopathy for targeted demographic and geospatial modeling.
- Detected and corrected a structural shift in the raw data starting in 2021, where the tape location for the "Race" column moved from positions 445–446 to 489–490.
- Translated coded values, such as ICD-10 and demographics, into human-readable text to prepare the dataset for visualization.

---

## Key Insights

**Age Factor**<br>
Cardiomyopathy dominates younger populations, accounting for approximately 60% of heart disease deaths in the 0–24 age group every single year. This share rapidly declines with age, ultimately being replaced by Chronic Ischemic Heart Disease and Heart Attacks.

**Geographic Distribution**<br>
Cardiomyopathy is spread across the nation with a national average of 4.5 deaths per 100k. Washington DC reported the highest rate at 29.8 per 100k, while Texas reported the lowest at 2.6 per 100k.

**Sex Disparity**<br>
Men bear double the mortality burden, with an approximate 2.1x average Male-to-Female ratio. Between 2018 and 2024, the male mortality rate fell from 6.4 to 5.3 per 100k, while the female rate fell more modestly from 3.0 to 2.6 per 100k.

**Seasonality**<br>
Averaged across all seven years, January is the peak month for mortality, showing a sharp increase from November. However, the single largest monthly count in the dataset occurred in July 2021, with 185 deaths.

**Overall Impact**<br>
Cardiomyopathy causes just 3% of all heart disease deaths (139,236 out of 4.77 million). Even though it is not the largest killer overall, it is silently becoming a major threat to the youth due to a lack of awareness and early screening.
