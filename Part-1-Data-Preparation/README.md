# Part 1
This folder contains the notebook for data loading and preprocessing.
Time Series Data Analysis & Preprocessing
1.	Dataset Description 
  Dataset Name: UCI HAR Dataset
  Source: UCI Machine Learning Repository
  Sensor Type: Accelerometer and Gyroscope in smartphones
  Collected Variables:
•	Accelerometer: tBodyAcc_X, tBodyAcc_Y, tBodyAcc_Z (body acceleration)
•	Gyroscope: tBodyGyro_X, tBodyGyro_Y, tBodyGyro_Z (angular velocity)
•	Labels (Activities): WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING
• Number of Samples: 10,299 rows in training set, 2,947 rows in test set
 
2.	Data Loading and Preprocessing 
Preprocessing Steps:
1.	Added Time Index
•	Reason: The dataset does not include timestamps. Adding a time column simulates chronological order, which is important for time series analysis.
2.	Sorted Data Chronologically
•	Reason: Ensures that all analyses and visualizations follow the correct time order.
3.	Handled Missing Values
• Method: Forward fill (ffill)
•	Reason: Prevents gaps in accelerometer/gyroscope readings which could distort movement detection.
4.	Removed Duplicates
•	Reason: Avoids repeated rows that could bias activity counts or plots.
5.	Renamed Columns
•	Method: Replaced - with _ in column names
•	Reason: Improves clarity and prevents syntax issues in Python code.


 
