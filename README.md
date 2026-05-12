# Real-Time Earthquake Severity & Alert Classification

## Project Overview

This project implements an end-to-end real-time earthquake monitoring and alert classification workflow using live USGS GeoJSON earthquake feeds.

The objective of the project is to:
- monitor real-time seismic activity
- classify earthquake severity
- identify high-risk earthquake events
- generate operational alert predictions
- detect anomalous seismic behavior

The workflow includes:
- real-time API ingestion
- data preprocessing and cleaning
- feature engineering
- exploratory data analysis (EDA)
- machine learning classification
- anomaly detection
- operational reporting and insights

---

## Dataset Source

USGS Real-Time Earthquake GeoJSON Feed:

https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_day.geojson

Reference:

https://earthquake.usgs.gov/earthquakes/feed/

---

## Dataset Features

The dataset contains:
- earthquake magnitude
- location information
- timestamps
- longitude and latitude
- earthquake depth
- tsunami indicators
- seismic significance scores
- additional seismic metadata

---

## Workflow

1. Fetch real-time GeoJSON earthquake feed
2. Normalize nested GeoJSON structures
3. Clean and preprocess seismic data
4. Extract geospatial and temporal features
5. Engineer severity and risk indicators
6. Perform exploratory data analysis (EDA)
7. Generate operational alert labels
8. Train Random Forest classification model
9. Perform anomaly detection using Isolation Forest
10. Generate operational insights and alert reports

---

## Feature Engineering

The following engineered features were created:
- severity category
- depth classification
- regional extraction
- temporal features (hour/day)
- risk indicators
- distance-related geospatial feature

---

## Machine Learning Models Used

### Random Forest Classifier

Used for:
- operational alert prediction
- earthquake severity classification
- feature importance analysis

### Isolation Forest

Used for:
- anomaly detection
- unusual seismic activity identification

---

## Exploratory Data Analysis (EDA)

EDA included:
- earthquake magnitude distribution
- geospatial earthquake visualization
- severity distribution analysis
- feature correlation heatmaps
- feature importance visualization

---

## Assumptions

- The original USGS dataset did not contain predefined operational alert labels
- The target variable `alert_required` was engineered using domain-based seismic thresholds
- Earthquakes with higher magnitude, shallow depth, high significance score, or tsunami indicators were treated as operationally risky
- The current USGS feed did not consistently contain `properties.alert`
- Engineered labels were used to create a supervised learning classification dataset

---

## Key Findings

- Most earthquake events were shallow seismic activities
- Earthquake depth was identified as the strongest predictive feature
- Geospatial features contributed significantly to alert prediction
- The classification model achieved strong recall performance for high-risk events
- Isolation Forest successfully identified anomalous seismic events

---

## Limitations

- Alert labels were engineered and not officially provided in the dataset
- Real-world earthquake alert systems use additional geophysical indicators
- The model was trained on short-term real-time seismic feeds
- Distance calculations were simplified for prototype implementation

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Requests
- Jupyter Notebook

---

## Setup Instructions

### Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn requests jupyter