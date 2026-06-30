---
license: cc0-1.0
pretty_name: Largest Maritime Hubs — Container Ports
tags:
  - maritime
  - ports
  - shipping
  - logistics
  - geospatial
language:
  - en
size_categories:
  - n<1K
---

# Largest Maritime Hubs — Container Ports

The world's largest container seaports, ranked by container throughput (TEU).
Part of **globalhubs.top** — datasets of the world's largest transport hubs
across three dimensions: maritime, aviation and land.

## Files

| File | Description |
|---|---|
| `ports.csv` | One row per port (UTF-8, comma-separated) |
| `ports.parquet` | Same data in Apache Parquet |

## Schema

| Column | Type | Description |
|---|---|---|
| `rank` | int | Rank by container throughput |
| `port_name` | string | Port name |
| `country` | string | Country |
| `country_iso2` | string | ISO 3166-1 alpha-2 country code |
| `region` | string | Geographic region |
| `latitude` | float | Latitude (WGS84) |
| `longitude` | float | Longitude (WGS84) |
| `teu` | int | Container throughput in TEU (twenty-foot equivalent units) |
| `yoy` | float | Year-over-year change in throughput, percent |
| `operator` | string | Operating company / port authority (where known) |
| `website` | string | Official website (verified; blank if none) |

## Coverage

Top **50** container ports by container throughput. Cargo tonnage, vessel calls
and additional dimensions (aviation, land) are planned for future versions.

## License

Released under **CC0 1.0**. The dataset is an independently compiled,
normalized table; numeric throughput figures are facts.

## Versioning

**v1** — initial release.
