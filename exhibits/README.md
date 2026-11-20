# Apartment REIT exhibits: data and formulas

Excel-ready data behind 37 exhibits on Vivmark Residential (VMRK, the AvalonBay / Equity Residential merger) and its apartment REIT peers (ESS, UDR, CPT, MAA): portfolio profile, market exposure, merger synergies and overhead, neighborhood density and NOI margins, size, mergers and the cost of capital across REITs, development lease-ups, nearby supply and absorption, lease rates, and website-listing rent indices.

**Every result is a live Excel formula over the source data.** The `data/` files hold the inputs as values, each row labelled with the document it came from. The `sheets/` files hold the exhibits: every number in them is a formula over the data sheets (or over a small input block on the same sheet, also labelled by source). `images/` shows what each exhibit looks like once charted and formatted.

Snapshot: **2026-11-20**. Company data as of 3Q26 (September 30, 2026) unless stated; CoStar data pulled November 2026; FactSet data pulled November 19-20, 2026 (bond spreads to November 13, 2026); website listings scraped weekly from March 28, 2026 (indices shown through October 31, 2026).

Exhibit numbers follow the source document: Exhibits 34-46 are built from other providers' data and are not included.

## Exhibits

| Exhibit | What it shows | Formula sheet | Sheet name | Image |
|---|---|---|---|---|
| 1 | VMRK is the most urban, highest-quality and highest-rent apartment REIT | [`ex01_portfolio_profile.tsv`](sheets/ex01_portfolio_profile.tsv) | **Ex01** | [image](images/exhibit_01.png) |
| 2 | VMRK is spread across both coasts and dominant in the Northeast | [`ex02_market_shares.tsv`](sheets/ex02_market_shares.tsv) | **Ex02** | [image](images/exhibit_02.png) |
| 3 | Northern California leads 3Q26 same-store revenue growth; the Mid-Atlantic and Denver lag | [`ex03_region_revenue_growth.tsv`](sheets/ex03_region_revenue_growth.tsv) | **Ex03** | [image](images/exhibit_03.png) |
| 4 | We test three of five claims: synergies, density and cost of capital | [`ex04_merger_claims.tsv`](sheets/ex04_merger_claims.tsv) | **Ex04** | [image](images/exhibit_04.png) |
| 5 | Overhead is $115mn of the $135mn net synergy target | [`ex05_synergy_bridge.tsv`](sheets/ex05_synergy_bridge.tsv) | **Ex05** | [image](images/exhibit_05.png) |
| 6 | Synergies ramp mostly through 2027 | [`ex06_synergy_ramp.tsv`](sheets/ex06_synergy_ramp.tsv) | **Ex06** | [image](images/exhibit_06.png) |
| 7 | In 2027, tax reassessment and merger financing absorb synergy capture | [`ex07_fy27_synergy_bridge.tsv`](sheets/ex07_fy27_synergy_bridge.tsv) | **Ex07** | [image](images/exhibit_07.png) |
| 8 | By 2028, full synergy capture adds about $80mn net | [`ex08_fy28_synergy_bridge.tsv`](sheets/ex08_fy28_synergy_bridge.tsv) | **Ex08** | [image](images/exhibit_08.png) |
| 9 | Past apartment mergers cut G&A; VMRK’s $50mn target is within that range | [`ex09_ga_after_mergers.tsv`](sheets/ex09_ga_after_mergers.tsv) | **Ex09** | [image](images/exhibit_09.png) |
| 10 | VMRK’s 2027 property-management cut is within past mergers’ range | [`ex10_property_mgmt_after_mergers.tsv`](sheets/ex10_property_mgmt_after_mergers.tsv) | **Ex10** | [image](images/exhibit_10.png) |
| 11 | Hitting the target would make VMRK the leanest operator in the group | [`ex11_overhead_ratio_fy2025.tsv`](sheets/ex11_overhead_ratio_fy2025.tsv) | **Ex11** | [image](images/exhibit_11.png) |
| 12 | Larger REITs carry less overhead; VMRK’s target fits its size | [`ex12_overhead_vs_size.tsv`](sheets/ex12_overhead_vs_size.tsv) | **Ex12** | [image](images/exhibit_12.png) |
| 13 | VMRK’s communities sit as close together as ESS’s, much closer than others | [`ex13_nearest_sister.tsv`](sheets/ex13_nearest_sister.tsv) | **Ex13** | [image](images/exhibit_13.png) |
| 14 | Counting communities, VMRK leads ESS by 1.3x and others by 4.5x | [`ex14_sister_communities.tsv`](sheets/ex14_sister_communities.tsv) | **Ex14** | [image](images/exhibit_14.png) |
| 15 | ESS and VMRK cluster most; most UDR, CPT, MAA communities stand alone | [`ex15_cluster_size.tsv`](sheets/ex15_cluster_size.tsv) | **Ex15** | [image](images/exhibit_15.png) |
| 16 | Within the same market, denser REITs do not earn higher margins | [`ex16_margin_vs_density.tsv`](sheets/ex16_margin_vs_density.tsv) | **Ex16** | [image](images/exhibit_16.png) |
| 17 | In most mergers, markets with biggest density gains lagged on NOI margins | [`ex17_merger_gap.tsv`](sheets/ex17_merger_gap.tsv) | **Ex17** | [image](images/exhibit_17.png) |
| 18 | Six ways of testing it: no detectable density margin benefit | [`ex18_six_density_margin_tests.tsv`](sheets/ex18_six_density_margin_tests.tsv) | **Ex18** | [image](images/exhibit_18.png) |
| 19 | Large caps have outperformed since 2021; among REITs, mainly since 2025 | [`ex19_large_caps_vs_rest.tsv`](sheets/ex19_large_caps_vs_rest.tsv) | **Ex19** | [image](images/exhibit_19.png) |
| 20 | The largest REITs in each property type trade at a premium | [`ex20_pffo_by_size_fifth.tsv`](sheets/ex20_pffo_by_size_fifth.tsv) | **Ex20** | [image](images/exhibit_20.png) |
| 21 | After REIT stock mergers, acquirers’ multiples lagged their peers | [`ex21_acquirer_pffo_after_mergers.tsv`](sheets/ex21_acquirer_pffo_after_mergers.tsv) | **Ex21** | [image](images/exhibit_21.png) |
| 22 | VMRK’s bond edge over peers is tracking its pre-deal trend | [`ex22_vmrk_bond_spread_vs_peers.tsv`](sheets/ex22_vmrk_bond_spread_vs_peers.tsv) | **Ex22** | [image](images/exhibit_22.png) |
| 23 | Most of VMRK’s pipeline is next door to existing communities | [`ex23_pipeline_adjacency.tsv`](sheets/ex23_pipeline_adjacency.tsv) | **Ex23** | [image](images/exhibit_23.png) |
| 24 | Almost half the units under construction are in Sunbelt expansion markets | [`ex24_units_under_construction.tsv`](sheets/ex24_units_under_construction.tsv) | **Ex24** | [image](images/exhibit_24.png) |
| 25 | VMRK has the largest development book relative to its size | [`ex25_development_vs_ev.tsv`](sheets/ex25_development_vs_ev.tsv) | **Ex25** | [image](images/exhibit_25.png) |
| 26 | Current lease-ups are running behind AvalonBay’s past projects | [`ex26_leaseup_vs_history.tsv`](sheets/ex26_leaseup_vs_history.tsv) | **Ex26** | [image](images/exhibit_26.png) |
| 27 | Most lease-ups trail history, and expansion markets are cutting rents | [`ex27_leaseups_now.tsv`](sheets/ex27_leaseups_now.tsv) | **Ex27** | [image](images/exhibit_27.png) |
| 28 | Next lease-ups lean to expansion markets; Lake Norman shows the risk | [`ex28_next_leaseups.tsv`](sheets/ex28_next_leaseups.tsv) | **Ex28** | [image](images/exhibit_28.png) |
| 29 | Overall, VMRK’s radial supply should remain relatively modest over the next 12 months | [`ex29_nearby_supply_uncaptured.tsv`](sheets/ex29_nearby_supply_uncaptured.tsv) | **Ex29** | [image](images/exhibit_29.png) |
| 30 | Next 12 months: supply edges up slightly near VMRK (driven by legacy EQR) | [`ex30_ntm_minus_ttm_by_company.tsv`](sheets/ex30_ntm_minus_ttm_by_company.tsv) | **Ex30** | [image](images/exhibit_30.png) |
| 31 | Supply rises (from low levels) near VMRK’s Seattle, Boston and Northern California communities | [`ex31_supply_by_region.tsv`](sheets/ex31_supply_by_region.tsv) | **Ex31** | [image](images/exhibit_31.png) |
| 32 | Heavy nearby supply/preleasing leads to relative rent growth underperformance vs peers | [`ex32_lease_rates_vs_supply_timing.tsv`](sheets/ex32_lease_rates_vs_supply_timing.tsv) | **Ex32** | [image](images/exhibit_32.png) |
| 33 | Last year’s absorption about matches next year’s nearby supply near VMRK | [`ex33_absorption_vs_nearby_supply.tsv`](sheets/ex33_absorption_vs_nearby_supply.tsv) | **Ex33** | [image](images/exhibit_33.png) |
| 47 | VMRK’s listed rents have softened more than most peers since March | [`ex47_listed_rent_index.tsv`](sheets/ex47_listed_rent_index.tsv) | **Ex47** | [image](images/exhibit_47.png) |
| 48 | On units as they lease, VMRK’s rents are in line with peers | [`ex48_new_lease_rent_index.tsv`](sheets/ex48_new_lease_rent_index.tsv) | **Ex48** | [image](images/exhibit_48.png) |
| 49 | The softness sits in legacy AVB communities | [`ex49_legacy_rent_index.tsv`](sheets/ex49_legacy_rent_index.tsv) | **Ex49** | [image](images/exhibit_49.png) |
| 50 | Legacy AVB fell 4–7% since March in every major market but NY | [`ex50_legacy_avb_by_market.tsv`](sheets/ex50_legacy_avb_by_market.tsv) | **Ex50** | [image](images/exhibit_50.png) |

