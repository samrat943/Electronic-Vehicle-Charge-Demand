# ⚡ Electronic Vehicle Charge Demand

An end-to-end machine learning toolkit designed to forecast electric vehicle (EV) charging station demand, helping operators optimize grid load distribution, avoid bottlenecking, and support sustainable infrastructure planning.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1DBjHI_35l-lnfRJVBlx3Mld4UNtESxku?usp=sharing)
[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 📌 Project Overview

Rapid EV adoption introduces volatile demand patterns that strain localized electrical grids. This project provides a structured pipeline to:
* Extract temporal usage patterns across peak and off-peak charging cycles.
* Model multi-step forward demand using recurrent and baseline forecasting techniques.
* Offer actionable projections for energy providers to balance station resources effectively.

---

## 🚀 Key Features

* **Data Engineering:** Automated cleaning pipelines handling missing values, temporal indexing, and feature creation (e.g., rolling averages, holiday flags, time-of-day encodings).
* **Forecasting Architectures:** Implementations of baseline models (ARIMA/SARIMAX, Tree-based regressors) alongside deep learning approaches (LSTM) for sequence modeling.
* **Metric Benchmarking:** Multi-metric performance tracking evaluated on Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and $R^2$ score.
* **Visualization Suite:** Built-in charting for load duration curves, seasonal decomposition, and prediction-vs-actual tracking.
* **Reproducible Setup:** Fully containerized logic with modular Python scripts and zero-friction Google Colab integration.

---

## 📁 Repository Structure

```text
EV-Charge-Demand/
├── data/
│   ├── raw/               # Immutable historical usage records
│   └── processed/         # Engineered datasets ready for model ingestion
├── models/                # Saved weights, architectures, and scalers (.pkl / .h5)
├── notebooks/             # Exploratory Data Analysis & visual experiment logs
├── src/
│   ├── data_loader.py     # Ingestion and train/test splitting routines
│   ├── features.py        # Feature engineering and scaling pipelines
│   ├── train.py           # Training loops and hyperparameter evaluation
│   └── evaluate.py        # Metric reporting and plot generation
├── requirements.txt       # Frozen environment dependencies
└── README.md
