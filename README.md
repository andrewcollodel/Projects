# Projects
Projects completed successfully using public datasets 

## About the projects
Each project has been completed as part of my learning for a L6 Data Science degree and apprenticeship. Each project was undertaken to learn specific skills as showcased in this repository. 

### Project 1: Using Ordinary Least Squares Regression to predict predict housing prices

This project is adapted from Source https://www.nickmccullum.com/python-machine-learning/linear-regression-python/
This notebook uses a randomly generated dataset to build a linear regression model that predicts housing prices

The purpose of this project is to predict housing based on area income, house age, average number of bedrooms, average number of rooms and area population.

#### Project 1: Conclusion
How good is this model? The metric indicate that this is a less than perfect model. The bedroom variable adds little value to the model. The best approach to evaluate this model would be to construct a second model with different predictor variables. Unfortunately this data set does not contain any other useful variables.

### Project 2: Classifying Data with Logistic Regression in Python

The purpose of this project is to predict if a borrower will default on their loan. The predictors are annual income and credit score, and the response is loan default.

Loan Approval Classification Dataset source information Synthetic Data for binary classification on Loan Approval

https://www.kaggle.com/datasets/taweilo/loan-approval-classification-data?resource=download

Observations about this dataset cited from the source in GitHub "This dataset is a synthetic version inspired by the original Credit Risk dataset on Kaggle and enriched with additional variables based on Financial Risk for Loan Approval data. SMOTENC was used to simulate new data points to enlarge the instances."

The dataset contains 45,000 records and 14 fields

#### Project 2: Conclusion
![Updated%20Boosted%20Confusion%20Matrix.jpg](attachment:Updated%20Boosted%20Confusion%20Matrix.jpg)

The first row of the matrix shows that of the $10,498$ instances, the model correctly predicted $9,778$ of them as `Yes` but incorrectly predicted $720$ as `Yes`when they should have been `No`. The second row of the matrix shows that of the $3,000$ instances the model correctly predicted $1,685$ as `No` but incorrectly predicted 1,315 false negatives.  

Correct predictions: 9,778 + 1,685 = 11,463 <span style="color:green">**(85% of predictions correct)**.</span>  

Incorrect predictions: 1,315 + 720 =  2,035 <span style="color:red">**(15% of predictions incorrect)**.</span>  

Total Predictions:                 = 13,498
