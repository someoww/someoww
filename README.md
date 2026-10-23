# Muktadir Somio

Second-year Applied Statistics & Data Science student at IASDS, University of Dhaka. I play with ideas until they hold or dissolve.

## About

- **Studying:** Applied Statistics & Data Science, IASDS, University of Dhaka.
- **Tools:** Python is my choice for analysis and modelling. R runs the curriculum, so I work in it too and keep the code, datasets and reports in one repository.
- **Away from the screen:** chess, which sharpens me; poker, which humbles me; Spanish, one word at a time on Duolingo.
- **Writing:** I post thoughts, ideas and longer pieces on [Substack](https://somiomuktadir.substack.com).

### How I work

- Start from the problem's failure modes, then pick the model. A route that looks fine on a map can still be fragile; the features should say why.
- Build the schema and the full pipeline on synthetic data first. Swap in real data once the plumbing is proven.
- Split by time whenever the data has a clock, so the model never trains on the future.
- Write the limitations in the README next to the results.

## Projects

### [supply_route](https://github.com/someoww/supply_route): Bangladesh Supply Route Intelligence

A prototype that predicts the condition of domestic supply routes before a disruption is visible. It is aimed at logistics operators, agri-businesses, retailers, policy analysts and humanitarian planners.

- **Problem:** monsoon floods, river erosion, cyclones, ferry and checkpost delays, fuel shocks, strikes, power and mobile-network failures, hoarding and panic buying compound each other. Single-factor models miss that.
- **Data:** a generator produces 100,000 hourly route-condition rows with 85+ columns, grouped as product, time, international shocks (fuel, shipping, forex), natural disasters, festival demand, man-made disruption, digital infrastructure, demographics, middlemen and syndicate risk, transport, cold chain and wastage, policy, contract risk, and engineered compound-risk features.
- **Targets:** `condition_class` (normal, degraded, critical), `delay_hours`, and `supply_route_condition_score` (0 to 100).
- **Model:** scikit-learn `HistGradientBoosting` classifier or regressor, with a time-ordered holdout, time-aware cross-validation, and four complexity presets (`lite`, `balanced`, `deep`, `ultra`).
- **Interface:** `data_generator.py`, `train.py` and `predict.py` run from the command line. Prediction accepts CSV or JSON, fills missing features with training medians, and can return class probabilities.
- **Status:** the data is synthetic and no performance figures are reported. There are no live feeds, no road-network graph and no causal layer yet. Next: real data, geospatial routing, drift monitoring.

Stack: Python, NumPy, pandas, scikit-learn.

### [R](https://github.com/someoww/R)

R code, datasets and reports for data analysis, simulation and data science workflows. Coursework and practice material, organised under `data_science/`.

### [someoww.github.io](https://github.com/someoww/someoww.github.io)

My personal site, built as a single self-contained HTML file: a small room with a cat, a window that follows the time of day, and my links as objects on the floor. No dependencies, no build step, no external requests.

## Elsewhere

- Substack: [somiomuktadir.substack.com](https://somiomuktadir.substack.com)
- Site: [someoww.github.io](https://someoww.github.io)
- Email: somiomuktadir@gmail.com
