# CS171 Final Project — Predicting Air Quality Using Sensor & Weather Data

## Authors
- Vince Lai ([VinceLai1026](https://github.com/VinceLai1026))
- Jjmaxxx ([Jjmaxxx](https://github.com/Jjmaxxx))

## Project Description
- Air pollution is a global concern that impacts public health and the environment.
- Our project aims to predict air quality levels (pollutant concentrations) using historical sensor measurements and weather data.
- We use a public Air Quality dataset recorded in an Italian city (UCI Machine Learning Repository), which includes:
CO, NO₂, NOₓ, Benzene concentrations
Temperature, humidity, absolute humidity
Chemical sensor responses

- Our goal is to create a machine-learning model that predicts pollutant levels based on these environmental features. The project demonstrates the process of data cleaning, feature engineering, model training, and result interpretation.


## Project Plan
- Collect and load the Air Quality dataset (UCI / Kaggle version).
- Clean the dataset and handle missing values.
- Perform exploratory data analysis (EDA).
- Train machine-learning models (Linear Regression, Neural Networks, etc.).
- Evaluate performance and produce visualizations.

### Vince Lai – Data Collection Plan
I will collect air quality and weather data using the  **Kaggle public datasets**.  
I will clean the data, remove missing values, and save the processed data into `.csv` format for training.  
This includes basic preprocessing and merging datasets into a single DataFrame for model input.

### Jjmaxxx – Model Plan
I will develop a **neural network model using PyTorch** to predict AQI values from the processed data.  
I will experiment with different architectures, activation functions, and optimizers to improve accuracy.


## Timeline
Week 9 – Create repo   |  Week 10 – Data Prep   |  Week 11 – Model Train   |  Week 12 – Analysis & Presentation

## License
This project is licensed under the **MIT License**.


