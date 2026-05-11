#⛽ FuelBrain — Predictive Fuel Cost Optimiser
## Built for Alblas International Logistics · NL–Germany corridor

**Status:** 🔨 In progress (Day 1 — environment setup complete)

---

## The problem
Diesel costs rose 11–49% across Europe in early 2026.
For a logistics company running 265+ trucks on NL–Germany routes daily,
even a 5% improvement in departure timing can mean hundreds of thousands
of euros in annual savings.

Alblas International Logistics operates daily linehaul shuttles between
the Netherlands and Germany carrying flowers, fresh produce, and chemicals.
Today there is no predictive model helping dispatchers choose the lowest-cost
departure window.

## What FuelBrain does
- Predicts fuel cost per km for any NL–Germany route and departure date
- Identifies the cheapest 1–2 day dispatch window each week
- Estimates fleet-wide monthly savings from timing optimisation
- Fires alerts when EU diesel prices drop below a configurable threshold

## Data sources (all free and public)
| Source | What it provides |
|--------|-----------------|
| EU Oil Bulletin (ec.europa.eu) | Weekly NL diesel prices |
| Open-Meteo API | Daily wind, rain, temperature for NL–DE routes |
| Synthetic trip data | 4,000 Alblas-modelled trip records |

## Tech stack
Python · LightGBM · SHAP · Streamlit · Plotly · pandas

## Key result
> *(Will be updated after model training in Week 2)*
> Estimated monthly saving: **€[X]** on a 100-truck NL–DE fleet

## How to run locally
```bash
git clone https://github.com/YOUR_USERNAME/fuelbrain-alblas.git
cd fuelbrain-alblas
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt
streamlit run app/streamlit_app.py
```

## Project structure
See /src for data pipeline scripts, /notebooks for model training,
/app for the Streamlit dashboard.

---
*Built as a portfolio project inspired by Alblas International Logistics.*
