In this project, I implemented a model to calculate the likelihood of a person obtaining a loan based on certain criteria found in a .csv file.

First, I checked for missing values in the dataset. If a column has too many missing values (more than 50% of examples), I exclude that column. If there are fewer missing values, I replace them with the column's mean for numerical data or the most common value for categorical data. I also check if the acceptance/rejection rate is significantly higher than the rejection/acceptance rate, as a major imbalance could cause issues for the model.

I normalize the 'LoanAmount' column and transform categorical data into numerical data.

I test logistic regression and KNN for this problem. I observe that the logistic regression model performs better, so I optimize its hyperparameters. Given the number of columns, I use the RandomizedSearchCV technique for more efficient optimization. I optimize 'C' - the regularization parameter, the regularization technique, and the optimization algorithm. I then rerun the model with the best hyperparameters and achieve an accuracy of 0.88 for loan denials and 0.83 for approvals. The average accuracy, considering the number of examples for each case, is 0.84.
