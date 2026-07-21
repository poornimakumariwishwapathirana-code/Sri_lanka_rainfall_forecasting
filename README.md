# 🌧️ Comparative Analysis of SARIMA and SARIMAX Models for Rainfall Forecasting Across Climatic Zones in Sri Lanka

## 📖 Overview

This project investigates the performance of **SARIMA (Seasonal AutoRegressive Integrated Moving Average)** and **SARIMAX (Seasonal AutoRegressive Integrated Moving Average with Exogenous Variables)** models for weekly rainfall forecasting across the **Wet, Intermediate, and Dry climatic zones of Sri Lanka**.

The study aims to determine whether incorporating meteorological variables improves forecasting accuracy compared to using historical rainfall observations alone.

The project was completed as part of the **IS4007 – Statistics in Practice II** module in the Department of Statistics, Faculty of Science, University of Colombo.

---

## 🎯 Objectives

- Analyze historical rainfall patterns across Sri Lanka's climatic zones.
- Develop SARIMA models using historical rainfall data.
- Develop SARIMAX models by incorporating meteorological variables.
- Compare forecasting performance across climatic zones.
- Evaluate whether exogenous meteorological variables improve rainfall prediction accuracy.

---

## 📂 Dataset

### Data Source

- **NASA POWER Data Access Viewer**
- https://power.larc.nasa.gov/

### Study Period

- January 2016 – December 2025

### Forecast Period

- January 2025 – December 2025

### Climatic Zones

- 🌿 Wet Zone
- 🌾 Intermediate Zone
- ☀️ Dry Zone

### Variables

| Variable | Description |
|----------|-------------|
| PRECTOTCORR | Weekly Rainfall |
| RH2M | Relative Humidity |
| ALLSKY_SFC_SW_DWN | Solar Radiation |

Daily observations were aggregated into weekly data before model development.

---

## 🛠 Data Preprocessing

The preprocessing pipeline included:

- Downloading meteorological data through the NASA POWER API
- Converting daily observations into weekly observations
- Aggregating district-level data into climatic zones
- Creating seasonal (monsoon) categories
- Handling missing and invalid values
- Splitting the dataset into training and testing sets

Training Data:
- 2016–2024

Testing Data:
- 2025

---

## 📊 Exploratory Data Analysis

EDA included:

- Time series plots
- Moving average smoothing
- Seasonal boxplots
- Histograms
- Correlation heatmaps

The analysis revealed:

- Strong seasonal rainfall patterns
- Different rainfall distributions among climatic zones
- Positive association between rainfall and humidity
- Negative association between rainfall and solar radiation

---

## 📈 Methodology

### 1. Stationarity Test

- Augmented Dickey-Fuller (ADF) Test

### 2. Model Identification

- ACF plots
- PACF plots

### 3. Model Development

- SARIMA
- SARIMAX

Model parameters were selected using Grid Search based on minimum AIC.

### 4. Model Diagnostics

- Ljung-Box Test
- Jarque-Bera Test
- Heteroskedasticity Test
- Residual Analysis

### 5. Forecast Evaluation

Models were evaluated using:

- Root Mean Square Error (RMSE)
- Mean Absolute Error (MAE)

---

## 📌 Results

### Forecast Performance

| Climatic Zone | Better Model |
|---------------|--------------|
| Wet Zone | SARIMA |
| Intermediate Zone | SARIMAX |
| Dry Zone | SARIMA |

### Key Findings

- Meteorological variables improved forecasting accuracy only in the Intermediate Zone.
- Historical rainfall alone was sufficient for accurate forecasting in the Wet and Dry Zones.
- The usefulness of exogenous variables depends on regional climatic characteristics.

---

## 💻 Technologies Used

### Programming Language

- Python

### Libraries

- Pandas
- NumPy
- Statsmodels
- Matplotlib
- Seaborn
- SciPy

### Tools

- Jupyter Notebook
- VS Code
- Git
- GitHub

---

## 📁 Repository Structure

```
Rainfall-Forecasting/
│
├── Data/
│
├── Notebooks/
│
├── Figures/
│
├── Results/
│
├── Report/
│
├── requirements.txt
│
└── README.md
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/Rainfall-Forecasting.git
```

### 2. Navigate to the project

```bash
cd Rainfall-Forecasting
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the notebooks and run the cells sequentially.

---

## 📷 Sample Outputs

The repository contains:

- Rainfall Time Series Plots
- Moving Average Plots
- Seasonal Boxplots
- Histograms
- Correlation Heatmaps
- ACF/PACF Plots
- Residual Diagnostic Plots
- Forecast Comparison Graphs

---

## 🔍 Future Improvements

Potential extensions include:

- Incorporating additional meteorological variables such as temperature and wind speed.
- Evaluating machine learning and deep learning forecasting models (e.g., XGBoost, LSTM).
- Developing hybrid statistical–machine learning models.
- Building an interactive dashboard for rainfall forecasting.
- Automating data retrieval from the NASA POWER API.

---

## 📄 Report

The complete project report is available in this repository.

---

## 👤 Author

**P. M. P. K. Wishwapathirana**

BSc (Hons) in Applied Statistics

Department of Statistics

University of Colombo

---

## 📜 License

This project was developed for academic purposes.
