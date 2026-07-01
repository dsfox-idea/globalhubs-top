---
license: cc0-1.0
pretty_name: Largest Container Shipping Lines
tags:
  - maritime
  - shipping
  - container
  - carriers
  - logistics
  - transport
language:
  - en
size_categories:
  - n<1K
---

# Largest Container Shipping Lines

The world's largest ocean container shipping lines, ranked by **operated fleet capacity (TEU)** — the industry-standard scale metric. Includes HQ location, fleet size, market share, consolidated brands, and (where the carrier discloses it) revenue.

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
| `rank` | Rank by operated fleet capacity (TEU) |
| `company` | Carrier (operating group) |
| `country` | HQ country |
| `country_iso2` | ISO 3166-1 alpha-2 code |
| `region` | Macro-region |
| `hq_city` | HQ city |
| `latitude` | HQ latitude (WGS84) |
| `longitude` | HQ longitude (WGS84) |
| `teu_capacity_k` | Operated capacity, thousand TEU — the ranking metric (Alphaliner snapshot) |
| `ships` | Operated vessels |
| `market_share_pct` | Share of world container fleet, % |
| `brands` | Subsidiary/absorbed carrier brands consolidated under this group (`none` if none) |
| `revenue_usd_m` | Latest disclosed revenue, USD millions (`n/d` = private / not disclosed) |
| `revenue_fy` | Fiscal year of the revenue figure |
| `website` | Official website |
| `source` | Ranking source (Alphaliner public Top 100) |

## Notes

Ranking metric is **operated fleet capacity (TEU)** from the Alphaliner public Top 100 (snapshot 2026-07-01) — the standard for "largest carriers"; note this is capacity, not throughput (which few carriers disclose). Subsidiaries stay **consolidated** under the operating parent (industry convention); the `brands` column lists the composition. MSC is #1 but privately held, so its revenue is `n/d`. No blank cells: undisclosed secondary values are `n/d`.

## Citation

Golubnichiy, Dmitry. *Largest Container Shipping Lines* (open dataset). globalhubs.top. DOI: [10.5281/zenodo.21115066](https://doi.org/10.5281/zenodo.21115066).

## License

Dedicated to the public domain under **CC0 1.0**. No attribution required; a credit to globalhubs.top is appreciated.
