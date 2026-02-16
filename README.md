# DengAI: Dengue Fever Prediction

Machine learning models to predict dengue fever cases in San Juan and Iquitos using environmental data.

## Overview

This project predicts weekly dengue cases using climate and environmental variables including temperature, humidity, precipitation, and vegetation indices. Separate models are trained for San Juan, Puerto Rico (936 weeks) and Iquitos, Peru (520 weeks).

## Dataset

**Features:**
- NDVI vegetation indices (4 directions)
- Temperature measurements (Kelvin & Celsius)
- Humidity metrics
- Precipitation data

**Target:** Weekly dengue case counts

## Methodology

1. **Preprocessing:** Forward/backward fill for missing values
2. **Feature Selection:** Correlation-based selection per city
3. **Model:** Linear Regression with StandardScaler
4. **Validation:** 80-20 temporal split

### Selected Features

**San Juan:** Humidity, temperature, and precipitation variables  
**Iquitos:** Temperature range, NDVI indices, and station temperatures

## Results

| City | Dataset Size | Model |
|------|--------------|-------|
| San Juan | 936 observations | Linear Regression |
| Iquitos | 520 observations | Linear Regression |

## Installation
```bash
pip install polars numpy scikit-learn matplotlib seaborn
```

## Usage
```python
python dengai_analysis.py
```

## Tech Stack

- **Data Processing:** Polars, NumPy
- **ML:** scikit-learn
- **Visualization:** Matplotlib, Seaborn

## Future Work

- Time series models (ARIMA, LSTM)
- Ensemble methods
- Lag features
- Hyperparameter optimization

## License

MIT License

---

*DrivenData Competition Entry*
