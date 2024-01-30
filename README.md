# Advanced Data Analytics Capstone
### Overview
In this project, we were taksed with analyzing why an employee may be likely to leave the company in order to understand how to better retain employees. We were given a dataset with fields such as _tenure_, _satisfaction level_, and _salary_, and the information about whether an employee left the comapny or not. We used the PACE strategy to approach this task in a logical and structured manner. When analyzing the data, we used the principles of EDA. Finally, we constructed a random forest model to predict whether an employee would eave the company or not, getting an accuracy of 0.958.

### Tools used
* Pandas for working with datasets.
* Saeborn and Pyplot for plotting the data.
* Scikit-learn to prepare the data for training and for constructing a machine learning model.

### Problem
There can be a good reason for an employee wanting to leave the company, but it may also be caused by some underlying problem with the company, such as bad management, uncomfortable wrokplace, etc. Our goal is to understand whther there are such factors that make an employee leaving the company likely.

### Data  
Our data contains entries for 15000 employees. We removed approximately 3000 duplicated entries, but we kept outliers which are not a problem for the model we chose later. Only around 83% of the employees in the dataset did not leave, which is imbalanced, but not extremely.    
We visualized correlations between individual prpoerties and whether an employee left the company or not using barplots and pie charts. For example, the average satsfaction level of employees who left was much smaller, and those who left received much less promotions on average.   
![left promotion barplot](https://github.com/jonny9066/AdvancedDataAnalyticsCapstone/blob/main/promotion_left_barplot.png?raw=true)
This way we chose _tenure_, _promotion received_ and _satisfaction level_ as the most important factors and proceeded to build a model as a first attempt.

### Model and Metrics
We chose the random forest model because it makes sense to us intuitively, and we have seen in practice that it works well with problems of this sort. We split the data to train, test, and validation. We used the train and validation data to pick good parameters, and then we trained the model with the chosen parameters and tested it on the test data. We received an accuracy of 0.958, which we found satisfactory.



