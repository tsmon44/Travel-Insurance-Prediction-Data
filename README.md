# Travel Insurance Prediction Data

## Predict Whether A Customer Will Be Interested In Buying Travel Insurance
A Tour & Travels Company is offering travel insurance package to their customers. The new insurance package also includes covid cover. The company requires to know the which customers will be interested to buy it based on its database history. The insurance was offered to some of the customers in 2019 and the given data has been extracted from the performance/sales of the package during that period.

The data is provided for almost 2000 of its previous customers. A Tour & Travel company requests to create a machine learning model that can predict if customers will be interested in buying a travel insurance package based on certain parameters.
  
## Dataset Sources
Source : https://www.kaggle.com/datasets/tejashvi14/travel-insurance-prediction-data?datasetId=1457162&searchQuery=acc

## Project Goals
- To predict the purchase rate of travel insurance packages.
- Knowing what kind of customers will be interested in buying the travel insurance.
- To make a recommendation in order to increase the purchase of travel insurance.

## Machine Learning Model
The modeling that will be used aims to predict whether customers will be interested in buying a travel insurance package based on certain parameters. The target variable to be used is TravelInsurance. To reduce prediction errors (False Positive), then choose a high precision value. Classification Task :

- False Positive: It is predicted that customers buying travel insurance packages don't actually buy insurance packages

- False Negative: It is predicted that the customer doesn't buy a travel insurance package but instead buys an insurance package

Machine Learning models that will be tested include:

- Logical Regression
- K-NN
- Decision Tree Classification
- Random Forest Classification 

## Conclusion :
From the observations made, it can be concluded that the best model for predicting whether a customer buys a travel insurance package or not is Hyperparameter Tuning using Optuna Random Forest Smoothen, because it has the best precision value of 91%.

## Recommendation :
1. The Company can make new offers, travel insurance packages at more suitable prices if needed, to people with incomes below 1.3 million such as people who work in the government sector
2. The Company need to do marketing and provide information about the packages provided
3. The company can get a smaller insurance package for ordinary travel or a coupon for users so that those who don't buy a travel insurance package can be enticed to buy it
