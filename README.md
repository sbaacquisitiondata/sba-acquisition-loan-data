---
license: cc-by-4.0
language:
  - en
pretty_name: SBA 7(a) Business Acquisition Loans
tags:
  - sba
  - small-business
  - lending
  - finance
  - franchise
  - naics
size_categories:
  - 1K<n<10K
configs:
  - config_name: franchises
    data_files: data/franchises.csv
  - config_name: industries
    data_files: data/industries.csv
  - config_name: states
    data_files: data/states.csv
  - config_name: metros
    data_files: data/metros.csv
  - config_name: lenders
    data_files: data/lenders.csv
  - config_name: state-industry
    data_files: data/state-industry.csv
  - config_name: defaults-by-cohort
    data_files: data/defaults-by-cohort.csv
  - config_name: defaults-by-industry
    data_files: data/defaults-by-industry.csv
  - config_name: defaults-by-state
    data_files: data/defaults-by-state.csv
  - config_name: defaults-by-franchise
    data_files: data/defaults-by-franchise.csv
  - config_name: defaults-by-lender
    data_files: data/defaults-by-lender.csv
  - config_name: state-lenders-fy2026
    data_files: data/state-lenders-fy2026.csv
  - config_name: metro-lenders-fy2026
    data_files: data/metro-lenders-fy2026.csv
  - config_name: top-100-lenders-fy2026
    data_files: data/top-100-lenders-fy2026.csv
  - config_name: naics-size-standards
    data_files: data/naics-size-standards.csv
  - config_name: sba-franchise-directory
    data_files: data/sba-franchise-directory.csv
---

# SBA 7(a) Business Acquisition Loans

Aggregated data on every U.S. Small Business Administration 7(a) loan recorded as a **change of ownership**, meaning a loan used to buy an existing business, approved FY2018 to FY2026. Built from the SBA's public 7(a) FOIA loan file and published by [SBA Acquisition Data](https://sbaacquisitiondata.com), where every table here also appears as a browsable page.

- **Data as of:** 2026-09-30 (SBA file release). Next SBA release expected January 2027.
- **Coverage:** 48,902 acquisition loans, $53.7B approved, median loan $645,250.
- **Charge-off rates** use the seasoned cohort, loans approved FY2018 to FY2021: 3.52% of 20,546 acquisition loans were charged off.
- **Aggregates only.** No borrower names, addresses or loan-level records are included.

## Files