## Data sheets

| Sheet name | What it holds | File(s) and paste cell |
|---|---|---|
| **Company** | Fiscal-year G&A, property management and property revenue by REIT (10-K) | [`company_financials.tsv`](data/company_financials.tsv) → **A1** |
| **Communities** | One row per REIT community (CoStar), with computed distance measures | [`communities.tsv`](data/communities.tsv) → **A1** |
| **Margins2025** | FY2025 same-store NOI margin by REIT and market, with density | [`margins_2025.tsv`](data/margins_2025.tsv) → **A1** |
| **Pairs** | Pairs of REITs with a similar urban/suburban mix in the same market | [`pairs_urban_mix.tsv`](data/pairs_urban_mix.tsv) → **A1** |
| **HistPanel** | REIT-market-year panel for the within-company test | [`hist_panel_2012_2025.tsv`](data/hist_panel_2012_2025.tsv) → **A1** |
| **Windows** | Three-year windows: large footprint changes vs stable markets | [`windows_three_year.tsv`](data/windows_three_year.tsv) → **A1** |
| **Mergers** | Acquirer markets around four past apartment mergers | [`mergers_four_deals.tsv`](data/mergers_four_deals.tsv) → **A1** |
| **LeaseUp** | Development communities by supplement quarter, AvalonBay 2012-2026 and VMRK 3Q26 | [`leaseup_panel.tsv`](data/leaseup_panel.tsv) → **A1** |
| **Listings** | Unit-level summary of weekly website listings for communities in lease-up | [`listings_units.tsv`](data/listings_units.tsv) → **A1** |
| **NOIMix** | Share of 3Q26 same-store NOI by reporting region (%) | [`noi_mix_by_region.tsv`](data/noi_mix_by_region.tsv) → **A1** |
| **Supply** | Nearby deliveries by month for each REIT community (equal-stock radius) | [`supply_by_community_part1.tsv`](data/supply_by_community_part1.tsv) → **A1**; [`supply_by_community_part2.tsv`](data/supply_by_community_part2.tsv) → **A545**; [`supply_by_community_part3.tsv`](data/supply_by_community_part3.tsv) → **A1094** |
| **CoStarMarkets** | CoStar net deliveries and inventory by submarket and quarter | [`costar_submarkets.tsv`](data/costar_submarkets.tsv) → **A1** |
| **LeaseTest** | EQR minus UDR lease rates by UDR region and quarter, with relative nearby supply | [`lease_test_panel.tsv`](data/lease_test_panel.tsv) → **A1** |
| **Absorption** | CoStar net absorption and inventory by submarket, 4Q25-3Q26 | [`costar_submarket_absorption.tsv`](data/costar_submarket_absorption.tsv) → **A1** |
| **RentIndex** | Weekly website-listing rent indices by REIT and market (scraper output) | [`listing_rent_indices.tsv`](data/listing_rent_indices.tsv) → **A1** |
| **PFFOPanel** | Forward P/FFO, market value and forward FFO by REIT-quarter, 2004-26 (FactSet) | [`pffo_panel_2004_2026_part1.tsv`](data/pffo_panel_2004_2026_part1.tsv) → **A1**; [`pffo_panel_2004_2026_part2.tsv`](data/pffo_panel_2004_2026_part2.tsv) → **A1187**; [`pffo_panel_2004_2026_part3.tsv`](data/pffo_panel_2004_2026_part3.tsv) → **A2309**; [`pffo_panel_2004_2026_part4.tsv`](data/pffo_panel_2004_2026_part4.tsv) → **A3431**; [`pffo_panel_2004_2026_part5.tsv`](data/pffo_panel_2004_2026_part5.tsv) → **A4554**; [`pffo_panel_2004_2026_part6.tsv`](data/pffo_panel_2004_2026_part6.tsv) → **A5669** |
| **REITReturns** | REIT quarterly total returns and starting market values, 2004-26 (FactSet) | [`reit_quarterly_total_returns_part1.tsv`](data/reit_quarterly_total_returns_part1.tsv) → **A1**; [`reit_quarterly_total_returns_part2.tsv`](data/reit_quarterly_total_returns_part2.tsv) → **A5544** |
| **ETFReturns** | SPY, RSP, IWB and IWM quarterly total returns (FactSet) | [`etf_quarterly_total_returns.tsv`](data/etf_quarterly_total_returns.tsv) → **A1** |
| **Bonds** | Senior-note spreads by date for VMRK and the comparison REITs (FactSet) | [`bond_spreads_core_issuers_part1.tsv`](data/bond_spreads_core_issuers_part1.tsv) → **A1**; [`bond_spreads_core_issuers_part2.tsv`](data/bond_spreads_core_issuers_part2.tsv) → **A2042**; [`bond_spreads_core_issuers_part3.tsv`](data/bond_spreads_core_issuers_part3.tsv) → **A4058** |

