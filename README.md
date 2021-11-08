# Neural_Network_Charity_Analysis
Module 19

## Overview
Create a binary classifier that is capable of predicting whether applicants will be successful if funded by AlphabetSoup.


## Results
### Deliverable 1:  Data Preprocessing
- What variable(s) are considered the targets for your model?
    - The target variable is:  IS_SUCCESSFUL
    - returned values are 0 or 1
- What variable(s) are considered to be the features for your model?
    - All other variables besides IS_SUCCESSFUL.  There are 44 columns. Categorical columns were broken out using OneHotEncoder, producing many more columns.  The Primary columns are:
        - APPLICATION_TYPE
        - AFFILIATION
        - CLASSIFICATION
        - USE_CASE
        - ORGANIZATION
        - STATUS
        - INCOME_AMT
        - SPECIAL_CONSIDERATIONS
        - ASK_AMT

- What variable(s) are neither targets nor features, and should be removed from the input data?
    - We removed the following columns:
        - EIN
        - NAME

### Deliverable 2:  Compiling, Training and Evaluating the Model
- How many neurons, layers and activation functions did you select for your neural network model, and why?
    - I started with 2 layers and 100 neurons each, using 'relu' activation.  We had 44 columns of input and it's suggested to use 2-3 times that number for neurons.
        - loss ~ 50%, accuracy ~ 72%
    - I added a 3rd layer and increased neurons to 150 each
        - loss ~ 50%, accuracy ~ 72%
    - I changed the activation to 'tanh'
        - loss ~ 50%, accuracy ~ 72%
- Were you able to achieve the target model performance?
    - No, after modifying the number of layers, neurons and activation function, I was never able to increase the performance accuracy
- What steps did you take to try and increase model performance?
    - As mentioned above, I changed the number of layers, neurons and activation function.  I even went smaller, and changed to 50 neurons in each layer.  It never made any difference in the loss and accuracy.


## Summary
- overall results of the deep learning model
    - Overall, we were never able to reach the target accuracy of 75%.  Numerous attempts did not change the outcome at all
- recommendation for how a different model could solve this classification problem
    - Using a different model entirely could change the outcome.  We are using a deep neural network model.  We could use a machine learning model such as Random Forest Classifier.  This model reduces risk of overfitting and accuracy is much higher.
