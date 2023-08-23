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

## CODE:
### Loan_data Code:
```
import pandas as pd
import numpy as np
import seaborn as sns
from google.colab import files
uploaded = files.upload()
loan = pd.read_csv("Loan_data.csv")
loan.isnull().sum()
loan=loan.dropna(subset=['Gender'])
loan.isnull().sum()
loan['Credit_History']=loan['Credit_History'].fillna(loan['Credit_History'].mode()[0])
loan.isnull().sum()
loan=loan.dropna(subset='Self_Employed')
loan=loan.dropna(subset='Dependents')
loan=loan.dropna(subset='LoanAmount')
loan.isnull().sum()
loan=loan.dropna(subset='Loan_Amount_Term')
loan.isnull().sum()
loan
loan.to_csv("loan.csv")
loan
files.download("loan.csv")
```

### Data_set Code:
```
df = pd.read_csv("Data_set.csv")
df.isnull().sum()
df
df=df.dropna(subset=['show_name'])
df.isnull().sum()
df.nunique()
df['current_overall_rank'].value_counts()
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['original_network'].mode()[0])
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df=df.dropna(subset=['watchers'])
df=df.dropna(subset=['rating'])
df.isnull().sum()
df.to_csv("data.csv")
files.download("data.csv")
df
```


## OUTPUT:
### Loan_data output:

![image](https://github.com/Georgepaultony/ODD2023-Datascience-Ex01/assets/120088748/6b134247-043f-49cc-9df7-fc342378a06c)

![image](https://github.com/Georgepaultony/ODD2023-Datascience-Ex01/assets/120088748/1db5b0a7-2bcc-448c-8dcc-20009646c7fc)

![image](https://github.com/Georgepaultony/ODD2023-Datascience-Ex01/assets/120088748/9c6ce41c-05e0-4b11-ab0a-8702b45bf686)

![image](https://github.com/Georgepaultony/ODD2023-Datascience-Ex01/assets/120088748/aadf38e8-dbfa-4b96-8102-ad684f8ccd02)

![image](https://github.com/Georgepaultony/ODD2023-Datascience-Ex01/assets/120088748/97812e9f-473b-47b2-ade5-3fc3ab26e1e4)

![image](https://github.com/Georgepaultony/ODD2023-Datascience-Ex01/assets/120088748/6f655ee7-4ffa-48b5-9fde-20014a70e6d2)

### Data_set Output:

![image](https://github.com/Georgepaultony/ODD2023-Datascience-Ex01/assets/120088748/26425368-3572-4d17-8a7c-4f146780239a)

![image](https://github.com/Georgepaultony/ODD2023-Datascience-Ex01/assets/120088748/996e6983-5f2b-4978-99d3-ce0b0d22850d)

![image](https://github.com/Georgepaultony/ODD2023-Datascience-Ex01/assets/120088748/ddaa0184-da41-431d-a9a6-dbe915350dc4)

![image](https://github.com/Georgepaultony/ODD2023-Datascience-Ex01/assets/120088748/24f15ad3-80ef-47ce-be1f-4b248a505c93)

![image](https://github.com/Georgepaultony/ODD2023-Datascience-Ex01/assets/120088748/9f7431f8-7430-40b3-854b-095718f7f6d1)

![image](https://github.com/Georgepaultony/ODD2023-Datascience-Ex01/assets/120088748/4d209ac1-f437-40ac-9f64-055c6de5c090)









