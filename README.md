# Neural_networks  
Following is a summary of my model generation and analysis for this assignment.  
(1) read charity_data.csv  
(2) From the data, the target variable is "IS_SUCCESSFUL"  
(3) There are 8 columns with categorical data.  
(4) A review of unique types shows that "Classification" has 71 unique types. I dropped this feature from the model since it is not likely to have any predictive value. I also dropped Statis, EIN, and Name features as they are not likely to be predictive.  
(5) The feature "Application_type" has 17 unique values. I retained it since this feature is likely to impact a successful outcome.  
(6) Ran one-hot encoder on the modified dataframe, excluded old columns and merged encode columns as the base df for model training  

## Deep neural network  
(7) I ran the neural network with 8 nodes in layer_1 and 5 in layer_2. The model accuracy is low at 0.53317.  
(8) I tried changing the following steps to improve the accuracy.  
- Excluding rows with income=0 improved the model accuracy to 0.59. However, that's not a reliable change since 2/3 of the data includes applications with 0 income.  
- Changing the number of layers did not change the accuracy significantly.  

## Single layer network  
(9) I generated a single layer model to evaluate if there would be any improvement.  
(10) The model accuracy improved significantly to 0.6946.  
(11) This shows that the additional layers were not improving performance with respect to this data set.
