# Data: Global Data on Sustainable Energy (2000-2020)

🌏⚡Explore 20-year Insights on Sustainable Energy⚡🌏

## File

| File | Size | Description |
|------|------|-------------|
| `global-data-on-sustainable-energy (1).csv` | 502 KB | — |

## Download

```bash
kaggle datasets download -d anshtanwar/global-data-on-sustainable-energy -p data --unzip
```

```python
from kaggle.api.kaggle_api_extended import KaggleApi
api = KaggleApi(); api.authenticate()
api.dataset_download_files("anshtanwar/global-data-on-sustainable-energy", path="data", unzip=True)
```

## Provenance

Downloaded from: https://www.kaggle.com/datasets/anshtanwar/global-data-on-sustainable-energy

Original source: anshtanwar (Kaggle)

**Citation:**
> Tanwar, A. (2023). *Global Data on Sustainable Energy (2000–2020)*. Kaggle. https://www.kaggle.com/datasets/anshtanwar/global-data-on-sustainable-energy
> Underlying data aggregated from World Bank, IEA, and UN SDG databases — no single primary paper.

## License

Attribution 4.0 International (CC BY 4.0)

## Columns

### `global-data-on-sustainable-energy (1).csv`

| Column | Description |
|--------|-------------|
| `Entity` | Country or region name |
| `Year` | Year of observation (2000–2020) |
| `Access to electricity (% of population)` | Population share with electricity access |
| `Access to clean fuels for cooking (% of population)` | Population share using clean cooking fuels as primary source |
| `Renewable-electricity-generating-capacity-per-capita` | Installed renewable energy capacity per person |
| `Financial flows to developing countries (US $)` | Aid from developed countries for clean energy projects |
| `Renewable energy share in total final energy consumption (%)` | Renewable share of final energy consumption |
| `Electricity from fossil fuels (TWh)` | Electricity generated from coal, oil, and gas |
| `Electricity from nuclear (TWh)` | Electricity generated from nuclear power |
| `Electricity from renewables (TWh)` | Electricity generated from hydro, solar, wind, etc. |
| `Low-carbon electricity (% electricity)` | Share of electricity from nuclear and renewables combined |
| `Primary energy consumption per capita (kWh/person)` | Energy use per person |
| `Energy intensity level of primary energy (MJ/$2011 PPP GDP)` | Energy use per unit of GDP (PPP-adjusted) |
| `Value_co2_emissions (metric tons per capita)` | CO₂ emissions per person |
| `Renewables (% equivalent primary energy)` | Renewable share of primary energy equivalent |
| `GDP growth (annual %)` | Annual GDP growth rate based on constant local currency |
| `GDP per capita` | Gross domestic product per person |
| `Density (P/Km2)` | Population density (persons per km²) |
| `Land Area (Km2)` | Total land area (km²) |
| `Latitude` | Country centroid latitude (decimal degrees) |
| `Longitude` | Country centroid longitude (decimal degrees) |

## Why this dataset?

Multi-country, multi-year panel data (20 years × ~176 countries) covering SDG 7 indicators. Excellent for EDA, missing data handling, time-series visualisation, and correlating renewable energy uptake with economic development. The panel structure introduces groupby-and-aggregate patterns; the geographic coordinates enable choropleth mapping as a first data viz exercise.

---

## Source description (from Kaggle)

# Description

&gt; Uncover this dataset showcasing sustainable energy indicators and other useful factors across all countries from 2000 to 2020. Dive into vital aspects such as electricity access, renewable energy, carbon emissions, energy intensity, Financial flows, and economic growth. Compare nations, track progress towards Sustainable Development Goal 7, and gain profound insights into **global energy consumption patterns** over time. 

# Key Features:

&gt;- **Entity**: The name of the country or region for which the data is reported.
- **Year**: The year for which the data is reported, ranging from 2000 to 2020.
- **Access to electricity (% of population)**: The percentage of population with access to electricity.
- **Access to clean fuels for cooking (% of population)**: The percentage of the population with primary reliance on clean fuels.
- **Renewable-electricity-generating-capacity-per-capita**: Installed Renewable energy capacity per person
- **Financial flows to developing countries (US $)**: Aid and assistance from developed countries for clean energy projects.
- **Renewable energy share in total final energy consumption (%)**: Percentage of renewable energy in final energy consumption.
- **Electricity from fossil fuels (TWh)**: Electricity generated from fossil fuels (coal, oil, gas) in terawatt-hours.
- **Electricity from nuclear (TWh)**: Electricity generated from nuclear power in terawatt-hours.
- **Electricity from renewables (TWh)**: Electricity generated from renewable sources (hydro, solar, wind, etc.) in terawatt-hours.
- **Low-carbon electricity (% electricity)**: Percentage of electricity from low-carbon sources (nuclear and renewables).
- **Primary energy consumption per capita (kWh/person)**: Energy consumption per person in kilowatt-hours.
- **Energy intensity level of primary energy (MJ/$2011 PPP GDP)**: Energy use per unit of GDP at purchasing power parity.
- **Value_co2_emissions (metric tons per capita)**: Carbon dioxide emissions per person in metric tons.
- **Renewables (% equivalent primary energy)**: Equivalent primary energy that is derived from renewable sources.
- **GDP growth (annual %)**: Annual GDP growth rate based on constant local currency.
- **GDP per capita**: Gross domestic product per person.
- **Density (P/Km2)**: Population density in persons per square kilometer.
- **Land Area (Km2)**: Total land area in square kilometers.
- **Latitude**: Latitude of the country's centroid in decimal degrees.
- **Longitude**: Longitude of the country's centroid in decimal degrees.

# Potential Use cases

&gt; - **Energy Consumption Prediction:** Predict future energy usage, aid planning, and track SDG 7 progress.
- **Carbon Emission Forecasting:** Forecast CO2 emissions, support climate strategies.
- **Energy Access Classification:** Categorize regions for infrastructure development, understand sustainable energy's role.
- **Sustainable Development Goal Tracking:** Monitor progress towards Goal 7, evaluate policy impact.
- **Energy Equity Analysis:** Analyze access, density, and growth for equitable distribution.
- **Energy Efficiency Optimization:** Identify intensive areas for environmental impact reduction.
- **Renewable Energy Potential Assessment:** Identify regions for green investments based on capacity.
- **Renewable Energy Investment Strategies:** Guide investors towards sustainable opportunities.
