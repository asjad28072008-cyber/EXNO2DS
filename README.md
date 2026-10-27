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


###**CATEGORICAL DATA ANALYSIS**
```


import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

dt=pd.read_csv("/content/titanic_dataset.csv")

dt

dt.info()

#DISPLAY NO OF ROWS AND COLUMNS

#SET PASSENGER ID AS INDEX COLUMN

dt.describe()
```

<img width="812" height="587" alt="image" src="https://github.com/user-attachments/assets/fd7766d3-ce27-48a8-bc6a-8b7ed471e564" />

###**UNIVARIATE ANALYSIS**
```

# USE COUNTPLOT AND PERFORM UNIVARIATE ANALYSIS FOR THE "SURVIVED" COLUMN IN TITANIC DATASET

# IDENTIFY UNIQUE VALUES IN "PASSENGER CLASS" COLUMN

# RENAMING COLUMN
dt.rename(columns = {'Sex':'Gender'}, inplace = True)
dt

```

<img width="1160" height="395" alt="image" src="https://github.com/user-attachments/assets/e9c6760c-3ef9-4236-a172-517f47a89a54" />

###**BIVARIATE ANALYSIS**

```
# USE CATPLOT METHOD FOR BIVARIATE ANALYSIS

fig, ax1 = plt.subplots(figsize=(8,5))
graph = sns.countplot(#USE THE NECESSARY PARAMETERS HERE)
graph.set_xticklabels(graph.get_xticklabels())
for p in graph.patches:
    height = p.get_height()
    graph.text(p.get_x()+p.get_width()/2, height + 20.8,height ,ha="left")

# USE BOXPLOT METHOD TO ANALYZE AGE AND SURVIVED COLUMN

```





# RESULT
        The Program and The Output has been sucessfully Verified along with the Visualization .
