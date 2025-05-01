# ST2195 Coursework Project (2023–24)

This repository contains the full submission for the ST2195 Business Analytics coursework, consisting of two parts:

- **Part 1**: Simulation using the Metropolis-Hastings (Random Walk Metropolis) algorithm
- **Part 2**: Statistical analysis and modeling of U.S. flight delay and diversion data over a 5-year period

The coursework combines R and Python for data processing, modeling, simulation, and visualization.

## 📌 Part 1: Markov Chain Monte Carlo – Metropolis-Hastings Algorithm

Simulates samples from the probability density:

\[
f(x) = \frac{1}{2} \exp(-|x|), \quad x \in \mathbb{R}
\]

### (a) Random Walk Metropolis Simulation

- Implemented the **Metropolis-Hastings algorithm** using \( N = 10{,}000 \) and step size \( s = 1 \)
- Plotted a **histogram**, **kernel density estimate**, and **true PDF** for visual comparison
- Calculated **Monte Carlo estimates**: mean and standard deviation of the samples

### (b) Convergence Diagnostics (R-hat)

- Computed the **R̂ diagnostic** over multiple chains to assess convergence
- Ran \( J = 4 \) chains of \( N = 2000 \) steps each with different initial values
- Varied the proposal standard deviation \( s \in [0.001, 1] \) and plotted **R̂ vs. s**
- R̂ values close to 1 indicated convergence; poor convergence at very small or large step sizes

## ✈️ Part 2: Flight Delay & Diversion Analysis (10-Year Subset)

Analyzed U.S. domestic flight data (from Harvard Dataverse) across a 5-year window using both **R** and **Python**.

### (a) Best Times & Days to Minimize Delays

- Aggregated delay statistics by hour and day of week per year
- Visualized with heatmaps and bar plots to identify optimal travel times

### (b) Do Older Planes Suffer More Delays?

- Merged plane age data with flight delay data
- Computed correlations and visualized yearly trends in delay vs. aircraft age

### (c) Predicting Diversions with Logistic Regression

- Built yearly logistic regression models (1996–2000) to predict flight diversions
- Features included: date attributes, departure/arrival times, airport coordinates, carrier, distance, and delay metrics
- Visualized model **coefficients** across years and evaluated metrics such as **accuracy**, **precision**, **recall**, **F1-score**, and **AUC**

## 🛠️ Tools & Libraries

**Python**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`  
**R**: `dplyr`, `ggplot2`, `caret`, `pROC`, `readr`


## 👤 Author

Created by Tan De Xun  
Course: ST2195 Programming for Data Science