| File | Table | Rows | Description |
|---|---|---|---|
| [`franchises.csv`](data/franchises.csv) | Franchise brands | 347 | One row per franchise brand page: acquisition loans, loan sizes and charge-off rate. |
| [`industries.csv`](data/industries.csv) | Industries (NAICS) | 300 | One row per six-digit NAICS industry page. |
| [`states.csv`](data/states.csv) | States and territories | 54 | One row per state or territory page. |
| [`metros.csv`](data/metros.csv) | Metro areas | 15 | One row per metro area page (counties grouped by the site). |
| [`lenders.csv`](data/lenders.csv) | Lenders | 280 | One row per lender page. Lender names are those recorded in the SBA file. |
| [`state-industry.csv`](data/state-industry.csv) | State by industry | 548 | One row per state and industry combination page. |
| [`defaults-by-cohort.csv`](data/defaults-by-cohort.csv) | Charge-offs by approval year | 4 | Charge-off counts and rates by approval year, FY2018 to FY2021, acquisition against non-acquisition 7(a) loans. |
| [`defaults-by-industry.csv`](data/defaults-by-industry.csv) | Charge-offs by industry | 75 | Charge-off rate for acquisition loans approved FY2018 to FY2021, industries with at least 50 seasoned loans. |
| [`defaults-by-state.csv`](data/defaults-by-state.csv) | Charge-offs by state | 46 | Charge-off rate for acquisition loans approved FY2018 to FY2021, states with at least 50 seasoned loans. |
| [`defaults-by-franchise.csv`](data/defaults-by-franchise.csv) | Charge-offs by franchise brand | 32 | Charge-off rate for acquisition loans approved FY2018 to FY2021, brands with at least 25 seasoned loans (supply agreements excluded). |
| [`defaults-by-lender.csv`](data/defaults-by-lender.csv) | Charge-offs by lender | 43 | Charge-off rate for acquisition loans approved FY2018 to FY2021, lenders with at least 100 seasoned loans. |
| [`state-lenders-fy2026.csv`](data/state-lenders-fy2026.csv) | State lender rankings FY2026 | 1,274 | Top 25 lenders by SBA 7(a) loans of any purpose in each state or territory in FY2026, with loans, dollars and the lender's acquisition share in that state. |
| [`metro-lenders-fy2026.csv`](data/metro-lenders-fy2026.csv) | Metro lender rankings FY2026 | 375 | Top 25 lenders by SBA 7(a) loans of any purpose in each metro area in FY2026, with loans, dollars and the lender's acquisition share in that metro area. |
| [`top-100-lenders-fy2026.csv`](data/top-100-lenders-fy2026.csv) | Top 100 lenders FY2026 | 100 | The 100 lenders with the most SBA 7(a) loans of any purpose in FY2026: loans, dollars, average loan, acquisition share and Preferred Lenders Program share. |
| [`naics-size-standards.csv`](data/naics-size-standards.csv) | NAICS size standards with loan counts | 300 | SBA size standard (table in effect on the date shown on the NAICS page) beside acquisition loan counts, for each industry with a page. |
| [`sba-franchise-directory.csv`](data/sba-franchise-directory.csv) | SBA Franchise Directory | 3,590 | Every entry in the SBA Franchise Directory copy dated 2026-10-28 with acquisition loan counts (FY2018 to FY2026) and the page here, if the brand has one. |

Column definitions for every file are in [DATA_DICTIONARY.md](DATA_DICTIONARY.md). Rates are fractions (0.0352 = 3.52%). Dollar amounts are unformatted US dollars.

## Method

1. Download the SBA 7(a) FOIA files from [data.sba.gov](https://data.sba.gov/dataset/7a-504-foia).
2. Keep loans whose business-age field reads "Change of Ownership" (recorded by the SBA from FY2018).
3. Exclude cancelled loans from counts and totals; exclude cancelled and undisbursed loans from charge-off rates.
4. Map 2017 NAICS codes to the 2022 edition where the industry was renumbered.
5. Aggregate by franchise brand, industry, state, metro area and lender.

Full methodology: [https://sbaacquisitiondata.com/methodology](https://sbaacquisitiondata.com/methodology). Every page on the site has a "Cite this data" block and a JSON endpoint; see [https://sbaacquisitiondata.com/ai](https://sbaacquisitiondata.com/ai).

## Limitations

- Business age is recorded by lenders and may be incomplete; loans not marked "Change of Ownership" are excluded even if they financed an acquisition.
- Charge-off is the SBA's final loss action and lags default; recent cohorts are still maturing.
- The file records the approved loan amount, not the purchase price, equity injection or seller financing.
- Lender names are as recorded in the SBA file.

## Citation

> SBA Acquisition Data, "SBA 7(a) Business Acquisition Loans," data as of 2026-09-30, https://sbaacquisitiondata.com. Source: U.S. Small Business Administration 7(a) FOIA loan file.

## License

The aggregates in this repository are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/); please credit SBA Acquisition Data and link to https://sbaacquisitiondata.com. The underlying SBA loan file is a U.S. government work.

## Updates

The SBA publishes a new FOIA file quarterly. This package is regenerated from the site after each release; the [changelog](https://sbaacquisitiondata.com/changelog) lists every update.

Not affiliated with the U.S. Small Business Administration. Not legal, financial or lending advice.
