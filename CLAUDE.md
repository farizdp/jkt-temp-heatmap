# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Jakarta Temperature Heatmap** — Daily temperature calendar heatmap visualization (2015–2025). Displays temperature as colored cells in a month-rows × year-columns grid using D3.js.

## Files

- `index.html` — Main app: D3.js single-file app with editorial design (inline CSS + JS, no build step)
- `jakarta_weather_data.csv` — Source weather data (tavg/tmin/tmax columns, daily 2015–2025)
- `jakarta_weather_notebook.ipynb` — Jupyter notebook for data fetching and analysis
- `README.md` — Documentation

## Architecture

`index.html` is a self-contained single-file app:
1. Fetch CSV data from `./jakarta_weather_data.csv`
2. Parse into a date→temperature lookup map
3. Render a 12-month × N-year grid where each cell = one day, colored by temperature bin
4. Tooltip on hover shows date + exact temperature
5. Controls for year range, temp type (tavg/tmin/tmax), and unit (°C/°F)

Color scale: 7 colors from blue (cool) → red (hot), with 7 temperature bins optimized for Jakarta's 24–32°C tropical range.

## Running

Open `index.html` directly in a browser. No build tools or server required. For the notebook, use Jupyter.
