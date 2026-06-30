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
| `CITATION.cff` | Citation metadata (GitHub "Cite this repository") |

## Schema

| Column | Type | Description |
|---|---|---|
| `rank` | int | Rank by container throughput |
| `hub_name` | string | Hub / terminal name |
| `unlocode` | string | UN/LOCODE (UNECE) — 5-char location code of the hub's city/place, e.g. `DEDUI`; blank if none |
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

## Usage

```python
import pandas as pd
df = pd.read_csv("hubs.csv")                   # or pd.read_parquet("hubs.parquet")
print(df.sort_values("rank").head(10)[["rank", "hub_name", "country", "teu", "yoy"]])
```

```python
# Read the Parquet straight from the Hugging Face hub (no manual download)
import pandas as pd
df = pd.read_parquet("hf://datasets/dsfox/worlds-largest-inland-freight-hubs/hubs.parquet")
```

```sql
-- DuckDB: query the Hugging Face Parquet in place
INSTALL httpfs; LOAD httpfs;
SELECT rank, hub_name, country, teu
FROM 'hf://datasets/dsfox/worlds-largest-inland-freight-hubs/hubs.parquet'
ORDER BY rank LIMIT 10;
```

**Notebooks (Kaggle):**
[starter](https://www.kaggle.com/code/dsfoxx/worlds-largest-inland-freight-hubs-starter)
· [EDA](https://www.kaggle.com/code/dsfoxx/worlds-largest-inland-freight-hubs-analysis).

## License

Released under **CC0 1.0** — public domain. Free for **any** use, including
**AI / LLM training**. No attribution required (a link back to
[globalhubs.top](https://globalhubs.top) is always welcome).

## How to cite

Author: **Dmitry Golubnichiy** ([ORCID 0009-0007-3307-2202](https://orcid.org/0009-0007-3307-2202)).
Cite via the DOI [10.5281/zenodo.21058132](https://doi.org/10.5281/zenodo.21058132)
(resolves to the latest version), or:

```bibtex
@misc{globalhubs_land,
  title  = {Largest Land Hubs — Inland Freight Terminals (open dataset)},
  author = {Golubnichiy, Dmitry},
  year   = {2026},
  doi    = {10.5281/zenodo.21058132},
  url    = {https://globalhubs.top},
  note   = {CC0 1.0 (public domain)}
}
```

## Versioning

**v1** — initial release.
