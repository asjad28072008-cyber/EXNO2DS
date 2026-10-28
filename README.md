### Name: MUHAMMAD ASJAD E
### Register no: 212225240091
### Date: 28.10.2026

# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT


```
import pandas as pd
df = pd.read_csv("/content/titanic_dataset.csv")
df
```

<img width="882" height="352" alt="image" src="https://github.com/user-attachments/assets/2d377d82-d44d-4618-9193-e2529abac103" />



```
df.info()
```

<img width="335" height="287" alt="image" src="https://github.com/user-attachments/assets/a796c4c5-a59e-4daf-b4b7-3f7b855fc0db" />


```
df.describe()
```

<img width="598" height="252" alt="image" src="https://github.com/user-attachments/assets/97ed56c5-9ca2-4c34-bebc-118e56433a0a" />


```
df.shape
```

<img width="122" height="67" alt="image" src="https://github.com/user-attachments/assets/bc7c354d-b5b4-4780-a290-bc190f05036e" />


```
df.dtypes
```

<img width="177" height="347" alt="image" src="https://github.com/user-attachments/assets/9aa23e98-5809-4c6e-8140-a14c1a21119e" />


```
df.value_counts()
```

<img width="968" height="377" alt="image" src="https://github.com/user-attachments/assets/7fac03ca-9d1f-4fe8-baa4-23f9ca448690" />


```
df.nunique()
```


<img width="212" height="368" alt="image" src="https://github.com/user-attachments/assets/76b2fa54-68f1-4f57-8138-8ebe153ca2f9" />


```
df["Survived"].value_counts()
```

<img width="230" height="161" alt="image" src="https://github.com/user-attachments/assets/a6d2cc08-dde4-4484-b331-6339aef125f0" />



```
import seaborn as sns
sns.boxplot(data=df, x ='Fare')
```

<img width="476" height="393" alt="image" src="https://github.com/user-attachments/assets/fcd07070-2d2f-439e-b360-ff3c7190b98b" />



```
sns.countplot(data=df, x = 'Survived')
```

<img width="601" height="357" alt="image" src="https://github.com/user-attachments/assets/0b471634-a861-48f0-b84c-c61cad70e1e2" />



```
sns.histplot(data=df,x="Age")
```


<img width="477" height="370" alt="image" src="https://github.com/user-attachments/assets/c48ff974-9843-4a5c-9df0-faad9b7ff1f6" />


```
df.rename(columns={'Sex':'Gender'},inplace=True)
print(df)
```

<img width="486" height="547" alt="image" src="https://github.com/user-attachments/assets/96e12de3-be6d-4a30-928a-045945070e7e" />



```
sns.barplot(x=df["Survived"] , y=df["Age"], data=df)
```


<img width="508" height="372" alt="image" src="https://github.com/user-attachments/assets/953e2cc0-0889-424c-b9b7-c4c85e97be60" />


```
sns.scatterplot(x=df["Survived"], y=df["Age"],data=df)
```

<img width="500" height="357" alt="image" src="https://github.com/user-attachments/assets/e36599b5-32e8-499e-97f0-fb40a4587b4a" />



```
sns.catplot(x='Gender', col='Survived', kind='count',data=df)
```


<img width="847" height="403" alt="image" src="https://github.com/user-attachments/assets/5f3e37e5-72f2-4bde-a68f-e916dd8a6fb8" />


```
df.boxplot(column="Age" ,by='Survived')
```

<img width="467" height="401" alt="image" src="https://github.com/user-attachments/assets/67a7a3d1-c4a3-4c4b-a47f-10eac0f5ba3e" />



```
sns.boxplot(x='Pclass', y='Age', hue='Gender', data=df)      
```


<img width="495" height="380" alt="image" src="https://github.com/user-attachments/assets/ec6ae7bc-17ab-4688-a481-503c07a11756" />




```
sns.catplot(data=df,col="Survived",x="Gender",hue="Pclass",kind="count")
```

<img width="862" height="410" alt="image" src="https://github.com/user-attachments/assets/10a32945-0524-4b36-8685-7d5c2196f4b7" />



```
sns.heatmap(df.corr(numeric_only=True),annot=True)
```



<img width="517" height="412" alt="image" src="https://github.com/user-attachments/assets/0b95f951-4f67-468c-a172-09720ce1afa5" />








# RESULT
        The Program and The Output has been sucessfully Verified along with the Visualization .
        Successfully performed Exploratory Data Analysis (EDA) by handling missing values, detecting and removing outliers, analyzing categorical and numerical data, and visualizing relationships using countplot, displot, crosstab, and heatmap.
