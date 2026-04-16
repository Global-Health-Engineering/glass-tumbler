# GENERAL INFORMATION

* Title of Dataset: Solar-Powered Glass Tumbling Efficiency Analysis
* Author Information:
    * Name: Emma Steinke
    * Institution: Global Health Engineering Lab, ETH Zürich
    * Email: steinkee@ethz.ch

* Date of data collection: October 2025 - February 2026
* Geographic location of data collection: Cape Maclear, Malawi 

# SHARING/ACCESS INFORMATION

* Licenses/restrictions placed on the data: CC-BY
* Was data derived from another source? Yes
    * If yes, list source(s): Solar Irradiance data sourced from Solcast API.

# DATA & FILE OVERVIEW

## File List:
* **glass_brightness.csv**: Raw data containing pixel brightness measurements for glass samples at various tumbling durations.
* **imperfections.csv**: Raw counts of physical imperfections across different glass batches and abrasive media.
* **irradiance_data_2024.csv**: Meteorological data including Global Horizontal Irradiance (GHI), cloud opacity, and air temperature for the year 2024.
* **derived_lifetime_costs.csv**: Calculated financial projections comparing the cost per 100kg of treated material over the system's lifetime.
* **glass_brightness_averages.csv**: Processed dataset providing the mean brightness values for each glass treatment category over time.
* **imperfections_averages.csv**: Processed dataset providing the average number of imperfections for each glass treatment category.
* **tumbler_start_260W.csv**: Start-up feasibility analysis for the tumbler using a single 260W solar panel configuration.
* **tumbler_start_520W.csv**: Start-up feasibility analysis for the tumbler using a dual 520W solar panel configuration.
* **tumbler_operational_stats.csv**: Yearly statistical distribution of daily operational runtimes for both the 260W and 520W power scenarios.

# METHODOLOGICAL INFORMATION
For a comprehensive breakdown of the experimental design, data collection protocols, and the theoretical framework supporting this study, please refer to the final master thesis report: **Development and Field Testing of a Solar-Powered Glass Tumbler for Waste Glass Processing in Cape Maclear, Malawi**.


## 1. Solar Panel Sizing and Operational Logic
The operational status for each hour ($S_{hr}$) was determined by comparing the available solar resource at Cape Maclear, Malawi, with the system's power demand. Local procurement in Blantyre identified 260 W panels as the standard available size. Consequently, the model evaluates the number of operational hours per day for both single (260 W) and dual (520 W) configurations using 2024 irradiance data.

**Operational Status Equation:**
$$S_{hr} = \begin{cases} 1 & \text{if } \left( \frac{G_{avail}}{1000} \right) \times P_{PV} \geq P_{peak} \\ 0 & \text{otherwise} \end{cases}$$

Where:
* **$G_{avail}$**: Hourly global horizontal irradiance ($W/m^2$).
* **$P_{PV}$**: Installed photovoltaic capacity (260 W or 520 W).
* **$P_{peak}$**: Required peak power for system operation (142.5 W).

A value of **1** indicates the solar resource is sufficient to meet the power demand, while **0** indicates a non-operational state.

## 2. Surface Clarity Analysis (Brightness/Fogginess)
Surface "fogginess" (the result of surface abrasion) was quantified through digital image processing. Post-tumbling, white glass samples were placed in a controlled-lighting environment in front of a black background and photographed.
* **Processing:** Square samples from the center of the glass piece were analyzed for mean pixel intensity.
* **Metric:** Values are expressed on a **Digital Number (DN)** scale from **0 to 255**. 
* **Interpretation:** Higher values (closer to 255) indicate a smoother, more reflective surface (polished), while lower values indicate a rougher, "foggier" surface caused by abrasive media.

## 3. Physical Integrity (Manual Imperfections)
To validate the efficacy of the abrasive media (Water, Sand, Silica Grit), a manual inspection protocol was established to count surface defects.
* **Sampling:** From each treatment batch, the **seven largest glass fragments** were selected for analysis.
* **Counting:** Each fragment was inspected for distinct physical imperfections such as conchoidal fractures. 
* **Averaging:** The final value represents the mean number of defects across those seven fragments per batch.

## 4. Total Cost of Ownership (Financial Analysis)
The financial viability of the system was modeled over its projected operational lifespan. The analysis accounts for both initial investment and recurring maintenance costs.
* **CAPEX (Capital Expenditure):** Costs associated with the solar panels, motor, structural frame, and tumbler drum.
* **OPEX (Operating Expenditure):** Maintenance requirements including scheduled applications of oil and grease for chain lubrication as well as labour costs. 
* **Normalization:** The final metric is calculated as the total lifetime cost divided by the total mass of glass processed, expressed in **USD per 100kg**.

## Instrument- or software-specific information needed to interpret the data: 
Image Processing: Python 3.11.5
Analysis Environment: Python 3.11.5 





