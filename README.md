# Fraud_Capstone
Analyze and identify fraudent transactions 

# Analysis
Analyzed multiple datasets and acquired dataset from Kaggle https://www.kaggle.com/datasets/chitwanmanchanda/fraudulent-transactions-data. The goal is to identify fraudulent transactions costing banks billions of dollars annually. Furthermore, impacted parties suffering financial loss at an institution often lose faith in institutions failing to proactively add safeguards to protect their assets.

# Features
### Problem 3: Understanding the Features

step - maps a unit of time in the real world. In this case 1 step is 1 hour of time. Total steps 744 (30 days simulation).
type - CASH-IN, CASH-OUT, DEBIT, PAYMENT and TRANSFER.'
amount - amount of the transaction in local currency.'
nameOrig - customer who started the transaction'
oldbalanceOrg - initial balance before the transaction
newbalanceOrig - new balance after the transaction'
nameDest - customer who is the recipient of the transaction'
oldbalanceDest - initial balance recipient before the transaction. Note that there is not information for customers that start with M (Merchants).'
newbalanceDest - new balance recipient after the transaction. Note that there is not information for customers that start with M (Merchants).'
isFraud - This is the transactions made by the fraudulent agents inside the simulation. In this specific dataset the fraudulent behavior of the agents aims to profit by taking control or customers accounts and try to empty the funds by transferring to another account and then cashing out of the system.'
isFlaggedFraud - The business model aims to control massive transfers from one account to another and flags illegal attempts. An illegal attempt in this dataset is an attempt to transfer more than 200.000 in a single transaction.'

# Account types

<img width="501" height="399" alt="image" src="https://github.com/user-attachments/assets/7c902daa-2f2b-4864-9abd-73cd6c32221c" />

type
CASH_IN     1399284
CASH_OUT    2237500
DEBIT         41432
PAYMENT     2151495
TRANSFER     532909

After data cleaning/dropping na records, the numbers match pre-cleaning.

# Fraudulent transactions
The data contains 8213 fraudulent transactions, only 16 where inferred.

# Baseline model
A baseline model shows a high accuracy. This is due to the fact that fraudulent transactions are a small fraction of the total number of transactions.
0.9987091795518198

# Research
Several models (tree, nearest neighbor, regression) will be required for training to predict fraudulent transactions at a later stage.

Three different models were used against the same training/test data and accuracy/precision were assessed. The results of each are shown below:

Decision Tree:
Precision: 0.86
Accuracy: 1.00

KNN:

Regression:


Results:
Logistic regression classification outscored both decision tree and KNN classifications. There was room to improve all three models by transforming additional features or by experimenting with various tree depths, etc. When it comes to performance, decision tree completed fastest while KNN and LR were significantly slower in processing the data which indicate higher compute and associated costs.
