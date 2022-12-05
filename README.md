## Overview of the analysis:
---------------
The purpose of this analysis is to analyze the impact of each donation and vet potential recipients. This helps ensure that the foundations money is being used effectively. The goal here is to help decide which organizations are worth donating to and which are too "high risk" by creating a mathematical data driven solution that can do this accurately. The Tensor-Flow library will be used to design and train a deep-learning neural network for this analysis. 

## Results
--------------
*Data Preprocessing*

***Target***
---------------
>IS_SUCCESSFUL 
>>Was the foundations money used effectively?



***Features*** 
---------------
- EIN and NAME = Identification columns
- APPLICATION_TYPE = Alphabet Soup application type
- AFFILIATION = industry sector
- CLASSIFICATION = Government organization 
- USE_CASE = Reason for funding
- ORGANIZATION = Organization type
- STATUS = Active status
- INCOME_AMT = Income amount
- SPECIAL_CONSIDERATIONS = Special consideration for application (y/n)
- ASK_AMT = Funding amount requested


>Variables that are neither targets nor features, and should be removed from the input data: 

Before optimization: EIN and NAME were dropped

<img width="1033" alt="dropEIN" src="https://user-images.githubusercontent.com/106992995/205575553-e3975743-22ad-47a4-ae31-46a913514aeb.png">


**Compiling, Training, and Evaluating the Model**
-------------------

Resulted with 2 hidden layers. 
- [x] Hidden layer #1 = 80 neurons
- [x] Hidden layer #2 = 30 neurons

- [x] Used RELU activation for both hidden layers

- [x] SIGMOID activation for the output layer (1:successful and/or 0:unsuccessful)

- [x] Accuracy: 0.7687 or 76.87%
<img width="644" alt="resultdata" src="https://user-images.githubusercontent.com/106992995/205578762-847e4734-2b67-4dde-8113-950d6d1e7d28.png">



