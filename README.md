
# **Responsible Data Analytics: Urban Renewable Energy Forecasting in the Baltic Capitals**

Welcome to the project repository for our Responsible Data Analytics final project! This work presents a comprehensive, four-phase analytics pipeline designed to assess urban sustainability and renewable energy potential across three Baltic capital cities: Vilnius, Riga, and Tallinn.


## 🏙️ Overview

Urban areas face mounting pressure to integrate renewable energy sources into their power grids while ensuring resilience against climate variability. Our project addresses this challenge by:

* Analyzing five years of meteorological data from NASA POWER
* Forecasting daily solar irradiance with a robust stacking ensemble
* Translating forecasts into actionable grid-management strategies

By combining advanced machine learning with ethical data practices, we pave the way for climate-resilient, energy-efficient cities.

---

# 📄Report
The complete project report is available for detailed reference:
[📘 View Full Report (PDF)](./Final-Project-Report-Milad-Jennifer-Group8.pdf)

---

## ✨ Key Features

* **Multi-City Analysis**: Comparative study of Vilnius, Riga, and Tallinn.
* **Comprehensive Pipeline**: Four phases: Descriptive, Diagnostic, Predictive, Prescriptive.
* **Stacking Ensemble**: Random Forest, Gradient Boosting, SVR, and MLP with RidgeCV meta-learner.
* **High Accuracy**: Achieved RMSE 0.58–0.66 kW·h/m²/day and R²≈0.93.
* **Actionable Insights**: Maintenance scheduling, battery dispatch, demand-side load shifting, market bidding.

---

## 📊 Data Sources

* **[NASA POWER](https://power.larc.nasa.gov/data-access-viewer/)**: Daily meteorological variables (solar radiation, temperature, wind speed, humidity) for 2018–2022.
* **City Metadata**: Geographic coordinates and urban parameters for each capital.

---

## 🔬 Methodology

### 1. Descriptive & Diagnostic Analysis

* Visualized seasonal trends and correlations among key variables.
* Identified interdependencies and potential outliers.

### 2. Predictive Modeling

* Engineered time-aware features (lagged variables, rolling statistics).
* Trained and validated a heterogeneous stacking ensemble.
* Evaluated performance via RMSE and R² metrics.

### 3. Prescriptive Strategies

* Translated irradiance forecasts into:

  * **Dynamic Battery Dispatch**: Optimized charge/discharge cycles.
  * **Maintenance Scheduling**: Scheduled during low-production periods.
  * **Demand-Response Load Shifting**: Recommended peak load adjustments.
  * **Market Bidding**: Informed pricing strategies based on forecast confidence.

### 4. Responsible Analytics

* Ensured data privacy and ethical use.
* Documented bias checks and model interpretability assessments.

---

## 📈 Results

| City    | RMSE (kW·h/m²/day) | R² Score |
| ------- | ------------------ | -------- |
| Vilnius | 0.60               | 0.92     |
| Riga    | 0.58               | 0.94     |
| Tallinn | 0.66               | 0.93     |

Our ensemble consistently delivered high predictive accuracy, enabling reliable operational planning.

---

## 🤝 Contributing

We welcome contributions! Please open issues or submit pull requests for bug fixes, enhancements, or new features.

---

## 👥 Authors

* Milad [@milad](https://github.com/miladtorabi65)
* Jennifer j.hu-16@student.tudelft.nl

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
