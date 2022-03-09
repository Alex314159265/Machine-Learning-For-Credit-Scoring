# Machine-Learning-For-Credit-Scoring
TER Project, M1, Alexandre BONICEL, Gabriel OLLIER, Lucas BLANCHETON

Session 1:

To completed (gab)

Session 2:

First, we open the data and check for the base rate. In our model we will have 7 different outputs (A,B,C,D,E,F,G) so we expect a base rate of about 0.14 (1/7). Our current base rate is 0.17 and mostly the minimum rate is 0.01 for G. Our Dataset is not balanced so we need to change that.

There are 3322 observations for G so if we delete enough observations in the other groups we could have a balanced dataset and still more than 23254 observations (3322 x 7).
It is the strategy that we think to do.

We search for a function to randomly errase observations in our overrepresented groups.
