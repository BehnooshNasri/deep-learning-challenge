# deep-learning-challenge

### Frist Optimization

- Dropped two more columns: "SPECIAL_CONSIDERATIONS" and "STATUS"
- Adjusted the cutoffs for both "APPLICATION_TYPE" and "CLASSIFICATION"
- Added a third hidden layer
- Not a significant change in accuracy and loss

### Second Optimization

- Put back the two previously dropped columns: "SPECIAL_CONSIDERATIONS" and "STATUS"
- Re-adjusted the cutoffs
- Changed the activation function of all the layers to "relu"
- Increased the epochs to 200
- loss increased and accuracy declined (not a significant amount)

### Third Optimization 

- Automate the Neural Network to get a more accurate model 
- Use keras tuner
- run time was very long so early stopping was used as a callback to move on if there was no improvements
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

- Accuracy and loss were still did not significantly change

