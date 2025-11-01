# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:

```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()

```
<img width="1577" height="426" alt="image" src="https://github.com/user-attachments/assets/f64294af-bd9c-4b6d-96a7-6e04b6a0637a" />


# 1.Line Plot

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')

```

<img width="911" height="727" alt="image" src="https://github.com/user-attachments/assets/333b2e6e-f53f-4a45-9627-18285db594bb" />


# 2.Multi Line Plot

```

x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')

```
<img width="956" height="800" alt="image" src="https://github.com/user-attachments/assets/a60b978a-5f03-4812-b0ae-d17210439610" />


# TO VISUALIZE RELATIONSHIPS
# 1.Bar Chart

```

plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")

```

<img width="1737" height="862" alt="image" src="https://github.com/user-attachments/assets/41b3c8b8-f5c5-4fed-b03b-d7fd23f3b5a3" />


# 2.Scatter Plot :

```

sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()

```

<img width="882" height="680" alt="image" src="https://github.com/user-attachments/assets/9c286d81-befb-4158-b659-cec22be5af83" />


# 3.Bubble Chart :

```

sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()

```

<img width="880" height="673" alt="image" src="https://github.com/user-attachments/assets/eb000e82-bc30-4724-bf5d-9ebda5f8540f" />


## TO CAPTURE DISTRIBUTIONS
# 1.Histogram :

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

```

<img width="842" height="627" alt="image" src="https://github.com/user-attachments/assets/23d2d19a-522e-4524-b812-db400eaaafc5" />


# 2.Box Plot :

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")

```

<img width="1637" height="800" alt="image" src="https://github.com/user-attachments/assets/f26148e6-5391-49ac-b0c1-f606c84774c4" />


# 3.Violin Plot:

```

sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()

```

<img width="943" height="697" alt="image" src="https://github.com/user-attachments/assets/1cec6758-475c-4f61-88dc-84842f0d2ce0" />


# 4.Density Plot :

```

sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()

```

<img width="917" height="826" alt="image" src="https://github.com/user-attachments/assets/536c0f4a-da23-4b93-a309-922671663732" />

# 5.Heatmap :

```

numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()

```

<img width="973" height="778" alt="image" src="https://github.com/user-attachments/assets/f03e971a-b2c1-45e2-a3d5-11a1c26d8e5f" />

# Result:
 
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
