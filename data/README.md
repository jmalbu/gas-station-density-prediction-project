# Data Folder – Gas Station Density Project

This folder contains all the raw and processed datasets used in our analysis of gas station density across North Carolina counties (2020). The data covers a range of socioeconomic, demographic, infrastructure, and public safety indicators.

---

## File Descriptions

| File | Description |
|------|-------------|
| `2022_Road&Highway.pdf` | Official NC DOT report on road and highway infrastructure used to extract state and municipal road mileage by county. |
| `Education2019-23.xlsx` | County-level educational attainment data (e.g., high school, college rates) from 2019–2023. |
| `IndexOffensesByAgencyInCounty.xlsx` | Crime statistics by county, including total index crimes and agency coverage. |
| `UrbanInfluenceCodes2024.xlsx` | USDA's rural–urban classification codes used to characterize county urbanization. |
| `census_2020_summary.xlsx` | Demographic and housing summary statistics from the 2020 U.S. Census. |
| `census_2020_summary_edited.xlsx` | Cleaned and reformatted version of the above, used in analysis scripts. |
| `employment-and-income-linc.xlsx` | Data on employment, income, and labor force participation by county. |
| `unemployment_edited.xls.xlsx` | Cleaned unemployment rates and labor force info from ACS/BLS sources. |

---

## Notes

- All datasets are either public or aggregated from official state/federal sources.
- Final merged datasets were cleaned and used in the `.Rmd` scripts located in the root directory.
- File formats include `.xlsx` and `.pdf`. The cleaned `.csv` versions used directly in modeling may be located in processing scripts.

---

## Data Sources

- U.S. Census Bureau (2020)
- NC Department of Transportation (2022)
- NC Department of Public Safety
- American Community Survey (ACS)
- USDA Economic Research Service

---
