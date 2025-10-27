# Weather Prediction Project

A machine learning project that predicts next-day maximum temperatures using historical weather data from Oakland International Airport (1960-2022).

## 📊 Project Overview

This project uses Ridge regression to predict tomorrow's maximum temperature based on historical weather patterns. The model achieves a Mean Squared Error of **19.38°F** through feature engineering and temporal analysis.

## 🎯 Features

- **Data Cleaning**: Handles missing values using forward-fill and intelligent imputation
- **Feature Engineering**:
  - 30-day rolling averages
  - Monthly temperature patterns
  - Day-of-year seasonal trends
  - Temperature ratio calculations
- **Model**: Ridge Regression (alpha=0.1)
- **Evaluation**: Train/test split with 2021-2022 as test period

## 📁 Project Structure

```
weather-prediction/
├── weather.ipynb          # Main Jupyter notebook with analysis
├── local_weather.csv      # Historical weather data (1960-2022)
├── .gitignore            # Git ignore rules for Python/Jupyter
└── README.md             # This file
```

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook

### Installation

1. Clone the repository:
```bash
git clone git@github.com:entrelation/weather-prediction.git
cd weather-prediction
```

2. Install required packages:
```bash
pip install pandas scikit-learn matplotlib jupyter
```

3. Launch Jupyter Notebook:
```bash
jupyter notebook weather.ipynb
```

## 📈 Results

### Model Performance

- **Initial Model (Basic Features)**: MSE = 20.56°F
- **Improved Model (Engineered Features)**: MSE = 19.38°F (5.7% improvement)

### Key Insights

- Current maximum temperature is the strongest predictor (0.82 correlation)
- Day-of-year averages capture seasonal patterns well (0.71 correlation)
- Model struggles with rapid weather changes (11-15°F errors)

### Prediction Example

| Date | Actual | Predicted | Error |
|------|--------|-----------|-------|
| 2021-01-01 | 57°F | 59.8°F | 2.8°F |
| 2021-01-17 | 83°F | 68.4°F | 14.6°F |

## 🔍 Data Source

Weather data obtained from **NOAA's Climate Data Online** service:
- Station: Oakland International Airport (USW00023230)
- Period: January 1960 - January 2022
- Variables: Temperature (max/min), Precipitation, Snow

[NOAA Climate Data](https://www.ncdc.noaa.gov/cdo-web/search)

## 🛠️ Technologies Used

- **Python 3.14**
- **pandas 2.3.3** - Data manipulation
- **scikit-learn 1.7.2** - Machine learning
- **matplotlib 3.10.7** - Visualization
- **Jupyter Notebook** - Interactive analysis

## 📝 Next Steps

Potential improvements for the model:

- [ ] Predict entire week ahead instead of single day
- [ ] Incorporate data from multiple nearby weather stations
- [ ] Use additional predictors (wind speed, pressure, humidity)
- [ ] Try different algorithms (Random Forest, XGBoost, Neural Networks)
- [ ] Implement backtesting across all years
- [ ] Add weather condition classification (sunny, rainy, etc.)

## 👤 Author

**entrelation**
- GitHub: [@entrelation](https://github.com/entrelation)

## 📄 License

This project is open source and available for educational purposes.

## 🙏 Acknowledgments

- NOAA for providing historical weather data
- Dataquest for project inspiration
- Claude Code for development assistance

---

*Generated with [Claude Code](https://claude.com/claude-code)*
