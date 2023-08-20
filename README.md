# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE
import pandas as pd

#Cleaning the file Data_set.csv
df=vmk.read_csv("Data_set.csv")
df.head(10)
df.info()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['original_network'].mode()[0])
df['rating']=df['rating'].fillna(df['rating'].mode()[0])
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mode()[0])
df['watchers']=df['watchers'].fillna(df['watchers'].mode()[0])

#data is cleaned
print('Data_set file after cleaning:')
df.isnull().sum()

#Cleaning the file Loan_data.csv
df1=pd.read_csv('Loan_data.csv')
df1.head(10)
df1.info()
df1.isnull().sum()
df1['Gender']=df1['Gender'].fillna(df1['Gender'].mode()[0])
df1['Dependents']=df1['Dependents'].fillna(df1['Dependents'].mode()[0])
df1['Self_Employed']=df1['Self_Employed'].fillna(df1['Self_Employed'].mode()[0])
df1['LoanAmount']=df1['LoanAmount'].fillna(df1['LoanAmount'].mode()[0])
df1['Loan_Amount_Term']=df1['Loan_Amount_Term'].fillna(df1['Loan_Amount_Term'].mode()[0])
df1['Credit_History']=df1['Credit_History'].fillna(df1['Credit_History'].mode()[0])

#data is cleaned
print('Loan_data file after cleaning:')
df1.isnull().sum()

# OUTPUT

Data_set.csv file.
![d1-img](https://github.com/venkatamohankrishnagithub/ODD2023-Datascience-Ex01/assets/127727792/d62f6393-0ae5-4097-807b-70a32ba7e5a9)

Dupplicate Data.
![d2-img](https://github.com/venkatamohankrishnagithub/ODD2023-Datascience-Ex01/assets/127727792/143a1484-d871-4e1e-937f-5badb9ad3de2)

After Cleaning.
![d3-img](https://github.com/venkatamohankrishnagithub/ODD2023-Datascience-Ex01/assets/127727792/9bccbaaa-5ca3-414f-a5df-59b5e273bc48)

Loan_data.csv file.
![l1-img](https://github.com/venkatamohankrishnagithub/ODD2023-Datascience-Ex01/assets/127727792/44d78198-ec0b-4559-a141-a3ab26e8c1cc)

Dupplicate Data.
![l2-img](https://github.com/venkatamohankrishnagithub/ODD2023-Datascience-Ex01/assets/127727792/eac93770-e549-43ec-8dd6-e70147a29cf9)

After Cleaning.
![l3-img](https://github.com/venkatamohankrishnagithub/ODD2023-Datascience-Ex01/assets/127727792/8dd19746-e8e7-4197-bd5d-048ea876cfb9)

# RESULT
Thus, the given data is read, cleansed and the cleaned data is saved into the file.
