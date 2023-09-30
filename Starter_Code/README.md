# Alphabet Soup Neural Model Report

# Contributors
Jeffrey Robertson

# Overview

The purpose of this analysis was to determine what patterns an commonalities were shared among successful and unsuccessful application.  The goal was to be able to get an accurate model to evaluate applications likelihood of success

# Results

## Data Preporcessing
### Target Variable
- The target variable was if based on the project was successful.  We wanted the model to be able to predict whether or not an application would be successful and that was the most appropriate choice 

### Features
- The features we used were the application type, classification, affiliation, use case, organization and income amount.  First we determined how many of each type of variable each feature held. Then we binned the data to reduce the size of a data and the amount of rows that held to few data types to evaluate appropriately.  For application type the cut off was set to any equal or greater than 700.  This left us with 8 unique application types with all others classified as 'other.  We did the same for Classification type and set the threshold at 1800 or above.  That left the dataset with 7 unique classification types

### Removed Data
- We did not include special considerations or status.  Status would have the potential to bias the data as ongoing projects might not have reached the point where it can be determined successful.  For special considerations, I was unaware of what those considerations were, so felt it would be best to not include it as most did not receive them

## Creating, training and optimizing the model
### Neurons Layers and activation functions
-   The initial model had 4 hidden layers.  The first had 9 units with the activation of reLU.  The second had 9 units and third had 5 and the the fourth had 3.  The output layer used tanh method as the final activation
### Target Performance
- The model did not achieve an accuracy of 75% either in the initial training or in the optimization.  To attempt to increase the accuracy, in the optimization, we increased the threshold for values to bin and changed the final activation to sigmoid but it didn't achieve target accuracy.

# Summary
- There was a significant loss of data in the performance of the model and the accuracy was only 73% after optimization.  If the number of epochs was increased then it might lead better accuracy but would require more computational power.
- The use of of Convulutional Neural Network or a Restricted Boltzmann Machine if they wish to evaluate the probability distribution of the likelihood of success for the applications