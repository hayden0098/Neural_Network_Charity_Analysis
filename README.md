# Neural_Network_Charity_Analysis

## Overview of the loan prediction risk analysis:
We are using neural networks to work to help the foundation predict where to make investments. we will use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

* EIN and NAME — Identification columns
* APPLICATION_TYPE — Alphabet Soup application type
* AFFILIATION — Affiliated sector of industry
* CLASSIFICATION — Government organization classification
* USE_CASE — Use case for funding
* ORGANIZATION — Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special consideration for application
* ASK_AMT—Funding amount requested
* IS_SUCCESSFUL—Was the money used effectively

## Results:
Data Preprocessing
  1. What variable(s) are considered the target(s) for your model?  
  
    column name "IS_SUCCESSFUL" is the target for the model.  
  2. What variable(s) are considered to be the features for your model?

    Every encode categorical columns, and value columns are consider as features for the model.
  3. What variable(s) are neither targets nor features, and should be removed from the input data?

    Columns that indicate name("NAME") and ID("EIN"), those are varbiales neither targets nor features 
    
Compiling, Training, and Evaluating the Model
  1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
  
    There are 2 hidden layers, 1st layer has 80 neurons with ReLu activation function, 2nd layer has 30 neurons also with ReLu activation.
    The output layer is made of unique neuron with sigmoid activation. We use ReLu for hidden layer becuase its simplifying the output, 
    we use Sigmod on output layer due to it transforms the output to a range between -1 and 1.  
    
   ![deep_leaning_model_summary](https://github.com/hayden0098/Neural_Network_Charity_Analysis/blob/main/screenshot/deep_leaning_model_summary.jpg)
    
  2. Were you able to achieve the target model performance?

    The accuracy of the model is around 0.7244, it's below 75% and its not meet the target performance predictive accuracy 
    to predict the outcome of charity donations.
  3. What steps did you take to try and increase model performance?
  
    We have added the third hidden layer, and increased the neurons in each layer; which 1st layer has 120, 2nd has 60 and 3rd has 20 nurons. 
    Also we changed the activation, uses leaky relu activation functions to improve the model performance. 
    After three attempts the accuracy of the model is 0.7257 still under 75% of target performance predictive accuracy.
    
## Summary: 
The deep learning model accuracy is around 0.7244, even we try to improve the performance of the model it still can not meet or over the target predictive accuracy 75%. Obviously, deep learning model is not outperform model, as recommendation since the dataset is the case of binary classification we can use random forest classifiers supervised machine learning instead, since its a type of ensemble leaning model taht combines multiple models into a more robust and accurate model, also its similar the neural network counterparts.
