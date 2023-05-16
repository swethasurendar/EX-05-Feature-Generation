# EX-05-Feature-Generation


## AIM
To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature Generation techniques to all the feature of the data set
### STEP 4
Save the data to the file


# CODE
```
data.csv
import pandas as pd   
import seaborn as sbn 
df=pd.read_csv("/content/data.csv") 
df.info() 
df.isnull().sum()
from sklearn.preprocessing import LabelEncoder 
le = LabelEncoder() 
df['Ord_2'] = le.fit_transform(df['Ord_2']) 
sbn.set(style ="darkgrid") 
sbn.countplot(df['Ord_2'])
from sklearn.preprocessing import OneHotEncoder 
enc = OneHotEncoder() 
enc = enc.fit_transform(df[['City']]).toarray() 
encoded_colm = pd.DataFrame(enc) 
df = pd.concat([df, encoded_colm], axis=1) 
df = df.drop(['City'], axis=1) 
df.head(10) 
df = pd.get_dummies(df, prefix=['Ord_2'], columns=['Ord_2']) 
df.head(10) 
df = pd.get_dummies(df, prefix=['Ord_1'], columns=['Ord_1']) 
df.head(10)
 ```
 
# encoding.csv
```
import pandas as pd 
import seaborn as sbn 
data=pd.read_csv("/content/Encoding Data.csv") 
data.info() 
data.isnull().sum() from sklearn.preprocessing import LabelEncoder 
le = LabelEncoder() data['ord_2'] = le.fit_transform(data['ord_2']) 
sbn.set(style ="darkgrid") 
sbn.countplot(data['ord_2']) from sklearn.preprocessing import OneHotEncoder 
en = OneHotEncoder() 
en = en.fit_transform(data[['nom_0']]).toarray() 
encoded_colm = pd.DataFrame(en) 
data= pd.concat([data, encoded_colm], axis=1) 
data= data.drop(['nom_0'], axis=1) 
data.head(10) 
data = pd.get_dummies(df, prefix=['bin_2'], columns=['bin_2']) 
data.head(10)
```

# titanic.csv
```
import pandas as pd 
import seaborn as sbn 
dt=pd.read_csv("/content/titanic_dataset.csv") 
dt.info() 
dt.isnull().sum() 
dt['Age']=dt['Age'] . fillna(dt ['Age'].mean()) 
dt ['Cabin']=dt['Cabin']. fillna(dt['Cabin']. mode() [0]) 
dt ['Embarked']=dt['Embarked'] . fillna(df ['Embarked'].mode( )[0]) 
dt.isnull().sum( ) from sklearn.preprocessing import LabelEncoder 
lc = LabelEncoder() 
df['Sex'] = lc.fit_transform(df['Sex']) 
sbn.set(style ="darkgrid") 
sbn.countplot(df['Sex']) from sklearn.preprocessing import OneHotEncoder 
enc= OneHotEncoder() 
enc= enc.fit_transform(dt[['Name']]).toarray() 
encoded_colm = pd.DataFrame(enc) 
dt= pd.concat([dt, encoded_colm], axis=1) 
dt= dt.drop(['Name'], axis=1) 
dt.head(10) 
dt = pd.get_dummies(dt, prefix=['Ticket'] ,columns=['Ticket']) 
df.head(10) 
dt = pd.get_dummies(dt, prefix=['Embarked'] ,columns=['Embarked']) 
df.head(10)
```
# OUPUT
# Data.csv
![image](https://github.com/swethasurendar/EX-05-Feature-Generation/assets/133625914/46aabfba-2109-4a79-88d0-908eb052b3c2)
![image](https://github.com/swethasurendar/EX-05-Feature-Generation/assets/133625914/ba1b650b-75b0-4ecb-88c9-88ffd17cbd6d)
![image](https://github.com/swethasurendar/EX-05-Feature-Generation/assets/133625914/89c8815f-ed10-4917-8b00-a385efa745df)
![image](https://github.com/swethasurendar/EX-05-Feature-Generation/assets/133625914/a3d50f31-5404-4221-80e7-606116fa9359)
![image](https://github.com/swethasurendar/EX-05-Feature-Generation/assets/133625914/f980af52-3a6b-4c08-8d2e-fed1605e1196)
# Encoding.csv
![image](https://github.com/swethasurendar/EX-05-Feature-Generation/assets/133625914/78ad1970-549f-4d77-97f7-dab6b3d35a5f)
![image](https://github.com/swethasurendar/EX-05-Feature-Generation/assets/133625914/1d79a8de-cce9-4f8e-941a-4f8cb8233891)
![image](https://github.com/swethasurendar/EX-05-Feature-Generation/assets/133625914/5b634abc-a12a-486a-a21a-e8bd2379f7af)
![image](https://github.com/swethasurendar/EX-05-Feature-Generation/assets/133625914/d084cc63-62f1-4f29-9c63-beee56313c66)
# Titanic.csv
![image](https://github.com/swethasurendar/EX-05-Feature-Generation/assets/133625914/5bf5e8ba-a864-4d27-aa20-e187fa3d9297)
![image](https://github.com/swethasurendar/EX-05-Feature-Generation/assets/133625914/b1f5ecc8-ee93-4023-aa67-539bbaa1715e)
![image](https://github.com/swethasurendar/EX-05-Feature-Generation/assets/133625914/07d3a61d-ab09-4217-b061-42220b32a7ae)
![image](https://github.com/swethasurendar/EX-05-Feature-Generation/assets/133625914/b793b80f-f540-42d4-96e9-44e32ce5769f)
![image](https://github.com/swethasurendar/EX-05-Feature-Generation/assets/133625914/52817c5c-7b2a-4f0b-9a1a-9354f4945cab)
![image](https://github.com/swethasurendar/EX-05-Feature-Generation/assets/133625914/5e134e2b-547a-4eb1-9e5c-f56d74ae32ca)
# RESULT:
Thus the program for Feature Generation is executed successfully.

