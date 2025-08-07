# Crop_Yield_Prediction
A machine learning-powered web application that predicts *crop yield* based on environmental and agricultural parameters. This tool is designed to assist farmers, researchers, and policymakers in making data-driven decisions to improve agricultural productivity.

# Project Overview
This project explores multiple regression models and ultimately deploys a *Decision Tree Regressor* for real-time crop yield prediction using a *Flask* web framework.

# Features
Predicts crop yield based on:
Year, Average rainfall (mm/year), Pesticide usage (tonnes), Average temperature, Area, Crop type.
Simple and clean web interface built using HTML + Flask.
Preprocessing with a saved pipeline using scikit-learn.

# Summary of Model Evaluation

| Model         | MAE (↓ Better) | R² Score (↑ Better) | Remarks                                     |
|---------------|----------------|---------------------|---------------------------------------------|
| Lasso         | 29,883.83      | 0.7473              | Poor performance; convergence issues        |
| Ridge         | 29,852.93      | 0.7473              | Similar to Lasso                            |
| Decision Tree | 5,697.28       | 0.9646              | ✅ Fast, interpretable, and good accuracy    |
| *KNN*       | *4,679.87*   | *0.9846*          | 🔥 Best accuracy, but slower & less interpretable |


# Why Decision Tree was Deployed

Although *KNN* showed the best performance in terms of *MAE* and *R², we selected the **Decision Tree* model for deployment due to:

- *Interpretability*: Easy to explain predictions
- *Speed*: Lower computational cost during prediction
- *Balanced Accuracy*: High R² and low MAE
- *Flexibility*: Handles both numerical and categorical features well

*Technologies Used*
- Python 3.8+
- Flask – web app backend
- scikit-learn – ML model training
- NumPy – numerical operations
- Pickle – saving trained models
- HTML/CSS – frontend templates

*Prediction Inputs*
The model requires the following inputs:
Year (e.g., 2020), 
Average Rainfall (mm/year),
Pesticides Used (tonnes),
Average Temperature (°C),
Area (region or country),
Item (crop name).
