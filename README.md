# EXNO2DS
# REGISTER NO : 212224040036
# NAME : ASIN RENIX V
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
import numpy as np
import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")
df
```
<img width="1452" height="481" alt="image" src="https://github.com/user-attachments/assets/70eb89fc-bbb5-4b32-b909-f7da40a1e631" />

df.info

<img width="498" height="399" alt="image" src="https://github.com/user-attachments/assets/c38ff6a3-c057-4806-8dd2-04827521e08a" />

df.describe

<img width="890" height="336" alt="image" src="https://github.com/user-attachments/assets/c5dc9131-de11-40d6-b41d-69f7b9d60b3b" />

df.dtypes

<img width="400" height="519" alt="image" src="https://github.com/user-attachments/assets/243bff89-d632-47f9-99be-bdb7acf48780" />

df.shape

<img width="202" height="38" alt="image" src="https://github.com/user-attachments/assets/e23d5b6f-be4c-48e6-b57a-dc124a59d052" />

df.value_counts()

<img width="1467" height="484" alt="image" src="https://github.com/user-attachments/assets/d77648e4-ed4e-4cd8-a0c7-d9d3a929f881" />

df['Age'].value_counts()

<img width="363" height="550" alt="image" src="https://github.com/user-attachments/assets/089c7470-eea0-4338-82d5-5ee511b050b1" />

```
df.set_index('PassengerId',inplace=True)
df
```

<img width="1404" height="514" alt="image" src="https://github.com/user-attachments/assets/bda0ac01-df6b-4dfd-be3a-9aac0cf6c920" />

df.nunique()

<img width="381" height="484" alt="image" src="https://github.com/user-attachments/assets/2f448681-09b9-4d9f-9c5f-d42d4d53b7ad" />

sns.countplot(data=df,x='Age')

<img width="821" height="521" alt="image" src="https://github.com/user-attachments/assets/e2aceacf-cc74-463c-9b33-7649a0f81fcd" />

```
df.rename(columns={'Sex':'Gender'},inplace=True)
df
```

<img width="1489" height="501" alt="image" src="https://github.com/user-attachments/assets/87e1d49f-84d6-49b4-bbe4-888d8e0cbc28" />

sns.catplot(x="Gender",col="Survived",kind="count",data=df,height=5,aspect=.7)

<img width="1087" height="574" alt="image" src="https://github.com/user-attachments/assets/d7c5772a-8b1f-4a65-8b44-775328cd1d79" />

df.boxplot(column='Age',by='Survived')

<img width="829" height="551" alt="image" src="https://github.com/user-attachments/assets/7974c42f-a6fa-4031-9ffd-bfb46d6b010f" />

sns.scatterplot(x=df["Age"],y=df["Fare"])

<img width="783" height="517" alt="image" src="https://github.com/user-attachments/assets/bd0e9b0f-470e-41c6-960e-5b804268b4b2" />

plt=sns.boxplot(x='Pclass',y='Age',hue='Gender',data=df)

<img width="758" height="497" alt="image" src="https://github.com/user-attachments/assets/2fc42ce0-cdb4-4d64-b52c-65488e518ab6" />

sns.catplot(x='Pclass',y="Age",hue="Gender",col="Survived",kind="box",data=df)

<img width="1352" height="584" alt="image" src="https://github.com/user-attachments/assets/58d964ac-f1cb-4a70-bcf9-942df5bce443" />

```
corr=df.corr(numeric_only=True)
sns.heatmap(corr,annot=True)
```

<img width="724" height="504" alt="image" src="https://github.com/user-attachments/assets/4a2742e1-7289-4e03-a52c-681b51a71e8c" />


# RESULT
Thus the above code executed successfully.
