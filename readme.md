# Deep learning challenge
## Overview
Using a CSV file containing more than 34000 organizations that have received funding from a fictional foundation over the years, we are supposed to create a multilayered neural network that predicts whether an application will be successful.  
The CSV has the following columns:
* `EIN` and `NAME`—Identification columns  
* `APPLICATION_TYPE`—Alphabet Soup application type
* `AFFILIATION`—Affiliated sector of industry
* `CLASSIFICATION`—Government organization classification
* `USE_CASE`—Use case for funding
* `ORGANIZATION`—Organization type
* `STATUS`—Active status
* `INCOME_AMT`—Income classification
* `SPECIAL_CONSIDERATIONS`—Special considerations for application
* `ASK_AMT`—Funding amount requested
* `IS_SUCCESSFUL`—Was the money used effectively

## Results
## Data Preprocessing

* Targets: `IS_SUCCESSFUL`
* Features: 
    * Categorical: `APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT`
    * Numerical: `ASK_AMT`
    * Binary: `STATUS, SPECIAL_CONSIDERATIONS`
* Variables to be removed: `EIN` and `NAME`


## Compiling, Training, and Evaluating the Model

* How many neurons, layers, and activation functions did you select for your neural network model, and why?  
    * For the first try, I used 84 nodes, then 21 and the final layer with 1 output. Relu activation was used for the input and hidden layer. The output used sigmoid activation.  The model was trained for 100 epochs
* Were you able to achieve the target model performance?  
    * These settings lead to a **72.12%** accuracy. Several optimization tools were used but the accuracy wouldn't go a lot higher.
* What steps did you take in your attempts to increase model performance?  
    * Increased epochs: **72.23%**
    * More nodes and mixed activation: **72.33%**
    * Extra hidden layer: **72.39%**
    * All of these methods together: **72.06%**
## Summary  
The results are not very promising, given that an accuracy this low shouldn't be trusted. The model could be improved engineering the features, deleting the ones that could be offuscating the results, or making sure that the model is being fed enough examples of successful and unsuccessful datapoints.