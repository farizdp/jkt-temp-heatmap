# Jakarta Temperature Heatmap

Daily temperature calendar heatmap for Jakarta (2015–2025), built as a single-file D3.js web application.

## Overview

An interactive visualization that displays daily temperature data as a calendar heatmap — 12 month rows by N year columns, where each cell represents one day colored by temperature. Built with an editorial design aesthetic using DM Serif Display and IBM Plex Sans typography.

## Files

- `index.html` — Single-file D3.js application (inline CSS + JS, no build step)
- `jakarta_weather_data.csv` — Daily weather data from Meteostat (2015–2025)
- `jakarta_weather_notebook.ipynb` — Jupyter notebook for data fetching and analysis

## Running

Open `index.html` in any modern browser. No build tools or server required.

For the notebook, install dependencies:

```
pip install meteostat pandas matplotlib numpy
```

## Data

| Field | Detail |
|-------|--------|
| Source | Meteostat — Jakarta Observatory, station 96745 |
| Period | 2015-01-01 to 2025-12-31 |
| Columns | `tavg`, `tmin`, `tmax` (daily temperatures in Celsius) |
| Climate | Tropical Rainforest (Af), decade average 28.6°C |

## Features

- Calendar heatmap with month-rows x year-columns grid
- Controls for year range, temperature type (avg/min/max), and unit (°C/°F)
- 7-color scale from blue (cool) to red (hot), optimized for Jakarta's 24–32°C tropical range
- Tooltip on hover showing exact date and temperature
- Export heatmap as PNG

## Temperature Scale (Tropical)

| Range | Label |
|-------|-------|
| Below 24°C | Cool |
| 24–26°C | Comfortably Cool |
| 26–28°C | Comfortable |
| 28–30°C | Comfortably Warm |
| 30–32°C | Hot |
| 32–35°C | Very Hot |
| Above 35°C | Extreme |

Based on Indonesian thermal comfort studies and the Köppen climate classification.

## Credits

Built with [D3.js](https://d3js.org). Data from [Meteostat](https://meteostat.net).
