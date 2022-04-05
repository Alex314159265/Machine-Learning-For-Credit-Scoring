# Machine-Learning-For-Credit-Scoring
TER Project, M1, Alexandre BONICEL, Gabriel OLLIER, Lucas BLANCHETON


### Session 1 (02/03/22):

We create a GitHub repository to share our work.

We choose our dataset on Kaggle: https://www.kaggle.com/devanshi23/loan-data-2007-2014 .
It is a Dataset on different mortgage in the USA.



### Session 2 (09/03/22):

First, we open the data and check for the base rate. In our model we will have 7 different outputs (A,B,C,D,E,F,G) so we expect a base rate of about 0.14 (1/7). Our current base rate is 0.17 and mostly the minimum rate is 0.01 for G. Our Dataset is not balanced so we need to change that.

There are 3322 observations for G so if we delete enough observations in the other groups we could have a balanced dataset and still more than 23254 observations (3322 x 7).
It is the strategy that we think to do.

We search for a function to randomly errase observations in our overrepresented groups.


### Session 3 (15/03/22):

To begin with we want to remove the missing values:
We tried to remove every rows with at least a missing value but it deleted the whole dataset. We decided to change the strategy by deleting columns with missing value. It is 'less professional' but it is an easy way to remove many parameters which seemed useless while keeping the same number of observations.

Then we balance the dataset:
There are many way to achieve that and we choose to do it randomly. Our idea is to randomly delete enough observations for each grade to balance the dataset.
To do it we split our dataset into 7 datasets, one for each group. Then we randomly erase the richt number for each grade (our target is to get about 3322 rows for each grade). 
It is very long to run when we delete rows one by one (about 3h).
To deal with that problem, we delete rows ten by ten (about 15 min).
After that we concatenate the 7 new dataframes and we get one new balanced dataset.
Finally we dowload our new dataset so we can take it next time without running the 15 min code.

We used some resources:
https://machinelearningmastery.com/tactics-to-combat-imbalanced-classes-in-your-machine-learning-dataset/
https://www.delftstack.com/fr/howto/python-pandas/split-pandas-dataframe/

### Session 4 (20/03/22):

We created the latex report on overleaf. We did the structure of the report, the introduction, the team and the data presentation. 

We did a qualitative study of the parameters. The idea is to delete parameters which are useless but it is only for those we can predict it before doing a correlation study. It can be because of their nature (member id carries no information for the grades) or because of their quality (title is a sentence written by the borrower, it is not usable for a regression).
We wrote that part in the report and we did the code on Python.

We discussed about the way we dealt with missing values and we want to change that to keep more usefull parameters.

### Session 5 (22/03/22):

we dealt with missing values. First we deleted columns with more than 10% of missing values. Then we droped rows with missing values. That process let us to keep more columns without leaving too many features.
We explained that part in the report.

We dealt with dates to change their form. Then we began to explain the process in the report.

We also explain how we balanced the dataset in the report.

We began to do the correlation matrix for the quantitative study of our features.

### Session 6 (30/03/22):

We changed the structure of the report according to what Jiao Yind told us. It is less technical and more explcative. The technical part is now in the annex part. We began to write the new parts.

We continued the data cleaning.

### Session 7 (31/03/22):

We finished the data cleaning. We did the Khi2 test for the categorical values and the correlation test for the numerical values. The goal was to remove every correlated values. We also factorized categorical values and normalized numerical values.

Then we prepare the cleaned data set for the classification. We splitted it in two parts : the train set and the test set.

We did four classification methods :

- logistic classification
- KNN classification (we found the best parameters)
- decision tree classification (we found the best depth)
- random forest classification

For each classification we computed the accuracy plotted the confusion matrix.

Finally we plotted the accuracies to compare the methods, we concluded that random forest is the best method.

### Session 8 (04/04/22):

We had an accuracy too high for decision tree and random forest (more than 90%). It shew a problem in our models. We found a perfectly correlated variable (interest rate). We removed it otherwise our model was cheated. We did the classifications again and we found our best accuracy of 48% for random forest. It is more realistic for a 7 labels model.

### Session 9 (05/04/22):

We seriously do the report. It should be finished soon!

