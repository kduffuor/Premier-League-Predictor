# ⚽Premier League Predictor
Machine learning models to predict Premier League match outcomes using historical data and team form analysis. Features Random Forest, XGBoost, Gradient Boosting, and Logistic Regression classifiers with interactive visualizations.

## Features
- **Multi-Model Comparison**: Evaluates 4 different ML algorithms
  - Random Forest Classifier
  - XGBoost Classifier
  - Gradient Boosting Classifier
  - Logistic Regression
- **Form-Based Predictions**: Uses team performance from last 5 matches
- **Interactive Visualizations**: Built with Bokeh for match outcome probabilities and team comparisons
- **Real Data**: Pulls live data from [football-data.co.uk](https://www.football-data.co.uk/)

## Dataset
The project uses Premier League match data from 3 seasons (2023-24, 2024-25, 2025-26) including:
- Match results (Home/Draw/Away)
- Goals scored by each team
- Team form metrics
- 830 total matches analyzed

## Installation
```bash
# Clone the repository
git clone https://github.com/kduffuor/Premier-League-Predictor.git
cd Premier-League-Predictor

# Install required packages
pip install pandas numpy scikit-learn xgboost bokeh scipy
```

## Usage
### Running the Jupyter Notebook
```bash
jupyter lab Football_PL_Prediction.ipynb
```

### Quick Prediction Example
```python
# Predict a match between two teams
result = predict_match(models['Logistic Regression'], df_features, 'Arsenal', 'Aston Villa')

print(f"Prediction: {result['prediction']}")
print(f"Home Win: {result['home_win_prob']:.1f}%")
print(f"Draw: {result['draw_prob']:.1f}%")
print(f"Away Win: {result['away_win_prob']:.1f}%")
```

## Key Features Explained
### Form Metrics
- **Points (Last 5 matches)**: Win = 3 pts, Draw = 1 pt, Loss = 0 pts
- **Goals Scored**: Total goals in last 5 matches
- **Goals Conceded**: Total goals allowed in last 5 matches

### Target Variable
- **H**: Home Win
- **D**: Draw
- **A**: Away Win

## Technologies Used
- **Python** - Core programming language
- **pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **scikit-learn** - Machine learning algorithms (Random Forest, Gradient Boosting, Logistic Regression)
- **XGBoost** - Gradient boosting framework
- **Bokeh** - Interactive visualizations
- **SciPy** - Statistical analysis
