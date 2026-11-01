# Data dictionary

Generated from the site's own CSV definitions. Data as of 2026-09-30. Rates are fractions; dollars are unformatted US dollars.


## franchises.csv

Franchise brands. One row per franchise brand page: acquisition loans, loan sizes and charge-off rate. Rows: 347. Online: https://sbaacquisitiondata.com/datasets/franchises.csv

| Column | Meaning |
|---|---|
| `slug` | URL slug; page is /franchise/{slug} |
| `name` | Display name |
| `url` | Page URL |
| `acquisition_loans` | SBA 7(a) loans recorded as a change of ownership, all approval years in the file |
| `total_dollars` | Sum of gross approval amounts, US dollars |
| `median_loan` | Median gross approval, US dollars |
| `p25_loan` | 25th percentile loan, US dollars |
| `p75_loan` | 75th percentile loan, US dollars |
| `avg_interest_rate` | Average initial interest rate in percent, loans with a recorded rate (blank if none) |
| `median_term_months` | Median loan term in months (blank if none recorded) |
| `jobs_supported` | Sum of jobs supported as reported by lenders |
| `seasoned_loans` | Disbursed loans approved FY2018 to FY2021 (the seasoned cohort) |
| `seasoned_charged_off` | Seasoned loans with status CHGOFF |
| `charge_off_rate` | seasoned_charged_off / seasoned_loans, as a fraction; blank under 20 seasoned loans |
| `primary_naics` | Most common NAICS code for the brand (blank if none) |
| `states_count` | Number of states with loans |
| `in_sba_directory` | true if the brand matched the SBA Franchise Directory |
| `supply_agreement` | true for fuel, dealer or similar supply agreements |

## industries.csv

Industries (NAICS). One row per six-digit NAICS industry page. Rows: 300. Online: https://sbaacquisitiondata.com/datasets/industries.csv

| Column | Meaning |
|---|---|
| `naics` | Six-digit NAICS 2022 code |
| `slug` | URL slug; page is /industry/{slug} |
| `name` | Industry name |
| `url` | Page URL |
| `acquisition_loans` | SBA 7(a) loans recorded as a change of ownership, all approval years in the file |
| `total_dollars` | Sum of gross approval amounts, US dollars |
| `median_loan` | Median gross approval, US dollars |
| `p25_loan` | 25th percentile loan, US dollars |
| `p75_loan` | 75th percentile loan, US dollars |
| `avg_interest_rate` | Average initial interest rate in percent, loans with a recorded rate (blank if none) |
| `median_term_months` | Median loan term in months (blank if none recorded) |
| `jobs_supported` | Sum of jobs supported as reported by lenders |
| `seasoned_loans` | Disbursed loans approved FY2018 to FY2021 (the seasoned cohort) |
| `seasoned_charged_off` | Seasoned loans with status CHGOFF |
| `charge_off_rate` | seasoned_charged_off / seasoned_loans, as a fraction; blank under 20 seasoned loans |

## states.csv

States and territories. One row per state or territory page. Rows: 54. Online: https://sbaacquisitiondata.com/datasets/states.csv

| Column | Meaning |
|---|---|
| `code` | Two-letter postal code |
| `slug` | URL slug; page is /state/{slug} |
| `name` | State name |
| `url` | Page URL |
| `rank_by_loans` | Rank by acquisition loans, 1 = most |
| `share_of_national` | Share of all acquisition loans, as a fraction |
| `acquisition_loans` | SBA 7(a) loans recorded as a change of ownership, all approval years in the file |
| `total_dollars` | Sum of gross approval amounts, US dollars |
| `median_loan` | Median gross approval, US dollars |
| `p25_loan` | 25th percentile loan, US dollars |
| `p75_loan` | 75th percentile loan, US dollars |
| `avg_interest_rate` | Average initial interest rate in percent, loans with a recorded rate (blank if none) |
| `median_term_months` | Median loan term in months (blank if none recorded) |
| `jobs_supported` | Sum of jobs supported as reported by lenders |
| `seasoned_loans` | Disbursed loans approved FY2018 to FY2021 (the seasoned cohort) |
| `seasoned_charged_off` | Seasoned loans with status CHGOFF |
| `charge_off_rate` | seasoned_charged_off / seasoned_loans, as a fraction; blank under 20 seasoned loans |

