# 🌐 GraphCast vs ERA5: 10-Day Forecast Evaluation

This repository contains a detailed evaluation of the GraphCast model's performance over a 10-day forecast period using ERA5 reanalysis data as ground truth.

## 📌 Project Overview

- **Goal**: Evaluate the accuracy of GraphCast's forecasts over India using four key atmospheric variables:
  - Mean Sea Level Pressure (MSLP)
  - Temperature at 500 hPa
  - U-wind at 500 hPa
  - V-wind at 500 hPa

- **Approach**:
  - Ran GraphCast inference using the `ai-models-gfs` pipeline
  - Aligned ERA5 data at 6-hourly intervals for June 2021
  - Calculated RMSE between GraphCast and ERA5 outputs
  - Visualized side-by-side maps and RMSE trends

## 🔍 Key Findings

- GraphCast delivers **reliable forecasts up to ~7–8 days**, especially for temperature.
- Wind components (U and V) show increasing RMSE beyond 7 days, indicating reduced forecast skill at longer horizons.
- MSLP was not included here but can be extended similarly.
- Compared to FourCastNet (run for 10 vs 14 days), GraphCast maintains **stronger performance at 500 hPa for wind and temperature**.

## 🗂 Folder Structure
graphcast-evaluation-10days/
├── notebooks/ graphcast_10days.ipynb
├── data
    / Running_AIWP
    / inputfile breakdown
├── results/ RMSE plot
├── report/ graphcast_10days.pdf
├── README.md # This file


## ⚙️ Requirements

Add the following to `requirements.txt`:

xarray
matplotlib
numpy
ipywidgets
netCDF4

