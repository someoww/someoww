# Muktadir Somio

Second-year Applied Statistics & Data Science student at IASDS, University of Dhaka. I like turning messy questions into something testable.

## About

- **Studying:** Applied Statistics & Data Science at IASDS, University of Dhaka.
- **Tools:** Python for analysis and modeling, R for coursework and reproducible work, with code, data, and reports in the same place.
- **Off-screen:** chess, poker, and Spanish on Duolingo.
- **Writing:** notes and longer pieces on [Substack](https://somiomuktadir.substack.com).

## How I work

- Start from the failure modes, then choose the method.
- Build the pipeline on synthetic data before using real data.
- Keep time in mind whenever the data has a clock.
- Write the limits next to the results.

## Projects

### [supply_route](https://github.com/someoww/supply_route): Bangladesh Supply Route Intelligence

A small prototype for spotting weak supply routes before disruption becomes obvious.

- **Problem:** floods, erosion, cyclones, delays, fuel shocks, strikes, power and network failures, hoarding, and panic buying all stack up.
- **Data:** 100,000 hourly rows with 85+ features generated synthetically across product, time, shocks, disasters, demand, and route conditions.
- **Targets:** `condition_class` (`normal`, `degraded`, `critical`), `delay_hours`, and `supply_route_condition_score` (0 to 100).
- **Model:** scikit-learn `HistGradientBoosting` with time-based validation and four presets: `lite`, `balanced`, `deep`, and `ultra`.
- **Interface:** CLI tools for generation, training, and prediction; accepts CSV or JSON and fills missing values with training medians.
- **Status:** synthetic data only. No live feed, no road network, no causal layer yet.

Stack: Python, NumPy, pandas, scikit-learn.

### [R](https://github.com/someoww/R)

R code, datasets, and reports for analysis, simulation, and data science work under `data_science/`.

### [someoww.github.io](https://github.com/someoww/someoww.github.io)

A small personal site built as one self-contained HTML page.

## Elsewhere

- Substack: [somiomuktadir.substack.com](https://somiomuktadir.substack.com)
- Site: [someoww.github.io](https://someoww.github.io)
- Email: somiomuktadir@gmail.com
