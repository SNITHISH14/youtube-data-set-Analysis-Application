# youtube-data-set-Analysis-Application
This dataset is take in Kaggle   
About this file
 Overview of the YouTube 2025 Dataset

This futuristic dataset offers a detailed look at 5,000 YouTube channels, designed to reflect how content creation might evolve by the year 2025. It explores not only the traditional metrics like subscriber count and video stats but also dives deep into cutting-edge trends such as AI-generated content, neural interface compatibility, and metaverse integration.

This project is a simple data analysis application using a machine learning model to analyze a YouTube dataset.

 Features
Data cleaning & preprocessing

Exploratory Data Analysis (EDA)

Machine learning model (e.g., regression/classification)

Result visualization

 Tech Stack
Python, Jupyter Notebook

Pandas, NumPy, Matplotlib, Seaborn

Scikit-learn for ML

 How to Use
Open the notebook:
Project_Develop_a_Simple_Data_Analysis_Application_with_Machine_Learning_model_in_youtube_data_set.ipynb

Run cells step by step to see analysis and model results.

 Output
Visual insights

ML predictions

Performance metrics


"""
YouTube 2025 Dataset Preprocessing Script

This script loads a YouTube dataset CSV, cleans the data by:
- Removing irrelevant or non-numeric columns
- Applying one-hot encoding to categorical features
- Dropping missing values

Usage: Run the script directly to view the original and preprocessed data.
"""
 YouTube Data Regression Model (2025 Dataset)
This Python script builds a machine learning regression model to predict YouTube video Engagement Scores based on various features from a futuristic dataset.

 What It Does
Loads the dataset (CSV file)

Cleans & preprocesses the data:

Drops irrelevant columns

One-hot encodes categorical values

Removes missing data

Trains a Random Forest Regressor on the data

Evaluates the model using RMSE and R² score

 Tech Stack
pandas, numpy – for data handling

scikit-learn – for ML model & evaluation

 Function Breakdown
1. load_and_preprocess(filepath)
Purpose: Cleans the dataset.

Steps:

Loads the CSV file.

Drops irrelevant/non-useful columns:

Channel Name, Youtuber Name, etc.

Encodes the categorical column Metaverse Integration Level using one-hot encoding.

Drops rows with any missing values.

2. split_data(df)
Purpose: Splits the data into train/test sets.

Steps:

Separates features (X) and target (y) → here Engagement Score is the target.

Splits the data:

80% for training

20% for testing

Prints the number of rows in each set.

3. main()
Loads and preprocesses the dataset.

Splits the dataset using the above functions.

Step-by-Step Breakdown
1. load_and_preprocess(filepath)
Loads the dataset from a CSV file.

Cleans the data by:

Dropping irrelevant columns like 'Channel Name', 'Best Video', etc.

Encoding the categorical column 'Metaverse Integration Level' using one-hot encoding.

Removing rows with missing values.

Train/Test Split
Splits data into:

Features (X) → all columns except 'Engagement Score'

Target (y) → 'Engagement Score'

Uses train_test_split() to split:

80% → Training data

20% → Testing data


Model Training
Trains a Random Forest Regressor, which is good for handling non-linear patterns and complex datasets.

Model Prediction & Evaluation
Predicts the engagement scores on the test set.
Calculates:

  RMSE (Root Mean Squared Error) – how far predictions are from actual values (lower = better)

  R² Score – how well the model explains the variability (closer to 1 = better)

   Interactive Option
   Lets the user choose whether to view the visualization.
   Your script:

Preprocesses the data

Trains a regression model

Evaluates it with metrics

Optionally visualizes results for better understanding
