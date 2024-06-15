# Income Prediction with Azure ML Studio

Using the Adult Census data, I will build two boosted decision tree models (one model will be trained on the upsampled data, and the other with just the original pre-processed data) and create an end-to-end pipeline using Azure ML Studio. The objectives are the following:

- Pre-process the data
- Train and evaluate the model with Azure ML Studio
- Create scoring and predictive experiments
- Deploy the trained model as an Azure web service

### Task I- Introduction and Overview

- Create a new experiment from the Azure ML Studio dashboard
- Import and explore the Adult Census data before moving on to pre-processing

a) Importing the dataset
![Importing Data](images/Data-1.png)

b) Viewing the class imbalance
![Class Imbalance](images/Class-Imbalance-2.png)

### Task 2- Data Cleaning

- Clean the data
- Handle missing values
- Exclude irrelevant or redundant columns
- Once the final set of features is ready, use the Edit Metadata module to convert specific columns from string to categorical

a) Clean missing data
![Clean Missing Data](images/Clean-Missing-Data-3.png)

b) Exlcuding unnecessary columns
![Excluding Columns](images/Excluding-Columns-4.png)

c) Using the Edit Metadata module to change datatypes
![Edit Metadata](images/Edit-Metadata-5.png)

d) Converting Categorical Columns
![Converting Categorical Columns](images/Converting-Cat-Columns-6.png)

### Task 3- Accounting for Class Imbalance

- Upsample the data, but only on the training data so that none of the information in the validation data is used to create synthetic observations. So these results should be generalizable.

a) Use the SMOTE (Synthetic Minority Over-sampling Technique) Module for Class Imbalance
![SMOTE](images/Smote-7.png)

### Task 4- Model Training and Hyperparameter Tuning

- Train a two-class boosted decision tree model to predict the income
- Perform hyperparameter tuning using the Tune Model Hyperparameters module

a) Split the Data (without SMOTE)
![Split the Data](images/Split-Data-8.png)

b) Implement Decision Tree Model
![Decision Tree](images/Decision-Tree-9.png)

c) Splitting the Data Once More (with SMOTE)
![Split the Data](images/Split-Data-10.png)

d) Tune Model Hyperparameters Module
![Tune Model Hyperparameters](images/Tune-Model-11.png)

e) View of the ML Workflow
![Worflow](images/Worflow-12.png)

### Task 5- Scoring and Evaluating Models

- Compare how the two models perform using the Score Model and Evaluate Model modules
- Use AOC and ROC metrics for evaluation

a) Use Evaluate Model Module 
![Evaluate Model](images/Score-Evaluate-Model-13.png)

b) Results of Upsampled Decision Tree
![Results 1](images/Results-14.png)

c) Results of Normal Decision Tree
![Results 2](imagaes/Results-15.png)

### Task 6- Publish the Trained Models as Web Service for Inference

- Create a web service from Azure Machine Learning prediction model
- Create a scoring / prediction experiment
- Publish the trained model as a web service

a) Deleted Normal Decision Tree Before Creating Web Service
![Delete DT Model](images/Deleted-Normal-DT-16.png)

b) Web Service Output
![Web Service Output](images/Web-Service-Output-17.png)

c) Predicting New, Unseen Data on the Decision Tree Model
![Predicting New Data](images/New-Data-Prediction-18.png)

d) Prediction- Scored Label
![Actual Prediction](images/Model-Prediction-19.png)
