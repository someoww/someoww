# Muktadir Somio

Second-year Applied Statistics & Data Science student at IASDS, University of Dhaka. I play with ideas until they hold or dissolve.

## About

- **Studying:** Applied Statistics & Data Science, IASDS, University of Dhaka.
- **Tools:** Python for analysis and modeling; R for coursework and reproducible workflows; code, datasets, and reports stay together in one repository.
- **Away from the screen:** chess, poker, and Spanish on Duolingo.
- **Writing:** thoughts and longer pieces on [Substack](https://somiomuktadir.substack.com).

### How I work

- Start from the problem's failure modes, then choose the model.
- Build the schema and pipeline on synthetic data before switching to real data.
- Split by time whenever the data has a clock.
- Write limitations next to the results.

## Projects

### [supply_route](https://github.com/someoww/supply_route): Bangladesh Supply Route Intelligence

A prototype that predicts domestic supply-route condition before disruption becomes visible.

- **Problem:** monsoon floods, river erosion, cyclones, ferry and checkpost delays, fuel shocks, strikes, power and mobile-network failures, hoarding, and panic buying compound each other.
- **Data:** 100,000 hourly route-condition rows with 85+ features, generated synthetically across product, time, external shocks, natural disasters, festival demand, and route conditions.
- **Targets:** `condition_class` (`normal`, `degraded`, `critical`), `delay_hours`, and `supply_route_condition_score` (0–100).
- **Model:** scikit-learn `HistGradientBoosting` classifier/regressor with time-ordered holdout, time-aware cross-validation, and four presets (`lite`, `balanced`, `deep`, `ultra`).
- **Interface:** command-line scripts for data generation, training, and prediction; accepts CSV or JSON input and fills missing values with training medians.
- **Status:** synthetic-only; no live feeds, road-network graph, or causal layer yet. Next: real data, geospatial routing, and drift monitoring.

Stack: Python, NumPy, pandas, scikit-learn.

### [R](https://github.com/someoww/R)

R code, datasets, and reports for data analysis, simulation, and data science workflows, organized under `data_science/`.

### [someoww.github.io](https://github.com/someoww/someoww.github.io)

My personal site: a single self-contained HTML page featuring a small room, a cat, a time-aware window, and links as objects on the floor.

## Elsewhere

- Substack: [somiomuktadir.substack.com](https://somiomuktadir.substack.com)
- Site: [someoww.github.io](https://someoww.github.io)
- Email: somiomuktadir@gmail.com
