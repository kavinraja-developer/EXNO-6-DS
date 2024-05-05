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
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/18a0f3c8-10a6-42b4-9eb3-45770f741ac3)

```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/0124fef5-dcba-4c31-9831-db85384d9c5a)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/1bbe2d28-735c-4114-aff7-9030d334c830)
```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/4d6c2a15-2352-4ba4-bd6b-97a54cd93ce7)
```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/86b30955-7bb2-44af-92d1-39e8be4b56ea)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/27a32e9f-e734-4f47-adf1-bafddba998c3)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
```
```
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/31f5b45b-5a80-4259-a259-a4cecee25ee5)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/359daca3-3920-4c78-b593-7d660c09cc36)
```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/b749f1ee-b0a6-4a67-a340-f9cae8a8290a)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/03dbd087-2a3e-4bfa-8847-bc2e9bbe7cc3)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/090114ac-6d91-4117-80ca-2bb2fe72af26)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/b7984ccc-60c8-4cf2-ba31-0dafe6119b91)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/5e149370-320f-4c4b-b6e9-93839011d166)
```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/39b3d5fa-e8af-45f5-afb2-2875c766a5e6)
```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/e8b91ede-1cc0-4087-beb6-c3c56d8137ee)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/c7d0ff3a-e9a0-4369-a9c9-9229d84776c3)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/dc5777c4-83cf-47d2-ba0c-b6bb81547441)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/8dec8878-d0bb-46ca-bc17-095aba86cffd)
```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/32c63c42-35dc-47df-b851-c13e54c166aa)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/bcbe61b9-5739-4853-a186-302272133266)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/727482e0-5b45-47e4-8542-93ebc9cfb5b7)
```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/9bb955c9-ba97-48ab-b158-35a44931ccf6)
```
sns.kdeplot(data=mart)
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/8cc57d95-8df2-4483-8c98-2edbcfb68b0c)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/f56e128b-5393-46e8-acb6-33bfd6fde4a9)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/4f66d13f-770e-4b17-b29d-74f42cb4395e)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/5eba9f52-3c11-4640-b78f-451463d24415)
```
hm=sns.heatmap(data=data)
```
![image](https://github.com/Sriram8452/EXNO-6-DS/assets/118708032/4bbbf59a-e638-4c7b-bf5c-5298f9bada3b)

# Result:

Thus, all the data visualization techniques of seaborn has been implemented.
