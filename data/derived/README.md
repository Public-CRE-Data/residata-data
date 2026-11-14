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
> **Correction, 2026-11-13 — AVB concessions restated back to 2026-03-31.**
> AVB tags its "select homes" offers on individual units; units without a tag
> get no discount on AVB's own site. Until this week the scraper gave every
> such unit the community-wide offer, so about half of AVB listings were
> recorded as discounted when they were not. AVB net effective rent (and VMRK,
> which includes it) is restated using Internet Archive snapshots of AVB
> community pages (Mar-Oct 2026) and live pages on 2026-11-13: units shown in a
> snapshot within 3 days are corrected exactly; the rest carry the offer
> weighted by their community's share of units with an offer of their own,
> interpolated between snapshots. AVB's average discount to asking falls from
> 7.4% -> 9.1% (Mar -> Nov, as published) to 3.6% -> 4.7%; the asking net
> effective index (Mar 28 = 100) moves from 95.6 to 96.2 in the week of
> 2026-11-14; gross rents are unchanged. Estimated weeks carry roughly +/-1.5
> pts uncertainty on the discount level (tested against the live pages). AVB's
> concession-share series still counts estimated rows as offering a
> concession. From 2026-11-20 the scraper records units' own offers only.
>
> **Correction, 2026-11-14 — UDR and MAA concessions restated back to 2026-03-31.**
> UDR and MAA, like AVB, attach many offers to individual units ("select
> apartments"); units without one get no discount on the REIT's own site.
> Until this week both scrapers gave every unit its community's offer, so on
> 2026-11-13 we recorded 91% of UDR and 75% of MAA listings as discounted
> against about 32% and 27% on the sites. Restated with the AVB method above
> (Internet Archive snapshots Mar-Oct 2026 plus live pages on 2026-11-13;
> where a unit's own offer text differs from the community's, it is re-parsed
> from its own text). Average discount to asking, first -> latest week:
> UDR 3.7% -> 4.4% as published, now 1.8% -> 2.7%; MAA 6.5% -> 6.4% as
> published, now 1.4% -> 2.6%. Because MAA's discounts were overstated most
> in the spring, its asking net effective index (Mar 28 = 100) moves from
> 99.5 to 98.2 in the week of 2026-11-14, below CPT (99.1); UDR moves from
> 100.4 to 100.4. Estimated weeks carry roughly +/-1 pt uncertainty on the
> discount level (tested against the live pages, both slightly understated).
> Also from this week, for all REITs: add-on offers that are not rent
> discounts (storage, parking, garages, amenity or package fees, e.g. UDR's
> "$44.99/month" package) are no longer counted as concessions, unless the
> offer also discounts rent; about 4,000 historical rows (UDR 2,700, AVB 660,
> ESS 420, EQR 170) are affected. Gross rents are unchanged. From 2026-11-20
> the UDR and MAA scrapers record units' own offers only.
>
> Also restated the same week. **CPT:** "$X OFF" banners whose fine print reads
> "Application and administrative fee credited at move-in" are fee credits, not
> rent discounts, and are no longer counted (26 of 70 CPT communities with
> offers on 2026-11-13; about 12,400 historical listing-weeks, classified from
> Internet Archive and live fine print; 9% of "$X OFF" offers had no fine print
> available and are still counted). CPT's average discount in the latest week
> falls from 3.5% to 3.2%. **ESS:** ESS shows one "Save up to $X" banner per
> community, limited in its fine print to select units, and its site data never
> says which units. Applying the full amount to every floor plan overstates the
> discount, so ESS discounts are now scaled to 41%: the share of "advertised
> amount x every unit" that units actually received on 2026-11-13 at the REITs
> whose sites do show unit-level offers (AVB 41%, MAA 41%, UDR 44%, pooled
> 41%). This is an estimate borrowed from other REITs, and leans high (units'
> own "up to" offers are still valued at their maximum); ESS's average
> discount falls from 3.2% to about 1.3% in the latest week,
> and changes in ESS concessions move its net effective series about half as
> much as before.
>
> **Method change, 2026-11-14 — new-lease index controls for unit size.**
> Within a building and bedroom count, the units that lease in a given week can
> be larger or smaller than usual, and ESS (which lists floor plans, not units)
> moved most on this. Each lease's rent is now restated to its cell's average
> size using the REIT's within-cell size elasticity (0.35-0.58, estimated on
> its whole portfolio and reused for every market). History is restated. New-lease
> net effective 4-week index, change since 2026-09-26, before -> after: ESS
> -3.3 -> -2.6, UDR +0.6 -> +0.1, INVH -3.0 -> -2.4, CPT -1.4 -> -0.9; other
> REITs within 0.4 pt. The listings index is unchanged.
>
> **Restored, 2026-11-14 — INVH new-lease history, April-July 2026.** Before
> 2026-08-01 the INVH scraper recorded a neighbouring home's price, so INVH was
> dropped before that date. The listings themselves were valid (which home,
> which weeks, beds, ZIP, lease term), so leases can still be identified; the
> new-lease index now prices them at each home's own rent from Internet Archive
> snapshots of its page, used only from the snapshot date and only where the
> snapshot was within 14 days of the home's last listed week, marked down by
> INVH's measured final-weeks markdown (-1.1% a week) for any staleness.
> Tested against correctly scraped rents on 2026-08-03 (same homes: median
> ratio 1.008 for snapshots within 30 days). About 30-220 leases a week before
> August (600-1,000 after), so read April-July as a trend. INVH's Aug-Nov
> values move by 0.2 pt or less; other REITs are unchanged. INVH's listings
> (asking) index still starts 2026-08-01: it needs every listed home's price
> every week, which the archive does not have.
>
> **Method change, 2026-11-05 — lease-term effects estimated REIT-wide.** The
> lease-term effect below is now estimated once per REIT, on its whole
> portfolio, and the same effects are applied to every market series. Fitting
> it market by market failed where a site switched every unit's term in the
> same week (INVH moved ~95-99% of homes in Las Vegas, Atlanta, Charlotte,
> Miami, Nashville and Phoenix to 18-23-month quotes the week of 2026-08-29):
> inside one market the term change and the price change cannot be separated.
> REIT totals are unchanged; market history is restated. Largest revisions
> (asking NER, Aug 1 -> Oct 31): INVH Las Vegas -8.5 pts, UDR Philadelphia
> -5.6, INVH Jacksonville +4.5, INVH Phoenix -3.4; new-lease 4-week: INVH
> Phoenix -6.8, CPT Austin -2.7, EQR Boston +2.5, INVH Atlanta +2.3.
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
