# EXNO2DS
# Name: Divya R V
# Reg No: 212223100005


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
# import pandas as pd
# import numpy as np
# import matplotlib.pyplot as plt
# import seaborn as sns
# dt=pd.read_csv('/content/titanic_dataset.csv')
# dt

![Screenshot 2024-09-03 142217](https://github.com/user-attachments/assets/c4b675b8-c74d-454f-a0a7-601c24334aa4)

# dt.info()
![Screenshot 2024-09-03 142231](https://github.com/user-attachments/assets/60064871-5a7d-4d8b-a0bf-1c23728a3b59)

# dt.shape

(891, 12)

# dt.set_index("PassengerId",inplace=True)
# dt.describe()

![Screenshot 2024-09-03 142255](https://github.com/user-attachments/assets/c0f0e218-ee7e-47b4-b954-8d0eec32b2aa)

# dt.nunique()

![Screenshot 2024-09-03 142307](https://github.com/user-attachments/assets/1083ace6-e8ee-4a67-8dd6-aade0c67c74e)

# dt["Survived"].value_counts()

![Screenshot 2024-09-03 142325](https://github.com/user-attachments/assets/c69eda1d-ebde-48c0-95ba-3c17ae273d90)

# per=(dt["Survived"].value_counts()/dt.shape[0]*100).round(2)
# per
![Screenshot 2024-09-03 142337](https://github.com/user-attachments/assets/667cfa39-445f-44a3-931a-ef0ab3601dbe)

# sns.countplot(data=dt,x="Survived")

![Screenshot 2024-09-03 142353](https://github.com/user-attachments/assets/d6f49bc9-e1df-449e-9b57-33f08104fea3)

# dt
![Screenshot 2024-09-03 142416](https://github.com/user-attachments/assets/37b28229-f7a9-4b45-9e61-8f43cd0842fc)

# dt.Pclass.unique()

array([3, 1, 2])

# dt.rename(columns = {'Sex':'Gender'},inplace=True)
# dt
![Screenshot 2024-09-03 142436](https://github.com/user-attachments/assets/2153b50d-9363-47a7-99ca-89ee614b52a0)

# sns.catplot(x="Gender",col="Survived",kind="count",data=dt,height=5,aspect=.7)

![Screenshot 2024-09-03 142448](https://github.com/user-attachments/assets/82b70b5f-d0ab-4488-9cf5-efdfd4543996)

# sns.catplot(x='Survived',hue="Gender",data=dt,kind="count")
![Screenshot 2024-09-03 142502](https://github.com/user-attachments/assets/9253aec9-9196-4340-9d8f-b0830aa0f327)

# dt.boxplot(column='Age',by="Survived")
![Screenshot 2024-09-03 142515](https://github.com/user-attachments/assets/a2c2d193-7f99-41b0-be04-628041096345)

# sns.scatterplot(x=dt["Age"],y=dt["Fare"])
![Screenshot 2024-09-03 142528](https://github.com/user-attachments/assets/b6ac9f22-8442-4032-9ea4-e0c9d1f28a3c)

# sns.jointplot(x="Age",y="Fare",data=dt)
![Screenshot 2024-09-03 142540](https://github.com/user-attachments/assets/b2d8b65c-972e-4004-abd2-0ab446120648)

# fig, ax1=plt.subplots(figsize=(8,5))
# pt= sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Gender',data=dt)

![Screenshot 2024-09-03 142554](https://github.com/user-attachments/assets/ecf00b99-b554-4a6d-bf12-519fe9c6d729)

# sns.catplot(data=dt,col="Survived",x="Gender",hue="Pclass",kind="count")

![Screenshot 2024-09-03 142609](https://github.com/user-attachments/assets/6712c701-96c6-4350-9c1a-11e0db6837a1)

# sns.pairplot(dt)

![Screenshot 2024-09-03 142643](https://github.com/user-attachments/assets/25fa6e0d-e0e4-407a-9275-5f899cb97da4)

![Screenshot 2024-09-03 142724](https://github.com/user-attachments/assets/98099b92-3667-4b09-a173-44cb0beb0633)
        

# RESULT
      Thus the exploratory data analysis on the given data set is performed.
