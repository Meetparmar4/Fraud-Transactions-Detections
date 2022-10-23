# Fraud-Transactions-Detections

## About the data 

It consisted of 5 different transaction types made by customers.  [Link to the dataset]: https://www.kaggle.com/datasets/meetparmarps5/fraud-transaction-detection

### The columns are explained below:

-  step - maps a unit of time in the real world. In this case 1 step is 1 hour of time. Total steps 744 (30 days simulation).
-  type - CASH-IN, CASH-OUT, DEBIT, PAYMENT and TRANSFER.
-  amount - amount of the transaction in local currency.
-  nameOrig - customer who started the transaction
-  oldbalanceOrg - initial balance before the transaction
-  newbalanceOrig - new balance after the transaction
-  nameDest - customer who is the recipient of the transaction
-  oldbalanceDest - initial balance recipient before the transaction. Note that there is not information for customers that start with M (Merchants).
-  newbalanceDest - new balance recipient after the transaction. Note that there is not information for customers that start with M (Merchants).
-  isFraud - This is the transactions made by the fraudulent agents inside the simulation. In this specific dataset the fraudulent behavior of the agents aims to profit by taking control or customers accounts and try to empty the funds by transferring to another account and then cashing out of the system.
-  isFlaggedFraud - The business model aims to control massive transfers from one account to another and flags illegal attempts. An illegal attempt in this dataset is an attempt to transfer more than 200.000 in a single transaction.

## Exploratory Data Analysis

-  There were 5 different  types of transactions for which we found which were used the most and which had fraudulent cases by using simple data summarisations and visualisations.
-  Then checked what factors were responsible for the isflaggedfraud column to be set 1.
-  Identified which features were responsible for marking a transaction fraud by EDA. 

## Data Cleaning

- Dropped useless attributes in the transaction types payment, debit, cash in transactions and isflagged fraud column to decrease the size of data and runtime for code.
- Made the data suitable for training ML models by reorganising it. Also checked for collinearity amongst the independent features.

## Model Training

Then trained different classification models to see which gives the best results of predictions by comparing confusion matrices, F1 score, precision and recall.


