# Income Prediction with Azure ML Studio

Using the Adult Census data, I will build two boosted decision tree models (one model will be trained on the upsampled data, and the other with just the original pre-processed data) and create an end-to-end pipeline using Azure ML Studio. The objectives are the following:

- Pre-process the data
- Train and evaluate the model with Azure ML Studio
- Create scoring and predictive experiments
- Deploy the trained model as an Azure web service

### Task I- Introduction and Overview

- Create a new experiment from the Azure ML Studio dashboard
- Import and explore the Adult Census data before moving on to pre-processing

### Task 2- Data Cleaning

- Clean the data
- Handle missing values
- Exclude irrelevant or redundant columns
- Once the final set of features is ready, use the Edit Metadata module to convert specific columns from string to categorical

### Task 3- Accounting for Class Imbalance

- Upsample the data, but only on the training data so that none of the information in the validation data is used to create synthetic observations. So these results should be generalizable.

### Task 4- Model Training and Hyperparameter Tuning

- Train a two-class boosted decision tree model to predict the income
- Perform hyperparameter tuning using the Tune Model Hyperparameters module

### Task 5- Scoring and Evaluating Models

- Compare how the two models perform using the Score Model and Evaluate Model modules
- Use AOC and ROC metrics for evaluation

### Task 6- Publish the Trained Models as Web Service for Inference

- Create a web service from Azure Machine Learning prediction model
- Create a scoring / prediction experiment
- Publish the trained model as a web service

