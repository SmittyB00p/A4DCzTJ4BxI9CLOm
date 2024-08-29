# Customer Satisfaction
This project looked to predict the satisfaction of customers of a food delivery service where the dataset was customers' survey responses; 6 features that corresponded to the 6 questions that they asked their customers with the answers being numeric values between 1 and 5 where 1 was a minimum satisfaction level and 5 was the maximum satisfaction level. Finding the most relevant features was a necessity as well so as to better evaluate the satisfaction of customers. 

## Exploratory Data Analysis
The initial phase of the project was to look at the dataset and see that the values corresponded to the values that were laid out by the company (1-5) as well as check for missing values and ultimately look at the descriptive statistics.
The next thing I wanted to do was to look at the distribution of the two classes and to also see if there were any differences between their average and median scores.
* The distribution of the satisfied and non-satisfied customers were fairly evenly distributed (1 ~ 55% and 0 ~ 45%)
* The scores were what I expected in that the satisfied customers had higher averages than the non-satisfied customers
* The one thing that I found interesting and concerning, especially for a food delivery service, was that the question 'contents of my order was as I expected' averaged a score of ~ 2.5 for both classes of customers...something to look at going forward.
The last thing I wanted to check for was any correlation between features and with the highest correlation being in the low 40's I could safely say that all the features could be used in model experimentation.

## Modeling
With both classes being equally important to the company and their goal of predicting what makes customers satisfied, the recall metric was chosen as the best metric to track for model performance. 
Using LazyPredict's LazyClassifier method I was able to get a good idea for the algorithms to try and experiment with:
  * Logistic Regression - base model for classification
  * LinearSVC - popular linear model used for classification
  * XGBoost - tree based model with proven record with classification
  * KNeighbors - popular model to use for classification using the average radius of each data point
  * GaussianNB - model that assumes features are Gaussian or evenly distributed (4 of 6 are Gaussian in our case)
Added later were Random Forest Classifier and SVC due to randomness

That randomness was later used to find the best recall scores for the respective models...if anyone knows of a way to automate this process, that would greatly appreciated!

The models that performed the best in that iterative process of finding the seed were GaussianNB, LinearSVC, XGBoost, and RandomForest