## metros.csv

Metro areas. One row per metro area page (counties grouped by the site). Rows: 15. Online: https://sbaacquisitiondata.com/datasets/metros.csv

| Column | Meaning |
|---|---|
| `slug` | URL slug; page is /metro/{slug} |
| `name` | Metro area name |
| `state_code` | Two-letter state code |
| `url` | Page URL |
| `share_of_state` | Share of the state's acquisition loans, as a fraction |
| `acquisition_loans` | SBA 7(a) loans recorded as a change of ownership, all approval years in the file |
| `total_dollars` | Sum of gross approval amounts, US dollars |
| `median_loan` | Median gross approval, US dollars |
| `p25_loan` | 25th percentile loan, US dollars |
| `p75_loan` | 75th percentile loan, US dollars |
| `avg_interest_rate` | Average initial interest rate in percent, loans with a recorded rate (blank if none) |
| `median_term_months` | Median loan term in months (blank if none recorded) |
| `jobs_supported` | Sum of jobs supported as reported by lenders |
| `seasoned_loans` | Disbursed loans approved FY2018 to FY2021 (the seasoned cohort) |
| `seasoned_charged_off` | Seasoned loans with status CHGOFF |
| `charge_off_rate` | seasoned_charged_off / seasoned_loans, as a fraction; blank under 20 seasoned loans |

## lenders.csv

Lenders. One row per lender page. Lender names are those recorded in the SBA file. Rows: 280. Online: https://sbaacquisitiondata.com/datasets/lenders.csv

| Column | Meaning |
|---|---|
| `slug` | URL slug; page is /lender/{slug} |
| `name` | Lender name as recorded by the SBA |
| `display_name` | Common name used on the site |
| `state` | Lender home state |
| `url` | Page URL |
| `all_7a_loans` | All 7(a) loans by the lender since FY2020, any purpose |
| `all_7a_dollars` | Gross approval of those loans, US dollars |
| `plp_share` | Share of acquisition loans under the Preferred Lenders Program, as a fraction |
| `acquisition_loans` | SBA 7(a) loans recorded as a change of ownership, all approval years in the file |
| `total_dollars` | Sum of gross approval amounts, US dollars |
| `median_loan` | Median gross approval, US dollars |
| `p25_loan` | 25th percentile loan, US dollars |
| `p75_loan` | 75th percentile loan, US dollars |
| `avg_interest_rate` | Average initial interest rate in percent, loans with a recorded rate (blank if none) |
| `median_term_months` | Median loan term in months (blank if none recorded) |
| `jobs_supported` | Sum of jobs supported as reported by lenders |
| `seasoned_loans` | Disbursed loans approved FY2018 to FY2021 (the seasoned cohort) |
| `seasoned_charged_off` | Seasoned loans with status CHGOFF |
| `charge_off_rate` | seasoned_charged_off / seasoned_loans, as a fraction; blank under 20 seasoned loans |

## state-industry.csv

State by industry. One row per state and industry combination page. Rows: 548. Online: https://sbaacquisitiondata.com/datasets/state-industry.csv

| Column | Meaning |
|---|---|
| `state_code` | Two-letter postal code |
| `state_slug` | State URL slug |
| `naics` | Six-digit NAICS 2022 code |
| `industry_slug` | Industry URL slug; page is /state/{state_slug}/{industry_slug} |
| `name` | Industry name |
| `url` | Page URL |
| `acquisition_loans` | SBA 7(a) loans recorded as a change of ownership, all approval years in the file |
| `total_dollars` | Sum of gross approval amounts, US dollars |
| `median_loan` | Median gross approval, US dollars |
| `p25_loan` | 25th percentile loan, US dollars |
| `p75_loan` | 75th percentile loan, US dollars |
| `avg_interest_rate` | Average initial interest rate in percent, loans with a recorded rate (blank if none) |
| `median_term_months` | Median loan term in months (blank if none recorded) |
| `jobs_supported` | Sum of jobs supported as reported by lenders |
| `seasoned_loans` | Disbursed loans approved FY2018 to FY2021 (the seasoned cohort) |
| `seasoned_charged_off` | Seasoned loans with status CHGOFF |
| `charge_off_rate` | seasoned_charged_off / seasoned_loans, as a fraction; blank under 20 seasoned loans |

