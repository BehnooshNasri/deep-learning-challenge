# deep-learning-challenge

## Overview

The purpose of this module's challenge is to use deep learning models to predict whether applicants for a funding company called Alphabet Soup are successful.

The dataset provided is a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.

## Results

The preprocessing of the data for almost all the models is very similar. The only difference is in the optimizations, columns have been added or dropped and the cutoffs for binning have been adjusted. In the end, this practice did not really change the final results.

### Intial Model 

- The initial model uses 2 hidden layers. 
- Loss: 0.5651512742042542, Accuracy: 0.7297959327697754

### Frist Optimization

- Dropped two more columns: "SPECIAL_CONSIDERATIONS" and "STATUS".
- Adjusted the cutoffs for both "APPLICATION_TYPE" and "CLASSIFICATION".
- Added a third hidden layer.
- Increased loss and decreased accuracy (not a significant amount).
- Loss: 0.5995520353317261, Accuracy: 0.7285131216049194

### Second Optimization

- Put back the two previously dropped columns: "SPECIAL_CONSIDERATIONS" and "STATUS".
- Re-adjusted the cutoffs.
- Changed the activation function of all the layers to "relu".
- Increased the epochs to 200.
- Increased loss and decreased accuracy (not a significant amount).
- Loss: 0.720808744430542, Accuracy: 0.7273469567298889

### Third Optimization 

- Automated the Neural Network to get a more accurate model.
- Used keras tuner.
- Run time was very long so early stopping was used as a callback to move on if there were no improvements.
- Keras tuner best hyperparameters are:

""" {'activation': 'sigmoid',
 'first_units': 36,
 'num_layers': 3,
 'units_1': 16,
 'tuner/epochs': 100,
 'tuner/initial_epoch': 34,
 'tuner/bracket': 4,
 'tuner/round': 4,
 'tuner/trial_id': '0145'} """

- Loss decreased and accuracy increased. 
- Loss: 0.5561479330062866, Accuracy: 0.7337609529495239

## Summary 

In conclusion, the automated neural network optimization gave slightly improved results overall. The accuracy did not go above 75%. Perhaps the best way to get better results would be to preprocess the data better and add or drop more columns in the dataset that would give a better shape to our data.


