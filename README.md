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

df.head(5)

df.tail(5)

df.describe()

df.info()

df.isnull().sum()

df=df[~df.duplicated()]
print(df)

df['Gender'].fillna(value=df['Gender'].mode())

df['LoanAmount'].fillna(value=df['LoanAmount'].median())
```

# OUPUT

![image](https://user-images.githubusercontent.com/118679646/226252553-3b9b6de6-b503-4f28-b238-1d53bd56dcd5.png)
![image](https://user-images.githubusercontent.com/118679646/226252649-710484ee-0a15-4e71-ad80-9128965aeecb.png)
![image](https://user-images.githubusercontent.com/118679646/226252752-d5bd74cc-6037-4a85-8b9e-215ef5e715e4.png)
![image](https://user-images.githubusercontent.com/118679646/226252887-78bba412-fe6a-4d4e-9f7e-71d69f63e89b.png)
![image](https://user-images.githubusercontent.com/118679646/226252964-1b20d45c-9296-4fc7-89a3-162c356a2bae.png)
