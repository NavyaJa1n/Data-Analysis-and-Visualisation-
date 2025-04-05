
# Customer Booking Prediction: Analyzing and Improving Model Performance

## Dataset Overview

The dataset used in this project contains customer booking data for a travel company. The target variable is whether a customer will complete their booking (`booking_complete`). The dataset includes several features that describe the customer's behavior and characteristics at the time of booking.

### Key Features:
- **sales_channel**: The channel through which the booking was made (e.g., online, call center).
- **trip_type**: The type of trip (e.g., one-way, round-trip).
- **flight_day**: The day of the flight.
- **route**: The flight route (departure and destination).
- **booking_origin**: The origin of the booking (e.g., country or city).
- **booking_complete**: The target variable, indicating whether the booking was completed (1) or not (0).

## Objective

The goal of this project is to predict whether a customer will complete their booking based on the available features. Since the dataset is imbalanced, we will apply various machine learning models and improve performance using techniques like **SMOTE** (Synthetic Minority Over-sampling Technique) and model comparison.

## Approach

The approach involves several key stages:

1. **Data Exploration and Preprocessing**: Begin by loading the data and performing basic exploratory data analysis (EDA) to understand the dataset's structure. We'll also encode categorical variables to prepare the data for modeling.

2. **Model Application**: Apply multiple machine learning models to predict the target variable (`booking_complete`).

3. **Hyperparameter Tuning**: Optimize the models using **Grid Search CV** to improve performance.

4. **Handling Imbalanced Classes**: Address the class imbalance using **SMOTE** to generate synthetic samples of the minority class.

5. **Re-evaluation and Performance Comparison**: Re-evaluate the models after applying SMOTE and compare the performance improvements.

6. **Visualization**: Visualize the results of model performance before and after applying SMOTE to analyze the improvements in model accuracy and other metrics.

## Data Exploration and Preprocessing

In the initial phase, we load the data and perform exploratory data analysis (EDA) to gain insights into the dataset's structure and distribution. This step includes checking for missing values, data types, and basic statistics. We also encode the categorical columns using techniques such as **Label Encoding**.

---

