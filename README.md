# Ex-08-Data-Visualization-

## AIM

To Perform Data Visualization on the given dataset and save the data to a file. 

## Explanation

Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## ALGORITHM

### STEP 1
Read the given Data

### STEP 2
Clean the Data Set using Data Cleaning Process

### STEP 3
Apply Feature generation and selection techniques to all the features of the data set

### STEP 4
Apply data visualization techniques to identify the patterns of the data.


## CODE

import pandas as pd

import numpy as np

import matplotlib.pyplot as plt

import seaborn as sbn

df=pd.read_csv("/content/Superstore.csv",encoding='windows-1252')

df.head()

df.info()

df.isnull().sum()

sbn.barplot(x=df['Segment'],y=df['Sales'])

plt.title("Highest Sales of the segment")

sbn.barplot(x=df['City'],y=df['Profit'])

plt.title("Highest Profit of cities")

City=df.loc[:,["City","Profit"]]

df.head(5)

City=City.groupby(by=["City"]).sum().sort_values(by="Profit")

plt.figure(figsize=(10,10))

sbn.barplot(x=City.index,y="Profit",data=City)

plt.xticks(rotation = 90)

plt.xlabel=("City")

plt.ylabel=("Profit")

plt.show()

sbn.barplot(x=df['Ship Mode'],y=df['Profit'])

plt.title("Profitable Ship Mode")

sbn.barplot(x=df['Sales'], y=df['Region'])

plt.title("Sales of Product based on Region")

sbn.lineplot(x=df['Sales'], y=df['Profit'])

plt.title("Relation between Sales and Profit")

sbn.barplot(x=df['Segment'],y=df['Profit'])

plt.title("Sales and Profit based on Segment")

sbn.barplot(x=df['City'],y=df['Profit'])

plt.title("Sales and Profit based on City")

sbn.barplot(x=df['Region'],y=df['Profit'])

plt.title("Sales and Profit based on States")

sbn.barplot(x=df['Ship Mode'],y=df['Profit'])

plt.title("Sales and Profit based on Ship mode")

sbn.barplot(x=df['Sales'],y=df['Profit'])

plt.title("Sales and Profit based on Segment")

## OUPUT

![image](https://github.com/Haripriya-Karunakaran/DS-EXERCISE-8/assets/126390051/3fb14eff-6cce-4fcb-8b12-f9f61e0cda9d)

![image](https://github.com/Haripriya-Karunakaran/DS-EXERCISE-8/assets/126390051/151db8ad-7210-4dea-b783-6f24a4052e82)

![image](https://github.com/Haripriya-Karunakaran/DS-EXERCISE-8/assets/126390051/483313f3-a463-4547-96a7-a2d730771e49)

![image](https://github.com/Haripriya-Karunakaran/DS-EXERCISE-8/assets/126390051/0e03799e-1df0-4107-9bc1-f66e0f41a128)

![image](https://github.com/Haripriya-Karunakaran/DS-EXERCISE-8/assets/126390051/b264f0c0-122b-48a1-a9ba-c6f2bcf8741e)

![image](https://github.com/Haripriya-Karunakaran/DS-EXERCISE-8/assets/126390051/f3a6c764-452b-444c-9c1b-8da66dae759b)

![image](https://github.com/Haripriya-Karunakaran/DS-EXERCISE-8/assets/126390051/92d09ff1-4e35-41f0-b4ea-1858fbdc30d1)

![image](https://github.com/Haripriya-Karunakaran/DS-EXERCISE-8/assets/126390051/efb6820f-67ca-4072-83e4-13226e5f3d8a)

![image](https://github.com/Haripriya-Karunakaran/DS-EXERCISE-8/assets/126390051/50495f9e-7a5f-495f-b534-0b1ee90fc3b8)

![image](https://github.com/Haripriya-Karunakaran/DS-EXERCISE-8/assets/126390051/d73f8744-fd9b-4f63-ae11-456a68fc95fd)

![image](https://github.com/Haripriya-Karunakaran/DS-EXERCISE-8/assets/126390051/656a4984-ae41-4436-ad87-efe8bbef2fb4)

![image](https://github.com/Haripriya-Karunakaran/DS-EXERCISE-8/assets/126390051/4e52a7a8-3e95-4ebd-953e-dee720552234)

![image](https://github.com/Haripriya-Karunakaran/DS-EXERCISE-8/assets/126390051/04ebee52-d9b1-4b47-9c95-42f53f253a61)

![image](https://github.com/Haripriya-Karunakaran/DS-EXERCISE-8/assets/126390051/3b7e909d-985d-4e6d-a78f-18b0a4310fb2)

## RESULT

Thus, the Feature Visualization for the given datasets had been executed
successfully.

