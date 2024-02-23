# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
```
import pandas as pd
df=pd.read_csv('/content/SAMPLEIDS.csv')
print(df)
df.head(10)
df.info()
data.isnull().sum()
data = pd.get_dummies(data)
columns_with_null = data.columns[data.isnull().any()]

### VISUALIZATION:
import seaborn as sns
plt.figure(figsize=(10,10))
sns.barplot(columns_with_null)
plt.title("NULL VALUES")
plt.show()

### NULL IMPUTATION
for column in columns_with_null:
    median = data[column].median()  
    data[column].fillna(median, inplace=True)
data.isnull().sum().sum()


```
![image](https://github.com/Vanitha-SM/exno1-datascience/assets/119557985/c9151899-86da-4aaf-8c49-2f999ed9d71d)

![image](https://github.com/Vanitha-SM/exno1-datascience/assets/119557985/f0d351fb-4ba1-4147-89c6-2ace56643ad9)

![image](https://github.com/Vanitha-SM/exno1-datascience/assets/119557985/4dc389a1-0966-4e26-bec8-3f2c8521cbf0)


![image](https://github.com/Vanitha-SM/exno1-datascience/assets/119557985/a33bd6bf-79b1-42e0-bf18-613f96c8b592)

![image](https://github.com/Vanitha-SM/exno1-datascience/assets/119557985/d88f4a69-2ce3-4604-abfb-f4163593f97b)

![image](https://github.com/Vanitha-SM/exno1-datascience/assets/119557985/46a386aa-5991-4236-bd7c-3235c42a7716)


# Result
Thus the given data is read,cleansed and the cleaned data is saved into the file.

