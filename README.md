# CS171 Final Project — Air Quality Prediction
### Authors
- Vince Lai ([VinceLai1026](https://github.com/VinceLai1026))
- Jjmaxxx ([Jjmaxxx](https://github.com/Jjmaxxx))
### Instructor: Dr. Mike Wood  
### Semester: Fall 2025 
This project predicts next-hour Air Quality Index (AQI) using pollutant sensor data and weather measurements from the UCI Air Quality Dataset.
We trained and compared Linear Regression, Random Forest, and a Neural Network (MLP) to determine which model performs best for short-term AQI forecasting.

## Project Overview
We used 9,358 hourly readings containing sensor measurements such as CO, NO₂, NOₓ, benzene concentration, along with weather variables (temperature, relative humidity, absolute humidity).
The project includes:
- Data preprocessing by each team member
- Model construction and training
- Evaluation and comparison across three ML models
- Analysis and visualization of results
- Clear separation of partner responsibilities

## Repository Structure
```
cs171-final-project/
│
├── vince_preprocessing.ipynb
├── justin_preprocessing.ipynb
│
├── vince_model.ipynb
├── justin_model.ipynb
│
├── analysis_visualization.ipynb
│
├── vince_clean_airquality.csv
├── justin_clean_airquality.csv
│
└── README.md
```

## Dataset Description
Source: UCI Machine Learning Repository – Air Quality Dataset
Contents include:
- Chemical sensor readings (CO, NMHC, NO₂, NOₓ, O₃)
- Metal-oxide sensor responses (PT08.*)
- Weather metrics (Temperature, RH, AH)
- Timestamped hourly recordings
The goal of this project is to predict the AQI for the next hour (AQI_next_hour) based on current sensor and weather data.


## Data Preprocessing
### Vince’s Preprocessing Notebook
vince_preprocessing.ipynb
- Removed unnamed columns
- Replaced sentinel value –200 with NaN
- Dropped columns with more than 50% missing data
- Filled remaining NaN values with median
- Merged date and time into a single datetime column
- Engineered hour, day_of_week, and month features
- Created the target variable AQI_next_hour
- Standardized features using StandardScaler

### Justin’s Preprocessing Notebook
justin_preprocessing.ipynb
- Calculated AQI from pollutant averages
- Generated AQI_next_hour
- Replaced missing values and dropped highly incomplete columns
- Created datetime column and ordered data chronologically
- Saved dataset for neural network training

## Models Trained
### Vince – Linear Regression & Random Forest
vince_model.ipynb
#### Linear Regression
- Baseline model
- Simple and interpretable
- Captures general AQI trend
- Struggles with extreme AQI values
- Performance:
MAE ≈ 47
RMSE ≈ 65
R² ≈ 0.78
#### Random Forest
- 300 trees, max depth 15
- Captures nonlinear interactions
- More accurate and robust than Linear Regression
- Feature importance highlights NMHC and CO as strongest predictors
- Performance:
MAE ≈ 49
RMSE ≈ 63
R² ≈ 0.80

### Justin – Neural Network (MLP)
justin_model.ipynb
- Multiple architectures tested
- Best model used hidden sizes [256, 128, 64]
- ReLU activation and Adam optimizer
- Achieved test MSE ≈ 0.196

## Analysis and Visualization
analysis_visualization.ipynb
Includes:
- Prediction vs actual plots for all models
- Random Forest feature importance
- Neural network training curves
- Comparison table of all model metrics

Key findings:
- Linear Regression provides a reliable baseline
- Random Forest achieves better accuracy and interpretability
- Neural Network performs competitively with slight overfitting

## Roles and Responsibilities
### Vince Lai
- Preprocessing notebook
- Linear Regression model
- Random Forest model
- Analysis & visualization for LR/RF
- Presentation sections

### Justin Nguyen
- Preprocessing notebook
- Neural Network model
- Analysis & visualization for NN
- Presentation sections

## Installation Instructions
Install required packages:

pip install pandas numpy matplotlib seaborn scikit-learn torch

Run order:
1. Preprocessing notebooks
2. Model notebooks
3. Analysis notebook
All notebooks run on any OS with Python 3.10+.

## Future Work
- Hyperparameter tuning
- LSTM or other time-series models
- Improved AQI calculations
- Real-time AQI prediction API pipeline
- Cross-validation for more robust evaluation

## Project Status: Complete and Ready for Grading
Thank you for reviewing our project!