## How to rebuild the exhibits in Excel

Excel 365 or Excel 2021 recommended (the sheets use MAXIFS, MINIFS, LINEST, EDATE and array formulas).

1. Open a new, blank workbook. **First create every sheet**, with the names in bold above, exactly as written (the 19 data sheets and the 37 exhibit sheets). Creating all sheets before pasting avoids Excel asking for missing files, because several sheets refer to each other.
2. **Data sheets:** open each file on GitHub, click **Raw**, press **Ctrl+A** then **Ctrl+C**, click the paste cell listed above on the matching sheet and press **Ctrl+V**. Files split into parts go into the same sheet, each part at its own start row.
3. **Exhibit sheets:** paste each `sheets/` file into cell **A1** of its sheet. Every cell calculates from the data sheets.
4. If cells show text such as `=SUMIFS(...)` instead of numbers, select the column, choose **Data → Text to Columns → Finish** (Excel then reads them as formulas).
5. Chart the columns named in each sheet's header row and compare with the image. Format share columns as **%** where they show decimals. Columns marked 'date serial' are Excel dates: format them as dates.
6. **Excel 2019 or earlier:** cells that use MEDIAN(IF(...)) (the PFFOPanel median column, Exhibit 21 and others) or INDEX/MATCH on two conditions are array formulas: click the cell, press **F2**, then **Ctrl+Shift+Enter**.

