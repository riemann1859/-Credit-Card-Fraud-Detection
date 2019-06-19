


Context\
It is important that credit card companies are able to recognize fraudulent credit card transactions so that customers are not charged for items that they did not purchase.

Content\
The datasets contains transactions made by credit cards in September 2013 by european cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

It contains only numerical input variables which are the result of a PCA transformation. Unfortunately, due to confidentiality issues, we cannot provide the original features and more background information about the data. Features V1, V2, ... V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-senstive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.

We can consider fradulent transactions as outliers and try to detect them via Local Outlier Factor(LOF) or Isolation Forest(IF) algorithms. These methods produce  poor results by themselves. Our strategy is that employing the mentioned outlier detection methods as a part of feature engineering and then applying oversampling to make the training data much more balanced and finally apply random forest algorithm.
As a result, on test data we have 0.999 accuracy score, which means almost all predictions are true, and 0.897 recall score, which means 
we catch almost 9 out of every 10 fradulent transactions, which is of course more significant than overall accuracy. 
