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


Using classification techniques, ensemble techniques, and dimensionality reduction, this project looked to find the optimal model to classify both satisfied and unsatisfied customers as well as find the optimal number of features to use where the model would not loose out on the performance metric (recall).