Calculation can take a few minutes after the Supply, PFFOPanel and LeaseUp sheets are pasted. Every exhibit cell was checked against the published value by recalculating this pack in LibreOffice (2,182 cells, all within rounding).

## What is an input and what is computed

- **Inputs (values):** figures as reported in company filings and presentations, CoStar property, building and market exports, FactSet prices, valuations, total returns and bond spreads, US Census data and weekly listings scraped from company websites. Each row names its source.
- **Computed inputs, marked `[computed]` in the column header:** measures that need geography or a large statistical step and are not practical as spreadsheet formulas. They are produced by script from the inputs beside them:
  - distances and counts of sister communities (straight-line, from CoStar latitude and longitude, earth radius 3,958.8 miles);
  - each community's equal-stock radius (the circle around it that holds about 10,300 units of Census ACS 2020-24 stock in buildings of 20+ units, 0.5 to 8 miles) and the units in that stock;
  - monthly deliveries inside each radius from the CoStar building list (buildings of 20+ units delivering 2023-2027; dates adjusted for typical delays; large buildings spread over their lease-up at about 50 units a month; senior housing and for-sale condominiums excluded). The 'incl. uncaptured' columns multiply Sunbelt deliveries from November 2026 by 1.30, the ratio of landed to forecast Sunbelt supply in CoStar's January 2026 forecast for 1Q-3Q26;
  - the relative-supply ratio in the lease test (ln of EQR's to UDR's nearby trailing-12-month deliveries in each UDR region, weighting EQR's markets by UDR's units);
  - margins and footprint flags after removing fixed effects in the within-company and three-year-window tests (REIT-market, market-year and REIT-year effects; the window test weighted by units).
