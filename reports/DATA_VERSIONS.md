# Dataset and Feature Set Versions

A record of each version of our cleaned data and feature list: what changed, and whose work it is based on.

---

## Version 2 (September 30, 2026)

**Files**

| File | What it is |
|---|---|
| `data/processed/cleaned_df_v2_2026-09-30_abhiram-agreed-cleaning_rhea-additions.csv` | Cleaned data (414 rows, 40 columns) |
| `data/processed/cleaned_df_encoded_v2_2026-09-30_abhiram-agreed-cleaning_rhea-additions.csv` | Model-ready copy with words turned into number columns (414 rows, 116 columns) |
| `reports/feature_sets_v2_2026-09-30_abhiram-agreed-cleaning_rhea-additions.json` | Columns the model may use (107 for spend, 102 for CPE) |

**Built from:** the team's agreed cleaning in Abhiram's notebook (`notebooks/clean_dataset.ipynb`, branch `abhiram-cleaned-dataset`), plus Rhea's additions (branch `cleaned-dataset-additions`).

**Whose input went into it**

| Teammate | Columns | Decisions |
|---|---|---|
| Rhea | brand, sub_product_name, country, pillar | Split brand into company, product and channel. Filled missing country and pillar as unknown |
| Emma | media_type, profession, specialty, campaign dates | Profession names from the advisor's code list. Removed specialty, the 3 rows with no start date, and campaign_end_date |
| Abhiram | reach, engagements, budget, engagement rate | No changes needed. Built the agreed cleaned dataset and notebook |
| Bakari | engagement frequency, pre-campaign prescriptions | No changes needed |
| Timothy | post_avg_NRx, pre_NRx_avg, npi_specialty, region, NRx_lift | Capped very high values, fixed two one-off labels, recalculated NRx_lift |
| Nida | cpe, total_spend, spend columns | Filled missing cpe with budget ÷ engagements |

**Rhea's additions on top of the agreed cleaning**

- Profession names in one style ("Unmapped code 15" for codes not on the advisor's list)
- Start date as a real date, plus year, quarter, month and campaign age
- 6 values recalculated so the NRx columns add up after the NRx_lift update
- Yes/no flags: cost filled in, spend under $1,000, budget looks wrong, missing targeting info, US region on a non-US campaign
- `n_periods` column (prescriptions before ÷ average prescriptions before)
- Model-ready encoded copy and feature list

---

## Version 1 (September 29, 2026)

**Files:** `data/processed/cleaned_df.csv`, `data/processed/cleaned_df_encoded.csv`, `reports/feature_sets.json`

**Built from:** Rhea's first cleaning (`notebooks/02_data_cleaning.ipynb`), based on the full data quality report (`notebooks/01_data_quality_report.ipynb`).

**Main differences from version 2:** it kept all 417 rows and the `specialty` column, used neutral profession labels (`code_8`), and did not cap outliers or recalculate NRx_lift. It is kept for reference.
