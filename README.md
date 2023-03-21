# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
import pandas as pd
df=pd.read_csv("/content/Loan_data.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df.head()
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df.head()
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
df.info()
df.isnull().sum()
```

# OUPUT
## DATA:
![image](https://user-images.githubusercontent.com/119477857/226617478-d61f559d-4a6e-4698-877e-599a9738c7e8.png)

![image](https://user-images.githubusercontent.com/119477857/226618502-605f94b2-ca8c-4222-a3fd-c6cf94d22881.png)

## NON NULL BEFORE

![image](https://user-images.githubusercontent.com/119477857/226618945-94262427-8f77-4c96-9c9f-99bc16e8c395.png)
![image](https://user-images.githubusercontent.com/119477857/226619399-acdc6547-fca7-4072-b8de-e288e4d6a41b.png)

## MODE
![image](https://user-images.githubusercontent.com/119477857/226619892-adc1eb86-95c4-4b50-94a4-ffaf8f81cd43.png)
## MEAN

![image](https://user-images.githubusercontent.com/119477857/226620232-a89d98b2-aadb-4f7d-874b-6037950a1884.png)

## MEDIAN

![image](https://user-images.githubusercontent.com/119477857/226620579-79ad29f2-1628-46a7-8f30-921346e719d4.png)

## NON NULL AFTER

![image](https://user-images.githubusercontent.com/119477857/226620843-c859a6bb-9713-48c2-9d96-46b832e2b619.png)

## RESULT

Thus, the given data is read, cleansed and the cleansed data is saved into the file.


