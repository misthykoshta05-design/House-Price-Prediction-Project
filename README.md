🏠 House Price Prediction using Machine Learning

📌 Project Overview

House Price Prediction is a beginner-friendly Data Science and Machine Learning project that predicts house prices based on different features such as area, number of bedrooms, bathrooms, location, furnishing status, parking, and house age.

The project demonstrates the complete Data Science workflow, including data generation, exploratory data analysis (EDA), data preprocessing, feature engineering, model training, evaluation, and saving the trained model.

Note: This project currently uses a synthetically generated dataset for learning purposes. The prices are not verified real-estate market prices.

🎯 Objectives

- Understand and analyze housing data using EDA.
- Perform data cleaning and preprocessing.
- Create new features using feature engineering.
- Train Machine Learning regression models.
- Evaluate model performance using different metrics.
- Save and load the trained model using Joblib.
- Predict the price of a new house.

🛠️ Technologies Used

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib

📂 Project Structure

house_price_project/
│
├── house_price_prediction.ipynb
├── house_price-model.pkl
├── README.md
│
└── data/
    └── house_data.csv


📊 Dataset Description

The dataset contains house-related features such as:

Feature| Description
Area| House area in square feet
Bedrooms| Number of bedrooms
Bathrooms| Number of bathrooms
Parking| Number of parking spaces
Stories| Number of floors
Location| City of the house
Furnishing| Furnishing status
Age| Age of the house
Price| Target variable to predict

Additional features created during feature engineering include:

- "House_Age"
- "Total_Rooms"
- "Area_per_Bedroom"
- "Area_Category"

🔍 Exploratory Data Analysis (EDA)

EDA is performed to understand the dataset and identify patterns and relationships.

The analysis includes:

- Checking dataset shape and information.
- Generating descriptive statistics.
- Checking missing values and duplicate records.
- Analyzing the distribution of house prices.
- Studying the relationship between area and price.
- Comparing prices across bedroom counts and locations.
- Visualizing numerical correlations using a heatmap.

🧹 Data Preprocessing

The following preprocessing techniques are used:

- Removing duplicate records.
- Handling missing numerical values using median imputation.
- Handling missing categorical values using most-frequent imputation.
- Scaling numerical features using StandardScaler.
- Encoding categorical features using OneHotEncoder.
- Using a preprocessing pipeline to organize the workflow.

⚙️ Feature Engineering

New features are created to represent house characteristics more effectively.

- House_Age: Represents the age of the house.
- Total_Rooms: Combines the number of bedrooms and bathrooms.
- Area_per_Bedroom: Calculates area per bedroom.
- Area_Category: Classifies houses into Small, Medium, and Large categories.

🤖 Machine Learning Models

Two regression models are trained and compared:

1. Linear Regression — models linear relationships between input features and house prices.
2. Random Forest Regressor — combines multiple decision trees to predict numerical values.

The dataset is split into training and testing sets to evaluate performance on unseen records.

📈 Model Evaluation

The models are evaluated using the following metrics:

- MAE (Mean Absolute Error): Measures the average absolute difference between actual and predicted prices.
- RMSE (Root Mean Squared Error): Penalizes larger prediction errors more strongly.
- R² Score: Measures how well the model explains variation in the target variable.


💾 Saving the Model

The selected trained pipeline is saved using Joblib.

import joblib

joblib.dump(best_model, "house_price_model.pkl")

The saved model can be loaded later to predict prices without training the model again.

🔮 Making Predictions

Example of loading the saved model:

loaded_model = joblib.load("house_price_model.pkl")

predicted_price = loaded_model.predict(new_house)[0]

print(f"Predicted House Price: ₹{predicted_price:,.0f}")

Here, "new_house" is a Pandas DataFrame containing the features required by the trained model.

🚀 How to Run the Project

1. Clone or download this repository.

2. Open the project folder.

3. Install the required libraries:
   
   pip install numpy pandas matplotlib seaborn scikit-learn joblib

4. Open Jupyter Notebook:
   
   jupyter notebook

5. Open "house_price_prediction.ipynb".

6. Run the notebook cells in order.

7. Explore the EDA graphs, preprocessing steps, model evaluation results, and price predictions.

📚 Key Learnings

Through this project, I practiced:

- Data analysis using Pandas and NumPy.
- Data visualization using Matplotlib and Seaborn.
- Data preprocessing and feature engineering.
- Building Machine Learning pipelines.
- Training regression models.
- Evaluating model performance.
- Saving and loading models with Joblib.

🔮 Future Improvements

- Use a real-world housing dataset.
- Improve feature selection and model performance.
- Perform hyperparameter tuning.
- Build an interactive prediction interface using Streamlit.
- Deploy the model as a web application.


⭐ Acknowledgement

This project is part of my journey in learning Data Science and Machine Learning. Feedback and suggestions for improvement are welcome.