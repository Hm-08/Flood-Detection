# Flood-Detection
Flood Detection using ANN on Malaysia Flood Dataset (2000 - 2010).

## Introduction
To detect flood based on rainfalls using deep learning techniques such as Artificial Neural Network (ANN) / Feedforward NN. This model has been used in my final year project called "Flood Monitoring and Alert System" to enhance predictive modelling for more precise flood forecasts, enabling proactive measures to be taken.

## System Design
![image](https://github.com/Hm-08/Flood-Detection/assets/64012738/1b6f2f0b-3a1c-4c7a-8c8d-94a498c8e27c)

## Data Collection and Exploration
To begin with the implementation of the flood detection, the Malaysia Flood Dataset was downloaded from the Omdena website. The National Centre for Environment Information provided rainfall data for many states and districts in Malaysia from 2000 to 2010. The dataset consists of 825 samples, and each sample consists of 17 variables. Columns in the dataset include the following:
![image](https://github.com/Hm-08/Flood-Detection/assets/64012738/c81cc739-4f71-4b62-a9dd-6473ccf108b0)
However, three columns, namely “STATE”, “ DISTRICT”, and “YEAR”, have been dropped from the dataset because they might not contribute useful information for the current learning task. Besides that, data exploration is carried out to understand its characteristics, patterns, and relationships, which involves visualisation techniques and data analysis to find any missing values or anomalies in the data. Other than that, a few histograms are displayed to observe how the rainfall index changes during the rainy season, from September to January.

## Data Preprocessing
The next component is data preprocessing, which includes handling missing values, feature scaling, and feature engineering tasks. Since “FLOOD” is the target variable, it is separated from the rest of the dataset. In addition, a 9:1 random sample ratio is used to split the dataset into two sets: the training and testing sets. Then, the input features of the dataset are standardised by centering the data around zero and scaling it to a comparable range.

## Model Training
For model training, a 3-layer artificial neural network is constructed and trained using the pre-processed data. During the training process, the training loss, validation loss, training accuracy, and validation accuracy for each epoch are stored in the history object. This information can be used to analyse the model’s performance and visualise the training process.

## Hyperparameter Tuning
For hyperparameter tuning, the RandomSearchCV is utilised to experiment with several combinations of hyperparameters, such as learning rate, optimiser, batch size, and number of epochs. After finishing hyperparameter tuning, the training data is trained on the model using the best parameters found. Next, the accuracy of the training and validation is calculated and compared with the initial model.

## Model Evaluation & Testing 
As the optimal model has been selected and trained, it is evaluated using a variety of performance metrics to assess its performance. For example, this is commonly done using metrics like accuracy score, confusion matrix, precision, recall, and F1-score. After evaluating the model’s performance, a few samples from the testing set are applied to test the model’s effectiveness in actual situations.

## Deployment 
Once the model has been trained, evaluated, and tested successfully, it is saved and converted to TensorFlow Lite format. Then, the TensorFlow Lite model is stored as a file that can be deployed and executed on other platforms, such as mobile devices and web applications.
