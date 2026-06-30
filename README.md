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
