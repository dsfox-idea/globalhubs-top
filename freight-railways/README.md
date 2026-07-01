---
license: cc0-1.0
pretty_name: Largest Freight Railways
tags:
  - rail
  - freight
  - railways
  - carriers
  - logistics
  - transport
language:
  - en
size_categories:
  - n<1K
---

# Largest Freight Railways

The world's largest freight railways, ranked by **net freight tonne-kilometres** — the UIC/ITF standard for rail-freight scale. Road haulage is out of scope (no comparable per-company volume metric). Includes HQ location, tonnes and indicative revenue.

Part of globalhubs.top — open datasets of the world's largest freight transport operators and hubs. Dedicated to the public domain (CC0 1.0); no attribution required (a credit to globalhubs.top is appreciated).

## Files

| File | Description |
|---|---|
| `railways.csv` | One row per railway (UTF-8, comma-separated) |
| `railways.parquet` | Same data in Apache Parquet |
| `README.md` | This file |
| `CITATION.cff` | Citation metadata |

## Schema

| Column | Description |
|---|---|
| `rank` | Rank by net freight tonne-km |
| `company` | Rail freight operator |
| `country` | HQ country |
| `country_iso2` | ISO 3166-1 alpha-2 code |
| `region` | Macro-region |
| `hq_city` | HQ city |
| `latitude` | HQ latitude (WGS84) |
| `longitude` | HQ longitude (WGS84) |
| `net_tkm_bn` | Net freight tonne-kilometres, billions — the ranking metric |
| `tonnes_mt` | Freight tonnes originated/carried, million (`n/d` if undisclosed) |
| `year` | Data year (fiscal where noted) |
| `revenue_usd_m` | Indicative freight/operator revenue, USD millions (`n/d` if not clean) |
| `website` | Official website |
| `source` | Data source |

## Notes

Ranking metric is **net freight tonne-kilometres** (UIC/ITF standard). US & Canadian Class I figures are converted from short-ton-miles (×1.45997). This is a **rail-only** list — road/trucking has no comparable per-company cargo-volume metric. Operators that publish only tonnes or stale tonne-km (e.g. Transnet, ČD Cargo, Iran, Egypt) are excluded. There are not 50 sizeable freight railways worldwide, so the list is ~30. Revenue is indicative (mixed net-freight vs group basis). Undisclosed values are `n/d`.

## Citation

Golubnichiy, Dmitry. *Largest Freight Railways* (open dataset). globalhubs.top. DOI: [10.5281/zenodo.21115074](https://doi.org/10.5281/zenodo.21115074).

## License

Dedicated to the public domain under **CC0 1.0**. No attribution required; a credit to globalhubs.top is appreciated.
