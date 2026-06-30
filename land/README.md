---
license: cc0-1.0
pretty_name: Largest Land Hubs — Inland Freight Terminals
tags:
  - rail
  - intermodal
  - dry-port
  - inland-port
  - freight
  - logistics
  - geospatial
language:
  - en
size_categories:
  - n<1K
---

# Largest Land Hubs — Inland Freight Terminals

The world's largest inland freight hubs — **dry ports and rail intermodal
terminals** — ranked by container throughput (TEU). Part of **globalhubs.top**,
datasets of the world's largest *freight* transport hubs across maritime,
aviation and land. (Passengers are out of scope.)

## Files

| File | Description |
|---|---|
| `hubs.csv` | One row per hub (UTF-8, comma-separated) |
| `hubs.parquet` | Same data in Apache Parquet |

## Schema

| Column | Type | Description |
|---|---|---|
| `rank` | int | Rank by container throughput |
| `hub_name` | string | Hub / terminal name |
| `city` | string | City |
| `country` | string | Country |
| `country_iso2` | string | ISO 3166-1 alpha-2 country code |
| `region` | string | Geographic region |
| `latitude` | float | Latitude (WGS84, city-level) |
| `longitude` | float | Longitude (WGS84, city-level) |
| `teu` | int | Container throughput (TEU) |
| `yoy` | float | Year-over-year change, percent (where available) |
| `operator` | string | Operating company (where known) |
| `website` | string | Official website (verified; blank if none) |

## Coverage & caveats

Top **50** inland freight hubs by container throughput. Unlike seaports and
airports, inland terminals report on **inconsistent bases** (handled TEU,
intermodal lifts, or design capacity) and reporting years differ, so ranks are
indicative rather than strictly comparable. Pure border crossings are excluded.

## License

Released under **CC0 1.0**. Independently compiled, normalized table.

## Versioning

**v1** — initial release.
