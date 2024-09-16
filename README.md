# Predicting Bank Customer Churn Using Machine Learning

## Problem Statement
The objective of this project is to predict whether a bank customer will churn (i.e., leave the bank) based on a set of customer attributes. By analyzing variables such as credit score, age, account balance, and customer activity, the goal is to build a machine learning model that can accurately identify customers at risk of churn. This will help the bank take proactive measures to retain valuable customers and reduce churn rates

## Dataset

| **Column Name**     | **Description**                                                                                  |
|---------------------|--------------------------------------------------------------------------------------------------|
| **RowNumber**        | A unique identifier for each row in the dataset, typically used for indexing purposes.            |
| **CustomerId**       | A unique identification number assigned to each customer by the bank.                            |
| **Surname**          | The last name or family name of the customer.                                                    |
| **CreditScore**      | A numerical value representing the customer's creditworthiness based on their financial history.  |
| **Geography**        | The country or region where the customer is located (e.g., France, Germany, Spain).              |
| **Gender**           | The gender of the customer (e.g., Male or Female).                                               |
| **Age**              | The age of the customer in years.                                                                |
| **Tenure**           | The number of years the customer has been with the bank.                                         |
| **Balance**          | The amount of money the customer has in their bank account.                                       |
| **NumOfProducts**    | The number of products the customer has purchased from the bank (e.g., credit cards, loans).     |
| **HasCrCard**        | Indicates if the customer has a credit card (0 = No, 1 = Yes).                                   |
| **IsActiveMember**   | Indicates if the customer is an active member of the bank (0 = Inactive, 1 = Active).            |
| **EstimatedSalary**  | The estimated annual salary of the customer.                                                     |
| **Exited**           | Indicates whether the customer has churned (left the bank) (0 = No, 1 = Yes).                    |

## Approach

### Load the Data
Upload the given data and create a dataframe

### Exploaratory Data Analysis:
* The data is heavyly skewed towards the people who will not churn.
* Histograms of credit card distribuition,age
* Count plots the customers per Gender,Has creditcard,Location 

### Feature Engineering
* Converting the categorical values to numerical (gender using labelencoder,location using onehot encoder)
* Drop the unnecessary columns (RowNumber,CustomerId,Surname)
* Scale the data using standard scaler
* Save these encoders and scalers for further use

### Create ANN Model
* Create a fully connected sequential Dense Layered model
* Create logs and callbacks
* Use Tensorboard to monitor the model
### Metrics
* An Accuracy score of 87% is achieved
### Input Data and predictions
* input_data={'CreditScore':600,
            'Geography':'France',
            'Gender':'Male',
            'Age':40,
            'Tenure':3,
            'Balance':60000,
            'NumOfProducts':2,
            'HasCrCard':1,
            'IsActiveMember':1,
            'EstimatedSalary':50000 }
  * Create a function to convert the abov einput data for the model requirements
  
## Conclusions


