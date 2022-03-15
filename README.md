# Machine-Learning-For-Credit-Scoring
TER Project, M1, Alexandre BONICEL, Gabriel OLLIER, Lucas BLANCHETON


Session 1 (02/03/22):

We create a GitHub repository to share our work.

We choose our dataset on Kaggle: https://www.kaggle.com/devanshi23/loan-data-2007-2014 .
It is a Dataset on different mortgage in the USA.



Session 2 (09/03/22):

First, we open the data and check for the base rate. In our model we will have 7 different outputs (A,B,C,D,E,F,G) so we expect a base rate of about 0.14 (1/7). Our current base rate is 0.17 and mostly the minimum rate is 0.01 for G. Our Dataset is not balanced so we need to change that.

There are 3322 observations for G so if we delete enough observations in the other groups we could have a balanced dataset and still more than 23254 observations (3322 x 7).
It is the strategy that we think to do.

We search for a function to randomly errase observations in our overrepresented groups.


Session 3 (15/03/22):

To begin with we want to remove the missing values. We tried to remove every rows with at least a missing value but it deleted the whole dataset. We decided to chage the strategy by deleting columns with missing value. It let us to easily remove many parameters which seemed .


Notes :

We are not sure to remove the attribute 'title'
