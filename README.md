# globalhubs.top — open datasets

Open, well-documented datasets of the world's largest **freight** transport hubs,
across three dimensions. Passengers are out of scope. Site: https://globalhubs.top · License: CC0 1.0.

| Dimension | Folder | Ranked by |
|---|---|---|
| Maritime — largest container ports | [`maritime/`](./maritime) | container throughput (TEU) |
| Aviation — busiest cargo airports | [`aviation/`](./aviation) | air cargo (tonnes) |
| Land — largest inland freight hubs | [`land/`](./land) | container throughput (TEU) |

Each folder holds a CSV + Parquet (top-50) and a README with the schema.
Every row carries country, coordinates, the ranking metric, year-over-year change,
and — where verified — the operator and official website.

## How to cite

Author: **Dmitry Golubnichiy** ([ORCID 0009-0007-3307-2202](https://orcid.org/0009-0007-3307-2202)).
Each dataset has its own Zenodo DOI (see `CITATION.cff` here and per folder):
maritime [10.5281/zenodo.21058128](https://doi.org/10.5281/zenodo.21058128),
aviation [10.5281/zenodo.21058130](https://doi.org/10.5281/zenodo.21058130),
land [10.5281/zenodo.21058132](https://doi.org/10.5281/zenodo.21058132). Released under CC0 1.0.
