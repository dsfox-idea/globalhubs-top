---
license: cc0-1.0
pretty_name: Largest Air Cargo Carriers
tags:
  - aviation
  - air-cargo
  - cargo
  - carriers
  - logistics
  - transport
language:
  - en
size_categories:
  - n<1K
---

# Largest Air Cargo Carriers

The world's largest air cargo carriers, ranked by **cargo tonne-kilometres (CTK, 2024)** — the industry-standard air-cargo volume metric. Covers cargo airlines, combination carriers and express integrators, with HQ location and (where disclosed) tonnes and revenue.

Part of globalhubs.top — open datasets of the world's largest freight transport operators and hubs. Dedicated to the public domain (CC0 1.0); no attribution required (a credit to globalhubs.top is appreciated).

## Files

| File | Description |
|---|---|
| `carriers.csv` | One row per carrier (UTF-8, comma-separated) |
| `carriers.parquet` | Same data in Apache Parquet |
| `README.md` | This file |
| `CITATION.cff` | Citation metadata |

## Schema

| Column | Description |
|---|---|
| `rank` | Rank by 2024 cargo tonne-km (CTK) |
| `company` | Carrier |
| `category` | integrator | combination carrier | cargo airline |
| `parent_group` | Parent group / cargo brand context |
| `country` | HQ country |
| `country_iso2` | ISO 3166-1 alpha-2 code |
| `region` | Macro-region |
| `hq_city` | HQ city |
| `latitude` | HQ latitude (WGS84) |
| `longitude` | HQ longitude (WGS84) |
| `ctk_m` | Cargo tonne-kilometres, millions, 2024 — the ranking metric |
| `ctk_basis` | `IATA WATS 2024` | `carrier-disclosed` | `estimated` |
| `cargo_tonnes_k` | Freight tonnes carried, thousand (`n/d` if undisclosed) |
| `revenue_usd_m` | Disclosed cargo / segment revenue, USD millions (`n/d` if not disclosed) |
| `revenue_fy` | Fiscal year of the revenue figure |
| `website` | Official website |
| `source` | Data source (IATA WATS reproduction or carrier disclosure) |

## Notes

Ranking metric is **cargo tonne-kilometres (CTK)** for 2024. Ranks 1–26 are IATA WATS 2024 (reliable); ranks 27–50 are mostly **estimated** (tonnes × stage-length or revenue/yield proxies) — the `ctk_basis` column flags each row's provenance. Express integrators (FedEx, UPS) are included and flagged; their `revenue` is a segment/group figure, not air-cargo-only. No blank cells: undisclosed values are `n/d`.

## Citation

Golubnichiy, Dmitry. *Largest Air Cargo Carriers* (open dataset). globalhubs.top. DOI: [10.5281/zenodo.21115072](https://doi.org/10.5281/zenodo.21115072).

## License

Dedicated to the public domain under **CC0 1.0**. No attribution required; a credit to globalhubs.top is appreciated.