## defaults-by-cohort.csv

Charge-offs by approval year. Charge-off counts and rates by approval year, FY2018 to FY2021, acquisition against non-acquisition 7(a) loans. Rows: 4. Online: https://sbaacquisitiondata.com/datasets/defaults-by-cohort.csv

| Column | Meaning |
|---|---|
| `fy` | SBA fiscal year of approval |
| `acq_loans` | Disbursed acquisition loans |
| `acq_charged_off` | Acquisition loans with status CHGOFF |
| `acq_rate` | Count rate, fraction |
| `acq_dollar_rate` | Charged-off dollars / approved dollars, fraction |
| `other_loans` | Disbursed non-acquisition 7(a) loans |
| `other_charged_off` | Non-acquisition loans with status CHGOFF |
| `other_rate` | Count rate, fraction |
| `other_dollar_rate` | Dollar rate, fraction |

## defaults-by-industry.csv

Charge-offs by industry. Charge-off rate for acquisition loans approved FY2018 to FY2021, industries with at least 50 seasoned loans. Rows: 75. Online: https://sbaacquisitiondata.com/datasets/defaults-by-industry.csv

| Column | Meaning |
|---|---|
| `naics` | NAICS code |
| `name` | Industry name |
| `slug` | Industry URL slug |
| `seasoned_loans` | Seasoned loans |
| `charged_off` | Loans with status CHGOFF |
| `charge_off_rate` | Fraction |
| `national_rate` | National acquisition rate for the same cohort, fraction |

## defaults-by-state.csv

Charge-offs by state. Charge-off rate for acquisition loans approved FY2018 to FY2021, states with at least 50 seasoned loans. Rows: 46. Online: https://sbaacquisitiondata.com/datasets/defaults-by-state.csv

| Column | Meaning |
|---|---|
| `code` | Two-letter postal code |
| `name` | State name |
| `slug` | State URL slug |
| `seasoned_loans` | Seasoned loans |
| `charged_off` | Loans with status CHGOFF |
| `charge_off_rate` | Fraction |
| `national_rate` | National acquisition rate, fraction |

## defaults-by-franchise.csv

Charge-offs by franchise brand. Charge-off rate for acquisition loans approved FY2018 to FY2021, brands with at least 25 seasoned loans (supply agreements excluded). Rows: 32. Online: https://sbaacquisitiondata.com/datasets/defaults-by-franchise.csv

| Column | Meaning |
|---|---|
| `name` | Brand display name |
| `slug` | Franchise URL slug |
| `seasoned_loans` | Seasoned loans |
| `charged_off` | Loans with status CHGOFF |
| `charge_off_rate` | Fraction |
| `national_rate` | National acquisition rate, fraction |
| `larger_sample` | true if the brand has at least 50 seasoned loans |

## defaults-by-lender.csv

Charge-offs by lender. Charge-off rate for acquisition loans approved FY2018 to FY2021, lenders with at least 100 seasoned loans. Rows: 43. Online: https://sbaacquisitiondata.com/datasets/defaults-by-lender.csv

| Column | Meaning |
|---|---|
| `name` | Lender name as recorded by the SBA |
| `display_name` | Common name |
| `slug` | Lender URL slug (blank if no page) |
| `seasoned_loans` | Seasoned loans |
| `charged_off` | Loans with status CHGOFF |
| `charge_off_rate` | Fraction |
| `national_rate` | National acquisition rate, fraction |

## state-lenders-fy2026.csv

State lender rankings FY2026. Top 25 lenders by SBA 7(a) loans of any purpose in each state or territory in FY2026, with loans, dollars and the lender's acquisition share in that state. Rows: 1,274. Online: https://sbaacquisitiondata.com/datasets/state-lenders-fy2026.csv

| Column | Meaning |
|---|---|
| `state_code` | Two-letter postal code |
| `state_name` | State name |
| `rank` | Rank by 7(a) loans in the state in the fiscal year, 1 = most |
| `lender_name` | Lender name as recorded by the SBA |
| `display_name` | Common name used on the site |
| `lender_slug` | Lender page slug (blank if the lender has no page) |
| `loans` | SBA 7(a) loans of any purpose approved in FY2026, cancelled loans excluded |
| `dollars` | Gross approval of those loans, US dollars |
| `share_of_state_loans` | loans / all 7(a) loans in the state that fiscal year, as a fraction |
| `acquisition_loans` | Of those loans, the number recorded as a change of ownership |
| `acquisition_share` | acquisition_loans / loans, as a fraction |

