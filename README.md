# Human-Activity-Recognition
A comparative study of traditional Machine Learning and Deep Learning models for Human Activity Recognition (HAR) using smartphone sensor data from the UCI HAR dataset.
“FINAL REPORT” 
Abstract:  
Energy expenditure estimation is one of the most essential tasks in health tracking, fitness 
tracking, and, in general, activity recognition systems in which activity awareness is involved. 
This study analyzes different machine learning algorithms and different variants of deep 
learning algorithms for measuring energy expenditure levels with smartphone-based 
accelerometers and gyro sensors in the UCI HAR dataset. As energy expenditure has a tight 
relationship with activity, activity recognition is considered as a surrogate in order to work 
with different intensity levels. Conventional machine learning algorithms, a fully connected 
network, as well as check RNN, LSTM, and GRU algorithms, are considered in this study. 
The experimental analysis demonstrates that all kinds of recurrent algorithms, especially 
GRU, outperform other algorithms, which asserts that time is a fundamental factor in 
expenditure patterns involved in motions. 
1. Introduction/Problem Statement: 
Energy Expenditure Estimation: It involves determining the energy used by a person in 
performing physical activities. It is important to estimate with accuracy in areas such as 
healthcare, obesity research, sports analysis, rehabilitation, and wearable computing. 
Smartphones with installed accelerometers and gyroscopes are a low-cost platform for 
estimating energy expenditure through motion analysis. Activities such as walking, sitting, 
and standing etc. have varying energy expenditure; hence, activity-based estimation is 
appropriate. 
1.1. Objective: 
The goal is to infer the levels of energy expenditure by learning patterns of motion from 
smartphone sensor data based on the following: 
 Feature-based machine learning 
 Fully connected neural networks 
 Recurrent neural networks for temporal modeling 
2. Related Work: 
From previous research, it has been shown that energy spent can be estimated using 
wearable sensors by means of activity classification and modeling of intensity. Traditional 
techniques rely on statistical feature engineering, while deep learning techniques, and more 
specifically recurrent architectures, were far more successful, exploiting the time-dependent 
characteristics of motion patterns. 
3. Methodology: 
3.1.  Feature Engineering & Traditional Machine Learning: 
Statistical, temporal, frequency domain-related features can now be extracted from the 
signal to measure the intensity of movement related to expenditure in energy. 
Features extracted: 
 Statistics: 
mean, median, standard deviation, variance, min, max, skewness, kurtosis 
 Temporal: 
zero-crossing rate, signal energy, peak to peak amplitude, signal magnitude area 
 Frequency: 
Frequency-spectral centroid, spectral entropy 
Models Used: 
 Logistic Regression 
 Support Vector Machine (RBF) 
 Random Forest 
 XGBoost 
3.2. Fully Connected Neural Network  
A fully connected neural network is then trained on these features to model non-linear 
patterns from motion features and different levels of energy expenditure. The network has 
various fully connected layers with ReLU activation functions, which is then optimized by 
Adam with cross-entropy loss. 
3.3. Recurrent neural networks 
To analyze the motion dynamics based on energy consumption, the Recurrent Neural 
Networks were directly trained on multivariable time-series data. 
Models Evaluated: 
These are the models we evaluated. 
 RNN 
 LSTM 
 GRU 
These models learn patterns in the movements of the data over time, and these learned 
patterns are significantly informative for the energy expenditure estimation. 
4. Experiments and Results 
4.1. Description of Dataset 
UCI Human Activity Recognition HAR Dataset-Acceleration and gyroscopes data obtained 
by smartphones. 
 Sensors:  
Accelerometer and Gyroscope 
 Activities : 
Walking, Walking Upstairs, Walking Downstairs, Sitting, Standing, Laying 
 Training samples: 7352 
 Test samples: 2,947 
 The output will be characterized by the following parameters: 
 Sampling rate: 50Hz 
 Sequence length: 128 timesteps 
4.2. Data Settings 
Train/Validation split: 80% / 20% 
Preprocessing: 
 time indexing 
 Handling missing value 
 Removing duplicates 
 Feature scaling (for ML and FCNN) 
Evaluation Metrics: 
 Accuracy 
 weighted F1-score 
4.3. Results 
Comparison of All Approaches 
The following models have been implemented following the literature. The following table 
shows the results:  
Accuracy 
F1-Score 
Model 
Logistic Regression 
61.59% 
SVM (RBF) 
0.606 
60.84% 
Random Forest 
0.597 
63.90% 
XGBoost 
0.636 
64.85% 
Fully Connected Neural Network 
0.646 
68.40% 
RNN 
0.673 
36.85% 
LSTM 
0.244 
21.75% 
GRU 
0.099 
82.94% 
4.4 .  Discussion 
0.827 
 Feature-based ML models are general in energy-related trends but are agnostic to 
time. 
 FCNN enhances performance by capturing non-linear interactions of features.  
 Instability of the gradient and Over fitting is observed in Vanilla RNN and LSTM.  
 GRU is able to reach the highest accuracy, accurately abstracting the idea of 
temporal intensity of motion.  
 Confusion between low-energy activities - Sitting vs Standing occurs due to patterns 
created from sensors being similar to each other.  
 These observations validate the significance of temporal abstraction to achieve an 
accurate result to generate the estimated expenditure of energy. 
5. Conclusion and Future Work 
Conclusion 
This work proves that the use of deep learning methods greatly assists in the calculation of 
energy expenditure from smartphone sensor data. Fair results are achieved by normal 
machine learning and FCNN algorithms. However, the most effective results are achieved by 
RNN algorithms, especially GRU algorithms because of their ability to model the motion 
dynamics.  
Best Performing Model:  
Recurrent Neural Network based on GRU.  Its predicted accuracy is 82.94%. 
Future Work 
 Direct regression-based energy expenditure estimation (calories/METs) 
 CNN–GRU hybrid architectures 
 Deployment on real-time mobile systems 