- **Website rent indices (RentIndex):** the scraper's weekly constant-mix, same-property indices, published in `data/derived` of this repository; the exhibit sheets look them up and difference them.
- **Formulas:** everything else, including all ratios, weights, medians, ranks and size fifths, cap-weighted returns, regressions (TREND, LINEST), standard errors and every exhibit cell.

## Definitions

- **Units:** apartment units; operating communities only unless stated. Joint ventures at 100%.
- **Legacy AVB / EQR:** VMRK communities by pre-merger owner.
- **Sister community:** another operating community owned by the same REIT (legacy rows: the same pre-merger company).
- **NOI margin tests:** same-store NOI / revenue by REIT and market from company reporting. 'Per doubling' coefficients are the slope on ln density x ln(2), in basis points.
- **Lease-up:** AvalonBay development tables 2012-2026 and VMRK 3Q26; quarters since first occupancy use each project's latest reported first-occupancy quarter.
- **Nearby supply:** deliveries inside each community's equal-stock radius as % of local stock (Census 20+ unit stock plus deliveries January 2024 to October 2026); REITs weighted by same-store NOI mix by region, units within a region.
- **Absorption (Exhibit 33):** CoStar net absorption 4Q25-3Q26 over 3Q25 inventory in each community's own CoStar submarket, with the same community weights.
- **Relative P/FFO (Exhibits 20-21):** forward P/FFO over the median of the other REITs of the same property type that quarter (3+ others; P/FFO 5-60x). Size = forward FFO in $ (market value / P/FFO).
- **Large caps (Exhibit 19):** each quarter, the 10 largest REITs by equity market value vs the rest, cap-weighted next-quarter total returns; towers, data centres and other converted REITs from their REIT election.
- **Bond spreads (Exhibit 22):** spread to the benchmark Treasury on USD senior notes; each date, spread on years to maturity, its square and issuer effects; VMRK = ERP and legacy AVB notes.

## Sources

- SEC EDGAR: 10-K filings FY2012-FY2025 and quarterly earnings releases and supplementals of AvalonBay, Equity Residential, Vivmark Residential, Essex, UDR, Camden and Mid-America; 10-Ks of Colonial Properties, BRE Properties and Post Properties; merger filings for deal dates; free-writing prospectus term sheets for note CUSIPs and currencies.
- Company presentations: AvalonBay / Equity Residential merger presentation and call (May 21, 2026); VMRK 3Q26 earnings presentation; AvalonBay 1Q26, Equity Residential March 2026, Camden June 2026 and MAA 1Q26 investor updates.
- CoStar: REIT-owned property exports, building-level supply list and multifamily submarket statistics (pulled November 2026).
- FactSet: REIT forward P/FFO, FFO estimates, market values, shares and quarterly total returns (2004-26); ETF total returns (SPY, RSP, IWB, IWM); bond spreads.
- US Census Bureau: ACS 2020-24 (B25024 units in structure), ACS 2019-23 and ZCTA land area.
- Company websites: weekly listings scraped from REIT websites (see `data/raw` and `data/derived` in this repository).

## Caveats

- CoStar and FactSet figures are as exported and may be revised; some property attributes and FactSet histories have gaps (REITs that failed or delisted without a deal, and a few acquired REITs, are missing).
- Margin tests rely on market-level averages and few companies; none of the estimates is statistically distinguishable from zero.
- Lease-up history ends when projects leave the development table, usually about two quarters after first occupancy for expansion-market projects.
- Not investment advice. Data is compiled from public and licensed sources and may contain errors.
