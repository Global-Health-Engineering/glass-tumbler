# Derived Data

Datasets produced from [`../raw_data/`](../raw_data/) by analysis scripts. These feed the figures and tables in [`results.qmd`](../../results.qmd).

| File | Description | Derived from |
| :--- | :--- | :--- |
| `glass_brightness_averages.csv` | Mean pixel brightness per (abrasive medium × tumbling time) group. | `glass_brightness.csv` |
| `imperfections_averages.csv` | Mean imperfection count across the seven largest fragments per batch. | `imperfections.csv` |
| `tumbler_start_260W.csv` | Hourly binary indicator (0/1) of whether a single 260 W panel provides sufficient irradiance to start the motor, for each hour of 2024. | `irradiance_data_2024.csv` |
| `tumbler_start_520W.csv` | Same as above for a dual-panel 520 W configuration. | `irradiance_data_2024.csv` |
| `tumbler_operational_stats.csv` | Distribution of daily operational hours over the year, for the 260 W and 520 W scenarios. | `tumbler_start_260W.csv`, `tumbler_start_520W.csv` |
| `derived_lifetime_costs.csv` | Lifetime cost per 100 kg of tumbled glass under different assumed system lifetimes and panel configurations. | Cost model (see `../metadata/README.md`, §4). |

Variable definitions, units, and value ranges are documented in [`../metadata/codebook.csv`](../metadata/codebook.csv). Methodology is documented in [`../metadata/README.md`](../metadata/README.md).
