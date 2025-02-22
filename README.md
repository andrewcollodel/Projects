# Projects
Projects completed successfully using public datasets 
___
## About the projects
Each project has been completed as part of my learning for a L6 Data Science degree and apprenticeship. Each project was undertaken to learn specific skills as showcased in this repository. 
___
# Project 1: Using Ordinary Least Squares Regression to predict predict housing prices
___
#### About this project
This project is adapted from Source https://www.nickmccullum.com/python-machine-learning/linear-regression-python/
This notebook uses a randomly generated dataset to build a linear regression model that predicts housing prices

The purpose of this project is to predict housing based on area income, house age, average number of bedrooms, average number of rooms and area population.

#### Conclusion
How good is this model? The metric indicate that this is a less than perfect model. The bedroom variable adds little value to the model. The best approach to evaluate this model would be to construct a second model with different predictor variables. Unfortunately this data set does not contain any other useful variables.

#### Explore Project 1: 
[Link to Project 1 Notebook](https://github.com/andrewcollodel/Projects/blob/main/01%20House_prices_OLS_Project.ipynb)

___
# Project 2: Classifying Data with Logistic Regression in Python
___
#### About this project
The purpose of this project is to predict if a borrower will default on their loan. The predictors are annual income and credit score, and the response is loan default.

Loan Approval Classification Dataset source information Synthetic Data for binary classification on Loan Approval

https://www.kaggle.com/datasets/taweilo/loan-approval-classification-data?resource=download

Observations about this dataset cited from the source in GitHub "This dataset is a synthetic version inspired by the original Credit Risk dataset on Kaggle and enriched with additional variables based on Financial Risk for Loan Approval data. SMOTENC was used to simulate new data points to enlarge the instances."

The dataset contains 45,000 records and 14 fields

#### Conclusion

![Updated Boosted Confusion Matrix](https://github.com/user-attachments/assets/ec6fe5bb-b066-4b39-8d91-869db4bdbe29)

The first row of the matrix shows that of the $10,498$ instances, the model correctly predicted $9,778$ of them as `Yes` but incorrectly predicted $720$ as `Yes`when they should have been `No`. The second row of the matrix shows that of the $3,000$ instances the model correctly predicted $1,685$ as `No` but incorrectly predicted 1,315 false negatives.  

Correct predictions: 9,778 + 1,685 = 11,463 <span style="color:green">**(85% of predictions correct)**.</span>  

Incorrect predictions: 1,315 + 720 =  2,035 <span style="color:red">**(15% of predictions incorrect)**.</span>  

Total Predictions:                 = 13,498

#### Explore Project 2:
[Link to Project 2 Notebook](https://github.com/andrewcollodel/Projects/blob/main/02%20Logistic_Regression_Loans.ipynb)
___
# Project 3:  NYC Bridge Crossings - Poisson regression model
___
#### About this project
This project was developed to learn Poisson regression and is adapted from the source cited below. The dataset is also available in Kaggle
Poisson regression model for regressing the bicyclist counts observed on the Brooklyn bridge between 01 April 2017 and 31 October 2017.
Source: https://timeseriesreasoning.com/contents/poisson-regression-model/
The project starts with the Poisson regression model and use it as the “control” for the Negative Binomial regression model in part 2 of this project. Cameron and Trivedi recommend best practice is to estimate both Poisson and Negative Binomial regression models (Cameron and Trivedi, 2013).
This project is continued in Project 4 where the Negative Binomial regression model is developed

#### Conclusion
The model appears to be tracking the trend in the actual counts. 
<span style="color:red">However</span> a significant number of the <span style="color:red">**predictions are inaccurate**</span> when compared to the actual value.

**Interpretation of this model’s statistics** 
* Deviance: 	24266.0
* Pearson chi2:	2.43  
The above to values are very large and a good fit unlikely (despite the reasonable plot).  
* DF Residuals 	= No. Observations minus DF model
                		= 179 – 6 = 173	
At p=0.05 and DF Residuals = 173, the chi-squared value (chi2) from a standard Chi-Squared table is 224.660
 (Source: https://www.medcalc.org/manual/chi-square-table.php ). 
This value is much smaller than this model’s reported Deviance = 24266 and Pearson chi2 = 24300. Therefore despite a reasonable visual fit or the test data the fit is statistically poor. (Source: https://timeseriesreasoning.com/contents/poisson-regression-model/ )

#### Explore Project 3: 
[Link to Project 3 Notebook](https://github.com/andrewcollodel/Projects/blob/main/03%20Poission_Bike_NYC.ipynb)
___
# Project 4: Classifying Exam Results with Logistic Regression in Python
___
#### About this project
The purpose of this project is to predict if a student will pass their exams based on an average pass rate of 60% (60% and above = pass below 60% is a fail) as this is the minimum requirement at prestigious Universities . The predictors are gender, ethnicity, preparation, lunch and parent’s education. The response is Year Result (pass or fail).
Students Performance in Exams Dataset source information
https://www.kaggle.com/datasets/spscientist/students-performance-in-exams/code?datasetId=74977&sortBy=voteCount&language=Python 
The dataset contains 1,000 records and 8 fields

#### Conclusion

The confusion matrix is illustrated as follows:  
  
![Exam Confusion Matrix](https://github.com/user-attachments/assets/cf534d6e-634d-4dda-a4cf-6eca570e7b09)
  
The first row of the matrix shows that of the `300` instances, the model correctly predicted `22` of them as `Yes` but incorrectly predicted `64` as `Yes`when they should have been `No`. The second row of the matrix shows that of the `300` instances the model correctly predicted `200` as `No` but incorrectly predicted `14` false negatives.  
<span style="color:green">Correct predictions:   200 + 22 = 222 (74% of predictions correct).</span>  
<span style="color:red">Incorrect predictions: 64 + 14 =  78 (26% of predictions incorrect).</span>  
Total Predictions:             = 300

#### Explore Project 4: 
[Link to Project 4 Notebook](https://github.com/andrewcollodel/Projects/blob/main/04%20Predicting%20exam%20results%20logistic%20regression.ipynb)
___
# Project 5: Using Polynomial Regression to predict Co2 emissions based on city mpg
___
#### About this project
This project uses a historical dataset to build a linear regression model that predicts Co2 emissions based on city mpg.

#### Conclusion  
**Result Test1:** Medium 14 mpg city - predicts 562.75 under reporting by 1.33%  

**Result Test 2:** High 40 mpg city - predicts 193.64 under reporting by 11.55%  

**Result Test 3:** Low 7 mpg city - predicts 1006.78 under reporting by 8.95%  

**Statistical tests**  
Mean squared error: 618.79  
R-squared: 0.96 (96%)  
The model has improved but may lack sufficient predictor variables.

#### Explore Project 5: 
[Link to Project 5 Notebook](https://github.com/andrewcollodel/Projects/blob/main/05%20Vehicle_Polynomial_Regression%20VERSION%202.ipynb)
