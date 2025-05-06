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
![image](https://github.com/user-attachments/assets/6d662e15-a7c5-4685-9b0b-622a304c099b)
```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/6ae723b7-3430-4398-9f73-b1b7245edcdb)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")

```
![image](https://github.com/user-attachments/assets/356ffdac-5578-4b06-a43c-c8c60cca9749)
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
![image](https://github.com/user-attachments/assets/283698bc-4c04-4194-85dc-bd49e92902b0)
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
![image](https://github.com/user-attachments/assets/628c9247-940a-4200-bf0a-6d593a908f10)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/user-attachments/assets/c90d534d-2a17-4a98-9e7d-7de21644efc1)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/user-attachments/assets/12901df9-70b7-4411-8dbd-06f3e8a590f3)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/5d4b9f0a-879d-476b-ae8c-31a64e9cd043)
```
tit=pd.read_csv("drive/MyDrive/DS2024/titanic_dataset.csv")
tit
```
![image](https://github.com/user-attachments/assets/e491bddb-1441-4192-a917-94a869a282ed)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/user-attachments/assets/7807e911-5566-4aff-9016-1435d1795c61)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/user-attachments/assets/9613d20b-1f3e-45f8-81ba-0087baf44fbf)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/83b7a291-7eab-4c4b-9a45-addd5ec57e04)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/user-attachments/assets/4fdf66b1-ce9b-4378-a5c2-06f7c07f0e2f)
```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/user-attachments/assets/44f3bb5a-8bfd-4d20-9c3e-5e54e66cadc4)
```
df=pd.read_csv("drive/MyDrive/DS2024/titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/user-attachments/assets/63b15104-7ad4-4fa1-ae0e-8fa201448376)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/user-attachments/assets/942d9246-9234-4e0e-8ba8-b1370b03a44c)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/user-attachments/assets/bf9e2d74-e82f-4229-9684-e9c280fc1d62)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/8dbba574-f1b1-4dfc-acb1-6e0cfca8d738)
```
mart=pd.read_csv("drive/MyDrive/DS2024/titanic_dataset.csv")
mart
```
![image](https://github.com/user-attachments/assets/a8cbc9ce-24aa-45db-a6d4-814618a495a0)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]
mart.head(10)
```
![image](https://github.com/user-attachments/assets/38a28c9e-206a-486e-b09f-1abb4aa88680)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/user-attachments/assets/b61dad96-dfc4-4695-b5f2-f5d706ba03b3)
```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/user-attachments/assets/bdad8a74-e74a-4d46-9e78-af5977ba03ab)
```
sns.kdeplot(data=mart)
```
![image](https://github.com/user-attachments/assets/19471985-92db-4caa-8a3a-e1aada2287c8)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/user-attachments/assets/7ef05649-b3ce-44a4-b4a2-b9d6cec8d9a7)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/user-attachments/assets/5f3ac0db-8614-415a-9315-50c05431a71a)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/user-attachments/assets/c95ce86b-2b8f-4245-9c21-4c21921fed4c)
```
hm=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/ac878619-2c07-484f-b3d2-e0d0fb661a2f)


# Result:
Thus the program to Perform Data Visualization using seaborn python library for the given datas is done successfully.


