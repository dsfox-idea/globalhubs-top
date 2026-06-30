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
| `CITATION.cff` | Citation metadata (GitHub "Cite this repository") |

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

## Usage

```python
import pandas as pd
df = pd.read_csv("ports.csv")                 # or pd.read_parquet("ports.parquet")
print(df.sort_values("rank").head(10)[["rank", "port_name", "country", "teu", "yoy"]])
```

```python
# Read the Parquet straight from the Hugging Face hub (no manual download)
import pandas as pd
df = pd.read_parquet("hf://datasets/dsfox/worlds-largest-container-ports/ports.parquet")
```

```sql
-- DuckDB: query the Hugging Face Parquet in place
INSTALL httpfs; LOAD httpfs;
SELECT rank, port_name, country, teu
FROM 'hf://datasets/dsfox/worlds-largest-container-ports/ports.parquet'
ORDER BY rank LIMIT 10;
```

**Notebooks (Kaggle):**
[starter](https://www.kaggle.com/code/dsfoxx/worlds-largest-container-ports-starter)
· [EDA](https://www.kaggle.com/code/dsfoxx/worlds-largest-container-ports-eda).

## License

Released under **CC0 1.0** — public domain. Free for **any** use, including
**AI / LLM training**. No attribution required (a link back to
[globalhubs.top](https://globalhubs.top) is always welcome).

## How to cite

Author: **Dmitry Golubnichiy** ([ORCID 0009-0007-3307-2202](https://orcid.org/0009-0007-3307-2202)).
Cite via the DOI [10.5281/zenodo.21058128](https://doi.org/10.5281/zenodo.21058128)
(resolves to the latest version), or:

```bibtex
@misc{globalhubs_maritime,
  title  = {Largest Maritime Hubs — Container Ports (open dataset)},
  author = {Golubnichiy, Dmitry},
  year   = {2026},
  doi    = {10.5281/zenodo.21058128},
  url    = {https://globalhubs.top},
  note   = {CC0 1.0 (public domain)}
}
```

## Versioning

**v1** — initial release.
