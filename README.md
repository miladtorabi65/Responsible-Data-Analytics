
# **Responsible Data Analytics: Urban Renewable Energy Forecasting in the Baltic Capitals**

Welcome to the project repository for our Responsible Data Analytics final project! This work presents a comprehensive, four-phase analytics pipeline designed to assess urban sustainability and renewable energy potential across three Baltic capital cities: Vilnius, Riga, and Tallinn.

---

## 📜 Table of Contents

1. [Overview](#overview)
2. [Key Features](#key-features)
3. [Data Sources](#data-sources)
4. [Methodology](#methodology)

   * Descriptive & Diagnostic Analysis
   * Predictive Modeling
   * Prescriptive Strategies
   * Responsible Analytics Considerations
5. [Results](#results)
6. [Getting Started](#getting-started)

   * Prerequisites
   * Installation
   * Usage
7. [Project Structure](#project-structure)
8. [Contributing](#contributing)
9. [Authors](#authors)
10. [License](#license)

---

## 🏙️ Overview

Urban areas face mounting pressure to integrate renewable energy sources into their power grids while ensuring resilience against climate variability. Our project addresses this challenge by:

* Analyzing five years of meteorological data from NASA POWER
* Forecasting daily solar irradiance with a robust stacking ensemble
* Translating forecasts into actionable grid-management strategies

By combining advanced machine learning with ethical data practices, we pave the way for climate-resilient, energy-efficient cities.

---

## ✨ Key Features

* **Multi-City Analysis**: Comparative study of Vilnius, Riga, and Tallinn.
* **Comprehensive Pipeline**: Four phases: Descriptive, Diagnostic, Predictive, Prescriptive.
* **Stacking Ensemble**: Random Forest, Gradient Boosting, SVR, and MLP with RidgeCV meta-learner.
* **High Accuracy**: Achieved RMSE 0.58–0.66 kW·h/m²/day and R²≈0.93.
* **Actionable Insights**: Maintenance scheduling, battery dispatch, demand-side load shifting, market bidding.

---

## 📊 Data Sources

* **NASA POWER**: Daily meteorological variables (solar radiation, temperature, wind speed, humidity) for 2018–2022.
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

## 🚀 Getting Started

### Prerequisites

* Python 3.8+
* `pip` package manager

### Installation

```bash
# Clone the repository
git clone https://github.com/<your-username>/baltic-renewable-forecast.git
cd baltic-renewable-forecast

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use `venv\\Scripts\\activate`

# Install dependencies
pip install -r requirements.txt
```

### Usage

```bash
# Preprocess data\ npython scripts/preprocess_data.py --input data/raw --output data/processed

# Train model
python scripts/train_model.py --config config/train_config.yaml

# Evaluate and generate reports
python scripts/evaluate_model.py --model_path models/stacking_ensemble.pkl --output reports
```

---

## 🗂️ Project Structure

```
├── data
│   ├── raw
│   └── processed
├── notebooks
│   └── exploration.ipynb
├── scripts
│   ├── preprocess_data.py
│   ├── train_model.py
│   └── evaluate_model.py
├── models
├── reports
├── requirements.txt
└── README.md
```

---

## 🤝 Contributing

We welcome contributions! Please open issues or submit pull requests for bug fixes, enhancements, or new features.

---

## 👥 Authors

* Milad [@milad](https://github.com/miladtorabi65)
* Jennifer [@jennifer-Email](j.hu-16@student.tudelft.nl)

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
