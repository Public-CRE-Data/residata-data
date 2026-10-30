# Derived analysis series

> **Method change, 2026-10-19 — headline rent indices restated.**
> The `index_same_property_*`, `markets_*` and `market_comparison_*` series
> are now a **constant-mix rent index**: rents compared within the same
> building and bedroom count (same ZIP and bedroom count for single-family),
> all weeks estimated jointly. Full detail and the per-series index with
> sample sizes: `data/summary/rent_index_history.csv`.
>
> The previous method chained week-over-week changes on units listed in both
> weeks. With listings data that pool is the units that have *not* leased,
> which get marked down while cheaper units lease and leave; the chain
> recorded every cut and never the turnover, so it overstated rent declines by
> roughly 1.5-2 pts a month for every REIT (Apr-Oct 2026: index -4% to -11%
> while rents in the same buildings were roughly flat). **Figures taken from
> these files before 2026-10-19 overstate declines and should not be used.**
>
> Also corrected: INVH series start 2026-08-01 (before that its scraper
> recorded a neighbouring home's price; recovered history to follow);
> Richmond VA (MAA, UDR) and ESS Bay Area properties no longer mis-mapped
> (ESS had a spurious Denver series); market series with a typical week under
> 30 listings are no longer published. "Up to" concession offers (e.g. MAA's
> "up to one month of free base rent", a quarter of MAA listings by Oct 2026)
> are valued at their stated maximum, as "up to $X" offers already were; a
> click-through quote at MAA Addison Circle granted the full advertised amount.
> Offers with no stated amount at all ("check out our specials") are left out
> of net effective rent rather than counted as no concession. The `same_prop_*` week-over-week
> series in `summary_history.csv` are retained as a measure of price-cut
> activity on listed units, not of rent levels.
>
> **Method change, 2026-10-29 — lease-term adjustment.** AVB, CPT, EQR, UDR and
> INVH quote each unit at one lease term (10-24 months), and the term shown
> changes from week to week (INVH switched most homes from 12/24-month to
> 18-23-month quotes on 2026-08-29). Monthly rent differs by term, so the
> constant-mix and new-lease indices now include a lease-term effect and price
> every week at a constant term mix. History is restated. Largest revisions to
> the new-lease 4-week index (Aug 8 -> Oct 24): CPT +1.1 pts, INVH +1.0, EQR +0.6,
> VMRK +0.5, AVB +0.3, UDR -0.4. MAA and ESS sites give no term and AMH always
> shows 12 months, so those series are unchanged.

> **New series, 2026-10-19 — new-lease rent index.** `new_lease_ner_4wk_index_by_reit`
> and `new_lease_rent_4wk_index_by_reit` (4-week averages, 2026-08-08 = 100,
> history from 2026-03); weekly detail by REIT and market, with lease counts,
> in `data/summary/new_lease_index_history.csv`. Where the listings index above
> measures rents on everything advertised, this measures rents on units **as
> they lease**: a unit listed one week and gone the next is a lease, counted
> once at its last advertised rent, compared within the same building and
> bedroom count (ZIP and bedroom count for single-family). Communities
> completed or acquired since 2024-10 that are also listing an abnormal number
> of units (lease-ups) are excluded. Weeks spanning missed scrapes are bridged,
> with the stale last price adjusted for the typical final-weeks markdown
> (tested by deleting real weeks: within ~0.2-0.5 pt for a two-week gap). Each
> point in these 4-week files is dated by the end of its leasing week -- the
> scrape that showed the units gone -- so the latest point carries the latest
> scrape's date (`new_lease_index_history.csv` dates each week by its start,
> the last scrape the units were listed in). It tracks the trend in
> new-lease rents, not lease-over-lease growth (possible from 2027-03); a
> withdrawn unit is indistinguishable from a leased one; ESS lists floor plans,
> not units, so its series is the thinnest. Renamed communities (e.g. ESS
> TENTEN Downtown -> Skylux on Wilshire) are now merged in all series.


CSV exports of the computed series behind the analysis workbook. Regenerated
by `build_excel.py` on every weekly run and committed by `weekly_run.py`
(STEP 7), so the repo carries the numbers behind the charts, not just the raw
scrapes.

## Format

Long format, one row per (date, series):

| column | meaning |
|---|---|
| `date` | Saturday-anchored week |
| `series` | REIT ticker, or macro market, depending on the file |
| `value` | the computed figure |
| `interpolated` | `True` = not observed (see below) |

## interpolated

Four weeks were never scraped — 2026-06-27, 07-04, 07-11 and 07-25 — because
the weekly run did not fire. Listings are a live snapshot, so there is nothing
to back-fill from; those points are linearly interpolated between the nearest
observed weeks on each side.

`interpolated` is also `True` where a single REIT has no value in a week the
others do (scraper miss, coverage gap, or a scraper methodology break).

**Never cite an `interpolated=True` row as an observation.** Filter them out
for any analysis that depends on measured values.

Interpolation never extrapolates: a series with no observation on one side of
a gap is omitted rather than guessed.

## Files

- `same_prop_avg_rent` / `same_prop_avg_ner` — count-weighted same-property
  levels ($) by REIT
- `index_*` — chain-linked same-property indices (base 100)
- `charts_concession_rate` — share of listings carrying a concession, by REIT
- `new_lease_<ner|rent>_4wk_index_by_reit` — new-lease rent index, 4-week average (see top)
- `new_lease_ner_4wk_index_by_market` — the same by market and REIT, from 2026-08-08 (= 100); `thin` = under 60 leases a week; `interpolated` as below
- `markets_<reit>_*` — per-REIT index by macro market
- `market_comparison_<market>_*` — cross-REIT index within one market

Same-property = units present in BOTH consecutive weeks, matched on `unit_id`.
Indices are chain-linked on weekly factors, so a missing factor does not shift
the level.
