
Feature Engineering + Machine Learning for HAR

1. PROJECT DESCRIPTION
----------------------
This project implements Human Activity Recognition (HAR) assignment.
The goal is to extract custom features from the UCI HAR Dataset and train classical
machine learning models to classify human activities.

The pipeline includes:
- Downloading and loading the UCI HAR Dataset
- Cleaning and preparing feature names
- Extracting custom statistical, temporal, and frequency features
- Training multiple ML models (LR, SVM, RF, XGBoost)
- Evaluating accuracy, precision, recall, F1-score, and confusion matrices


2. FILE STRUCTURE
-----------------
The submission contains the following files:

- report.pdf
    Full Week-1 report including dataset summary, feature engineering,
    ML models, evaluation metrics, and discussion.

- code.ipynb
    Jupyter Notebook containing all Python code used for:
    data loading, preprocessing, feature extraction,
    model training, and evaluation.

- features.csv (optional)
    Contains extracted features for all samples. Only included if exported.

- README.txt
    You are reading this file. It explains project structure and how to run the code.


3. HOW TO RUN THE CODE
----------------------
Requirements:
Python 3.8+  
Install dependencies using:

pip install pandas numpy scipy scikit-learn xgboost requests

Steps to execute:
1. Open code.ipynb in Jupyter Notebook or Colab Notebook.
2. Run all cells sequentially from start to end.
3. The notebook will:
   - Download and extract the dataset
   - Process raw data and extract features
   - Train ML models
   - Print evaluation metrics

No GPU is required; CPU execution is sufficient.


4. DATASET INFORMATION
----------------------
Dataset: UCI HAR Dataset (Human Activity Recognition Using Smartphones)
Source: UCI Machine Learning Repository
Sensors: Accelerometer, Gyroscope
Classes: Six human activities (Walking, Sitting, etc.)

The dataset is automatically downloaded by the notebook.


5. NOTES
--------
- Results may vary slightly due to randomness in train/test splits.
- This Week-1 submission focuses only on classical machine learning models.
- Deep learning models will be implemented in Week-2.
