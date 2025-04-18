# Predictive Analysis on UFO Sightings and Related Scientific Datasets

## Overview

This repository contains datasets and analysis notebooks for the Data Analytics CA70 course project. The project explores multiple scientific datasets through various machine learning and statistical methods for predictive analysis, focusing on UFO sightings, NASA meteorite landings, air pollution data, and Kepler exoplanet data.

## Project Structure

```
Data_analytics_CA70-/
├── data/                  # Dataset folders
│   ├── ufo_sightings/     # NUFORC UFO Sightings data
│   ├── nasa_meteorite/    # NASA Meteorite Landing data
│   ├── air_pollution/     # U.S. Pollution Data (2000-2023)
│   └── kepler_exoplanet/  # Kepler Exoplanet data
├── notebooks/             # Jupyter notebooks for analysis
│   ├── ufo_analysis.ipynb       # Random Forest for UFO shape prediction
│   ├── meteorite_analysis.ipynb # Logistic Regression for meteorite classification
│   ├── pollution_analysis.ipynb # SMA for CO level forecasting
│   └── exoplanet_analysis.ipynb # Linear Regression for KOI score prediction
├── scripts/               # Utility scripts for data processing
└── README.md              # This file
```

## Datasets

This project utilizes four distinct datasets:

1. **NUFORC UFO Sightings Dataset**
   - Contains 80,000+ records of UFO sightings
   - Features include location (city, state, coordinates), duration, datetime, and comments
   - Analysis focuses on the most recent 15,000 rows and top three UFO shapes (circle, sphere, triangle)

2. **NASA Meteorite Landing Dataset**
   - Contains ~45,000 records of meteorites that have fallen to Earth
   - Features include location, mass, composition, and fall year
   - Analysis focuses on the top 20 most common meteorite classes

3. **U.S. Pollution Data (2000-2023)**
   - Contains 665,000+ rows of air pollution measurements
   - Features include date, location, and concentrations of pollutants (SO2, NO2, O3, CO)
   - Analysis focuses on predicting CO levels

4. **Kepler Exoplanet Dataset**
   - Contains 9,564 records of Kepler Objects of Interest
   - Features include stellar properties, planetary parameters, and detection metrics
   - Analysis focuses on predicting the KOI score (probability of candidate being a true planet)

## Methods and Analysis

### UFO Sightings Analysis
- **Method**: Random Forest classifier
- **Goal**: Predict UFO shapes (circle, sphere, triangle)
- **Techniques**: TF-IDF for text comments, feature normalization, hyperparameter tuning
- **Results**: Achieved 85% accuracy on test set

### NASA Meteorite Analysis
- **Method**: Logistic Regression
- **Goal**: Predict meteorite classification (recclass)
- **Features**: Mass, latitude, longitude
- **Techniques**: Standard scaling, multi-class classification

### Air Pollution Analysis
- **Method**: Simple Moving Average (SMA)
- **Goal**: Forecast carbon monoxide (CO) levels
- **Techniques**: Time series forecasting with 30-day window
- **Results**: R² of 0.62, MAE of 8.63

### Kepler Exoplanet Analysis
- **Method**: Linear Regression
- **Goal**: Predict KOI score (exoplanet candidate probability)
- **Techniques**: Mean imputation, one-hot encoding, log transformation, feature scaling
- **Results**: Created effective baseline model with good predictive capability

## Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook or JupyterLab
- Required Python packages:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn
  - tensorflow
  - nltk

### Installation

1. Clone the repository:
   ```
   git clone https://github.com/narayanenharris/Data_analytics_CA70-
   ```

2. Navigate to the project directory:
   ```
   cd Data_analytics_CA70-
   ```

3. Install required packages:
   ```
   pip install -r requirements.txt
   ```

### Usage

1. Launch Jupyter Notebook:
   ```
   jupyter notebook
   ```

2. Open any notebook in the `notebooks/` directory to view the analysis.

## Key Findings

- **UFO Sightings**: The Random Forest model successfully classified UFO shapes with 85.37% accuracy. TF-IDF vectorization of comments proved effective for feature extraction.

- **Meteorite Classification**: Logistic Regression provided a baseline for predicting meteorite classes based on mass and landing coordinates, revealing patterns in geographical distribution.

- **Air Pollution**: The 30-day Simple Moving Average effectively captured general trends in Ozone AQI with an R² of 0.62, but showed limitations in predicting sudden changes.

- **Kepler Exoplanets**: Linear Regression with proper preprocessing demonstrated strong predictive capability for KOI scores, suggesting the presence of linear correlations among input features.

## Future Work

- **UFO Analysis**: Explore additional features like time of day and weather conditions; investigate deeper classifications beyond top three shapes; utilize LSTM for improved classification.

- **Meteorite Analysis**: Incorporate additional features; test non-linear models; implement proper train-test splits and cross-validation.

- **Air Pollution**: Test advanced time-series models like ARIMA and LSTM; explore different preprocessing techniques; expand to multiple pollutants and regions.

- **Exoplanet Analysis**: Implement regularized models (Lasso/Ridge); explore tree-based methods; optimize with hyperparameter tuning; integrate astrophysical domain knowledge.

## Contributors

- Harris Narayanen Ramalingam Sathishkumar
- Madhan Kumar Ramesh Babu
- Shraddha Shailesh Gawade
- Kaviya Rajavel

## License

This project is licensed under the MIT License - see the LICENSE file for details.
