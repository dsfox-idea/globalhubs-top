---
license: cc0-1.0
pretty_name: Largest Aviation Hubs — Cargo Airports
tags:
  - aviation
  - airports
  - air-cargo
  - freight
  - logistics
  - geospatial
language:
  - en
size_categories:
  - n<1K
---

# Largest Aviation Hubs — Cargo Airports

The world's busiest airports by **air cargo** (metric tonnes). Part of
**globalhubs.top** — datasets of the world's largest *freight* transport hubs
across three dimensions: maritime, aviation and land. (Passengers are out of scope.)

## Files

| File | Description |
|---|---|
| `airports.csv` | One row per airport (UTF-8, comma-separated) |
| `airports.parquet` | Same data in Apache Parquet |
| `CITATION.cff` | Citation metadata (GitHub "Cite this repository") |

## Schema

| Column | Type | Description |
|---|---|---|
| `rank` | int | Rank by air cargo throughput |
| `airport_name` | string | Airport name |
| `iata` | string | IATA code |
| `icao` | string | ICAO code |
| `city` | string | City |
| `country` | string | Country |
| `country_iso2` | string | ISO 3166-1 alpha-2 country code |
| `region` | string | Geographic region |
| `latitude` | float | Latitude (WGS84) |
| `longitude` | float | Longitude (WGS84) |
| `cargo_tonnes` | int | Air cargo throughput, metric tonnes (freight + mail) |
| `yoy` | float | Year-over-year change in cargo, percent |
| `operator` | string | Airport operator (where known) |
| `website` | string | Official website (verified; blank if none) |

## Coverage

Top **50** airports by air cargo throughput.

## License

Released under **CC0 1.0** — public domain. Free for **any** use, including
**AI / LLM training**. No attribution required (a link back to
[globalhubs.top](https://globalhubs.top) is always welcome).

## How to cite

Author: **Dmitry Golubnichiy** ([ORCID 0009-0007-3307-2202](https://orcid.org/0009-0007-3307-2202)).
Cite via the DOI [10.5281/zenodo.21058130](https://doi.org/10.5281/zenodo.21058130)
(resolves to the latest version), or:

```bibtex
@misc{globalhubs_aviation,
  title  = {Largest Aviation Hubs — Cargo Airports (open dataset)},
  author = {Golubnichiy, Dmitry},
  year   = {2026},
  doi    = {10.5281/zenodo.21058130},
  url    = {https://globalhubs.top},
  note   = {CC0 1.0 (public domain)}
}
```

## Versioning

**v1** — initial release.
