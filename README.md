# Syriatel-churn-classification

## Business and Data Understanding
Most telecom companies suffer from voluntary churn. Churn rate has strong impact on the life time value of the customer because it affects the length of service and the future revenue of the company. 
When a customer leaves, the company loses money spent on acquiring the customer and also future revenue that could have been generated from that customer. It also could destroy the brand image of the company

## Stakeholder audience 
My client, Syriatel would like to find ways to decrease churn.
Using the data provided, I would like to determine the features that affect churn,make appropriate recommendations and also create a model to identify customer churn behaviour from observations. 

## Data & Methodology
Data was downloaded from [here](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset). The original data contains 3333 rows and 21 columns
The target column is churn which is subdivided into:
    ![Screenshot (31)](https://user-images.githubusercontent.com/82956881/181801249-fa2a129a-4e9d-48cf-b5b1-a5f2bcab96a9.png)

As can be seen, there is an imbalance in the dataset. 

## Modeling and Evaluation
My main aim was to find a good  accuracy and good precision since the goal was to reduce the misclassification of those who churn as not churning. The table below shows the different models used and the results of the two on the test data.


Model	|Accuracy |Precision|Recall
--- | --- | --- | ---
Baseline	|0.85|	0.54	|0.17
--- | --- | --- | ---
Logistic Regression|	0.78|	0.395|	0.78
--- | --- | --- | ---
Decision Trees	|0.91	|0.7	|0.75
--- | --- | --- | ---
Random Forest|	0.93|	0.77|	0.76
--- | --- | --- | ---
XGBClassifier	|0.93	|0.9	|0.81



The choice was the final model: XGBClassifier with hyperparameters = {'learning_rate': 0.4, 'max_depth': 5, 'n_estimators': 180}
### The confuson matrix:
![matrix ](https://user-images.githubusercontent.com/82956881/181811561-876a7f66-82d4-4846-9a22-e52532fbaff1.png)


## Conclusion
 Using the model, the features of the customer can predict whether  a customer will churn or not. Then the customers can be put into different groups and different marketing strategies can be used on them, one for retaining the customers who wont churn and another for holding onto the one who thinks of churning. Instead of wasting money on one marketing strategy for all
 
 More analysis and insights can be found in the notebook and powerpoint presentation in this repository

 
 
