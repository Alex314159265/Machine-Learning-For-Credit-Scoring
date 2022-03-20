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

### Session 4 (20/03/22)

We created the latex report on overleaf. We did the structure of the report, the introduction, the team and the data presentation. 

We did a qualitative study of the parameters. The idea is to delete parameters which are useless but it is only for those we can predict it before doing a correlation study. It can be because of their nature (member id carries no information for the grades) or because of their quality (title is a sentence written by the borrower, it is not usable for a regression).
We wrote that part in the report and we did the code on Python.

We discussed about the way we dealt with missing values and we want to change that to keep more usefull parameters.

Notes :

We are not sure to remove the attribute 'title'
