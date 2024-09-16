# Predicting Bank Customer Churn Using Machine Learning

## 1. Problem Statement
The objective of this project is to predict whether a bank customer will churn (i.e., leave the bank) based on a set of customer attributes. By analyzing variables such as credit score, age, account balance, and customer activity, the goal is to build a machine learning model that can accurately identify customers at risk of churn. This will help the bank take proactive measures to retain valuable customers and reduce churn rates

## 2. Dataset

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

## 3. Approach to the problem

### Load the Data
* Upload the given data and create a dataframe for further statistical analysis

### Exploaratory Data Analysis:
* A detailed exploaration of the data is done to understand the key features
* The data is heavyly skewed towards the people who will not churn.
* **`Visualizations:`**
> * Histograms of features like CreditScore, Age, and Balance to show their distribution.
> * Count plots showing customer breakdowns by features such as Gender, HasCrCard, and Geography.

### Feature Engineering
* **`Encoding Categorical Variables:`**
> *  Gender was encoded using LabelEncoder.
> *  Geography was transformed using OneHotEncoder
* **`Drop Unnecessary Columns:`**
> *  Drop the unwanted columns (`RowNumber`,`CustomerId`,`Surname`)
* **`Split the data into Train and Test sets`**
> * Using tarin test split from sklearn,we split the data into tarin and test sets with a `test size of 20%`
* **`Scaling the features`**
> *  Scale the data using standard scaler
* Save these encoders and scalers for further use

### Create ANN Model
* **`Model Architecture:`**
> * A fully connected sequential neural network model was created using Dense layers.
> * Optimizer =Adam,loss=Binarycrossentrophy
> * Activation functions (relu and sigmoid) were used
* **`Callbacks and logs:`**
> * ensorBoard was used to monitor the training process, and callbacks were added for early stopping and performance tracking.

### Evaluation Metrics
* The model achieved an accuracy score of 87% accuracy on the test set, which indicates reasonable performance for predicting customer churn.

  
## 4. Conclusions
This project demonstrates the use of  artificial neural network (ANN)  to predict customer churn in a banking environment. The model's ability to predict churn with a high degree of accuracy(87%) allows banks to focus on retention strategies for at-risk customers. Further improvements could involve refining the model architecture, experimenting with more complex models, and incorporating additional customer features for enhanced accuracy.


