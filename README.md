# Neural_Network_Charity_Analysis

With my knowledge of machine learning and neural networks, in the provided dataset I will help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

I first preprocessed the data, then compiled, trained, and evaluated the model. Finally, the model was optimized in three ways in an attempt to reach an accuracy of 75% or greater.

## Resources

- Jupyter Notebook 6.4.5

## Results 

- Data Processing
  - What variable(s) are considered the target(s) for your model? IS_SUCCESSFUL
  - What variable(s) are considered to be the features for your model? APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, PECIAL_CONSIDERATIONS, ASK_AMT
  - What variable(s) are neither targets nor features, and should be removed from the input data? EIN, NAME (SPECIAL_CONSIDERATIONS removed during one optimization attampt)

- Compiling, Training, and Evaluating the Model
  - How many neurons, layers, and activation functions did you select for your neural network model, and why? The initial model includes a single input features and two hidden layers. The first hidden layer has 50 neurons, the second has 25. Additionally, each of the hidden layers employed the "relu" activation method, the output layer I used the "sigmoid" activation.
  - Were you able to achieve the target model performance? I reached almost 73.1% accuracy.
  - What steps did you take to try and increase model performance?
    1. First attempt: Reduced the application_counts to less than 500 and the classification_counts to less than 800; increased neurons to 80 and 30 respectively.
    2. Second attempt: Dropped SPECIAL_CONSIDERATIONS for the prevalance of "N" for the value, returned application_counts to less than 700 and classification_counts to less than 1800; returned hidden layers to original values. Then added a third hidden layer with 25 neurons.
    3. Third attempt: Dropped the third hidden layer and changed the activation method for the output layer to "tanh"

## Summary

After optimizing the data set 3 times I was unable to reach 75% accuracy. The Random Forest Classifier may work better with this supervised machine learning model. Perhaps dropping a different feature would lead to a higher accuracy.
