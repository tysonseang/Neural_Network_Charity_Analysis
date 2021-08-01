# Neural_Network_Charity_Analysis


## Overview of the Analysis
The purpose of this analysis is to help a nonprofit foundaiton, Alphabet Soup, analyze the impact of its previous donations and vet potential recipients in order to ensure the foundation's resources are being used effictely. The philanthropic foundation is a prolific donor that has raised and donated over 10 billion dollars and funded more than 34,000 organizations over the years. In order to analyze data at this scale, a deep learning neural network with a binary classifier was developed that is capable of prediciting whether an applicant's mission will be successful if funded by the foundation. 

To complete this task, I used Python's TensorFlow library, Pandas, Jupyter Notebook, and a CSV file containing data on each of the 34,000+ orgnizations, to include:
- EIN and NAME — Identification columns
- APPLICATION_TYPE — Alphabet Soup application type
- AFFILIATION — Affiliated sector of industry
- CLASSIFICATION — Government organization classification
- USE_CASE — Use case for funding
- ORGANIZATION — Organization type
- STATUS — Active status
- INCOME_AMT — Income classification
- SPECIAL_CONSIDERATIONS — Special consideration for application
- ASK_AMT — Funding amount requested
- IS_SUCCESSFUL — Was the money used effectively


## Results

### Data Preprocessing
- **What variable(s) are considered the target(s) for your model?**
Target variable: 'IS_SUCCESSFUL' 

- **What variable(s) are considered to be the features for your model?**
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

- **What variable(s) are neither targets nor features, and should be removed from the input data?**
Dropped variables: 'EIN', 'NAME', 'SPECIAL_CONSIDERATIONS', 'INCOME_AMOUNT'

### Compiling, Training, and Evaluating the Model
- **How many neurons, layers, and activation functions did you select for your neural network model?**
Finale_model:
![final_model](https://github.com/tysonseang/Neural_Network_Charity_Analysis/blob/main/Resources/final_model.png)

- **Were you able to achieve the target model performance?**
My most successful model received an accuracy of roughly 73%. 

- **What steps did you take to try and increase model performance?**
    - Added a hidden layer
    - Updated Other bin cut off for 'APPLICATION_TYPE' to < 5
    - Updated Other bin cut off for 'CLASSIFICATION' to < 750
    - Attempted various neuron counts for each hidden layer


## Summary
My most successful model had 3 hidden layers with 80, 40, and 15 neurons. I use ReLU and Sigmoid activation functions, and earned an accuracy score of 72.5%%. This was a significant imrpovement over my original model, which had a higher loss and lower accuracy score (61.7%). 

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

