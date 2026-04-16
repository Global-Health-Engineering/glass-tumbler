# Raw Data

Unprocessed measurements from field trials and external sources. These files are the authoritative inputs to everything in [`../derived_data/`](../derived_data/).

| File | Description | Source |
| :--- | :--- | :--- |
| `glass_brightness.csv` | Pixel-brightness measurements of individual tumbled glass samples across durations and abrasive media. | Digital image processing of photographs taken under controlled lighting. |
| `imperfections.csv` | Manual counts of surface imperfections on the seven largest glass fragments per batch. | Visual inspection of post-tumbling fragments. |
| `irradiance_data_2024.csv` | Hourly Global Horizontal Irradiance (GHI), cloud opacity, and air temperature for Cape Maclear, Malawi, throughout 2024. | [Solcast API](https://solcast.com/). |

Variable definitions, units, and value ranges are documented in [`../metadata/codebook.csv`](../metadata/codebook.csv).

## Conventions

- Timestamps in `irradiance_data_2024.csv` are UTC (ISO 8601), matching the Solcast export.
- Tumbling durations (`time_h`, `Hours`) are whole hours from batch start.
- Do not modify files in this directory — analyses should read from here and write to `../derived_data/`.
