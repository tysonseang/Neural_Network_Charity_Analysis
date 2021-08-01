# Neural_Network_Charity_Analysis

## Overview of the Analysis
Explain the purpose of the analysis

## Results

### Data Preprocessing
- What variable(s) are considered the target(s) for your model?
Target variable: 'IS_SUCCESSFUL' 

- What variable(s) are considered to be the features for your model?
Features: 'STATUS', 'ASK_AMT', 'APPLICATION_TYPE_Other',
       'APPLICATION_TYPE_T19', 'APPLICATION_TYPE_T3', 'APPLICATION_TYPE_T4',
       'APPLICATION_TYPE_T5', 'APPLICATION_TYPE_T6',
       'AFFILIATION_CompanySponsored', 'AFFILIATION_Family/Parent',
       'AFFILIATION_Independent', 'AFFILIATION_National', 'AFFILIATION_Other',
       'AFFILIATION_Regional', 'CLASSIFICATION_C1000', 'CLASSIFICATION_C1200',
       'CLASSIFICATION_C2000', 'CLASSIFICATION_C2100', 'CLASSIFICATION_C3000',
       'CLASSIFICATION_Other', 'USE_CASE_CommunityServ', 'USE_CASE_Heathcare',
       'USE_CASE_Other', 'USE_CASE_Preservation', 'USE_CASE_ProductDev',
       'ORGANIZATION_Association', 'ORGANIZATION_Co-operative',
       'ORGANIZATION_Corporation', 'ORGANIZATION_Trust'

- What variable(s) are neither targets nor features, and should be removed from the input data?
Dropped variables: 'EIN', 'NAME', 'SPECIAL_CONSIDERATIONS' and 'INCOME_AMOUNT'

### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?

- Were you able to achieve the target model performance?
My best model received an accuracy of XX% with a loss of 

- What steps did you take to try and increase model performance?
Added hidden layers
Updated Other bin cut off for 'APPLICATION_TYPE' to < 5
Updated Other bin cut off for 'CLASSIFICATION' to < 750

## Summary
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.

Model 1:
Loss: 0.9341922402381897, Accuracy: 0.617959201335907
![model_1](https://github.com/tysonseang/Neural_Network_Charity_Analysis/blob/main/Resources/model_1.png)

Model 2:
Loss:1.4600861072540283, Accuracy: 0.5355101823806763
![optimization_attemp1](https://github.com/tysonseang/Neural_Network_Charity_Analysis/blob/main/Resources/optimization_attemp1.png)


Model 3:
Loss:0.5521408915519714, Accuracy: 0.7250145673751831
![optimization_attempt2](https://github.com/tysonseang/Neural_Network_Charity_Analysis/blob/main/Resources/optimization_attempt2.png)

Mdel 4:
Loss:0.5521408915519714, Accuracy: 0.7250145673751831
![optimization_attempt3](https://github.com/tysonseang/Neural_Network_Charity_Analysis/blob/main/Resources/optimization_attempt3.png)