## metro-lenders-fy2026.csv

Metro lender rankings FY2026. Top 25 lenders by SBA 7(a) loans of any purpose in each metro area in FY2026, with loans, dollars and the lender's acquisition share in that metro area. Rows: 375. Online: https://sbaacquisitiondata.com/datasets/metro-lenders-fy2026.csv

| Column | Meaning |
|---|---|
| `metro_slug` | Metro page slug; page is /metro/{metro_slug} |
| `metro_name` | Metro area name |
| `rank` | Rank by 7(a) loans in the metro area in the fiscal year, 1 = most |
| `lender_name` | Lender name as recorded by the SBA |
| `display_name` | Common name used on the site |
| `lender_slug` | Lender page slug (blank if the lender has no page) |
| `loans` | SBA 7(a) loans of any purpose approved in FY2026, cancelled loans excluded |
| `dollars` | Gross approval of those loans, US dollars |
| `share_of_metro_loans` | loans / all 7(a) loans in the metro area that fiscal year, as a fraction |
| `acquisition_loans` | Of those loans, the number recorded as a change of ownership |
| `acquisition_share` | acquisition_loans / loans, as a fraction |

## top-100-lenders-fy2026.csv

Top 100 lenders FY2026. The 100 lenders with the most SBA 7(a) loans of any purpose in FY2026: loans, dollars, average loan, acquisition share and Preferred Lenders Program share. Rows: 100. Online: https://sbaacquisitiondata.com/datasets/top-100-lenders-fy2026.csv

| Column | Meaning |
|---|---|
| `rank` | Rank by 7(a) loans in the fiscal year, 1 = most |
| `lender_name` | Lender name as recorded by the SBA |
| `display_name` | Common name used on the site |
| `lender_slug` | Lender page slug (blank if the lender has no page) |
| `home_state` | Most common bank state on the lender's loans |
| `loans` | SBA 7(a) loans of any purpose approved in FY2026, cancelled loans excluded |
| `dollars` | Gross approval of those loans, US dollars |
| `avg_loan` | dollars / loans, US dollars |
| `acquisition_loans` | Of those loans, the number recorded as a change of ownership |
| `acquisition_share` | acquisition_loans / loans, as a fraction |
| `plp_share` | Share of the loans processed under a Preferred Lenders Program method, as a fraction |
| `share_of_all_loans` | loans / all 7(a) loans approved in the fiscal year, as a fraction |

## naics-size-standards.csv

NAICS size standards with loan counts. SBA size standard (table in effect on the date shown on the NAICS page) beside acquisition loan counts, for each industry with a page. Rows: 300. Online: https://sbaacquisitiondata.com/datasets/naics-size-standards.csv

| Column | Meaning |
|---|---|
| `naics` | Six-digit NAICS 2022 code |
| `title` | Census NAICS title |
| `size_standard` | Size standard as text, for example "$8 million in average annual receipts" (blank if the code is not in the SBA table) |
| `size_basis` | receipts, employees or assets (blank if none) |
| `size_value` | Number in millions of dollars (receipts, assets) or employees |
| `acquisition_loans` | Acquisition loans, all approval years |
| `median_loan` | Median gross approval, US dollars |

## sba-franchise-directory.csv

SBA Franchise Directory. Every entry in the SBA Franchise Directory copy dated 2026-10-28 with acquisition loan counts (FY2018 to FY2026) and the page here, if the brand has one. Rows: 3,590. Online: https://sbaacquisitiondata.com/datasets/sba-franchise-directory.csv

| Column | Meaning |
|---|---|
| `brand` | Brand name as listed by the SBA |
| `sba_code` | SBA Franchise Identifier Code (blank if none) |
| `start_date` | Directory start date (blank if none) |
| `recertified_date` | Directory recertification date (blank if none) |
| `sba_note` | Note from the SBA file (blank if none) |
| `acquisition_loans` | SBA 7(a) loans recorded as a change of ownership under the code, all approval years in the file |
| `page` | Brand page on this site (blank if the brand has none) |
