# Strava Performance Analysis

An interactive exercise analytics dashboard built from personal Strava workout data using Python, Altair, and Plotly. The project cleans GPS and physiological metrics, then visualizes them to surface patterns in training behavior, athletic performance, and workout intensity.

## Overview

Strava records a rich set of signals for every workout — distance, pace, heart rate, elevation, cadence, and more. This project loads a raw export of those activities, cleans and enriches the data, and produces a set of linked visualizations to answer questions like:

- How has training volume and intensity changed over time?
- What's the relationship between pace, heart rate, and elevation gain?
- Which workout types correlate with the strongest performance trends?
- Where do anomalies or outlier sessions sit in the broader pattern?

## Dataset

| File | Description |
|---|---|
| `data/raw/strava.csv` | Raw Strava activity export — one row per workout with GPS, pace, heart-rate, and elevation metrics |

## Project structure

```
strava-performance-analysis/
├── analysis/                # Jupyter notebook with the dashboard
│   └── Strava Data (Insights and Reflection).ipynb
├── data/
│   └── raw/                 # Raw Strava export
│       └── strava.csv
├── outputs/                 # Rendered dashboard exports
│   ├── html/
│   │   └── Strava Data (Insights and Reflection).html
│   └── pdf/
│       └── Strava Data (Insights and Reflection).pdf
├── docs/                    # Assignment brief / reference material
│   └── Assignment 4 - Instructions.pdf
├── .gitignore
└── README.md
```

## Key visualizations

- **Training volume over time** — distance and duration trends by week/month
- **Pace vs. heart rate** — efficiency and effort relationship across workout types
- **Elevation impact** — how climbing affects pace and HR distributions
- **Workout-type breakdown** — distribution and trends across run, ride, and other activity types
- **Interactive filtering** — brush and select to drill into specific time windows or activity classes

## How to run

Requires Python 3.9+ and Jupyter.

```bash
pip install pandas altair plotly notebook
jupyter notebook "analysis/Strava Data (Insights and Reflection).ipynb"
```

Run the cells top-to-bottom to render the dashboard inline.

> **Note:** the notebook loads the CSV by bare filename (`strava.csv`). When running from `analysis/`, either launch Jupyter from `data/raw/` or update the path string to `../data/raw/strava.csv`.

## Outputs

Pre-rendered exports of the dashboard live under `outputs/`:

- HTML (interactive): [`outputs/html/Strava Data (Insights and Reflection).html`](outputs/html/Strava%20Data%20%28Insights%20and%20Reflection%29.html)
- PDF (static): [`outputs/pdf/Strava Data (Insights and Reflection).pdf`](outputs/pdf/Strava%20Data%20%28Insights%20and%20Reflection%29.pdf)

## Tech stack

- **Python** — pandas for data wrangling
- **Altair** — declarative, interactive visualization (Vega-Lite)
- **Plotly** — interactive charts for richer exploration
- **Jupyter Notebook** — analysis environment

## Author

**Zainulabidin Adhami**
