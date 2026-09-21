Week 2 — Mini Project 2: House Price Prediction Model

Machine Learning internship/coursework for Week 2, focused on Supervised Learning using Linear Regression.

This project builds a Linear Regression model using the Kaggle – House Prices Dataset to predict house sale prices.

📌 Project Overview

Project: House Price Prediction Model
Week: Week 2 — Supervised Learning (Regression & Classification)
Dataset: Kaggle — House Prices Dataset
Model: Linear Regression
Target Variable: SalePrice

The objective is to train a Linear Regression model, predict house prices, evaluate the model using the R² score, and visualize Predicted vs Actual house prices.

🎯 Tasks Completed
Load the Kaggle House Prices Dataset
Perform necessary data preprocessing and cleaning
Select suitable features
Select SalePrice as the target variable
Split the data into training and testing sets
Train a Linear Regression model
Predict house prices
Evaluate the model using R² score
Plot Predicted vs Actual values
🔧 Methodology
1. Data Preprocessing

The dataset is inspected for missing values and unnecessary columns. Missing numerical values are handled appropriately before model training.

2. Feature Selection

Relevant numerical features are selected to train the Linear Regression model and predict SalePrice.

3. Train-Test Split

The dataset is divided into training and testing sets using an 80:20 split with random_state=42.

4. Model Training

A Linear Regression model from Scikit-learn is trained using the selected features.

5. Prediction

The trained model predicts house prices for the test dataset.

6. Model Evaluation

The model is evaluated using the R² (R-squared) score.

7. Visualization

A Predicted vs Actual Values plot is created to visually compare the model's predictions with the actual house prices.

📊 Results
Metric	Value
R² Score	0.8199
MSE	994,803,510
RMSE	$31,540

The model achieved an R² score of 0.8199 on the test data.

📈 Predicted vs Actual Values

The following plot compares the predicted house prices with the actual house prices from the test dataset.

📁 Project Structure
week2-house-price-prediction/
│
├── data/
│   └── house_prices_train.csv
│
├── images/
│   └── predicted_vs_actual.png
│
├── 03_mini_project2_house_price_prediction.ipynb
│
├── requirements.txt
└── README.md
🛠️ Technologies Used
Technology	Purpose
Python	Programming language
Pandas	Data loading and preprocessing
NumPy	Numerical operations
Matplotlib	Data visualization
Scikit-learn	Linear Regression and evaluation
Jupyter Notebook	Project development
▶️ How to Run
1. Clone the repository
git clone https://github.com/<your-username>/week2-house-price-prediction.git
cd week2-house-price-prediction
2. Install dependencies
pip install -r requirements.txt
3. Open the Jupyter Notebook
jupyter notebook

Then open:

03_mini_project2_house_price_prediction.ipynb

Run the notebook cells from top to bottom.

📚 Learning Outcomes

Through this project, the following concepts were practiced:

Supervised Learning
Regression
Linear Regression
Data preprocessing
Feature selection
Train-test splitting
Model prediction
R² evaluation
Predicted vs Actual visualization
📌 Submission

Week 2 — Mini Project 2: House Price Prediction Model

Dataset: Kaggle — House Prices Dataset
Algorithm: Linear Regression