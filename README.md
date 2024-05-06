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

Developed by :JANANI S

REG NO : 212223230086
```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/5557723c-3de9-456a-96a3-3cc33e2e4c66)

```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/86e7c082-188e-4047-9bd1-ef5b0572ddc1)

```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/b817215d-bf03-49bf-b921-11661943f400)

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
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/d07c7acc-659b-40c2-a387-d84c0d35550e)

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
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/bcc557a8-887c-4bf9-94b8-82d53152bbe7)

```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/f7e43938-da49-4a68-98b4-0a45020af30d)

```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
```
```
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/1c9cbc7c-53ca-428b-a9fb-90e59d223474)

```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/4fba335f-8197-476c-96b5-18d84e2424bf)

```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/41578e68-391e-4bfc-b0c6-01f9b6a74165)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/e77a4540-76dd-468c-8a9b-1b88ec675e9f)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/eca443d2-3415-450a-b175-5822e925ede4)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/88f8d0e3-c09d-4cc2-a145-0bdd0429d77a)

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/dd5796d9-cc6b-469a-9d80-3f484df30ba7)

```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/d62590ed-3b93-4b13-bc2b-098f34c0cc3c)

```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/8cbb4c9e-702b-4872-8daf-084dd4c2775f)

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/6b853987-5406-4ea7-940e-9aada2e5ea25)

```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/e0445d75-e430-4e12-990e-333a95f3e065)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/4522bd95-382d-4044-8668-1c952d48222c)

```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/ccf2ca69-8494-4574-ba3f-09eebfda7039)

```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/cb8f6ea8-39ad-4c4e-83e2-c055828269a5)

```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/d9bf25b4-64f7-4bd9-8516-4ff90a359a03)

```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/a02a683c-f7aa-49e9-9341-70190a78cac6)

```
sns.kdeplot(data=mart)
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/9fe37e98-138a-494b-b7f6-34c9d31b917b)

```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/57036deb-2e1f-4b99-a4b4-80c6e15ccea6)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/571e7ce0-e656-417e-b289-97b80022772b)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/c3f407f5-8118-4d40-94aa-68b8fce3b971)

```
hm=sns.heatmap(data=data)
```
![image](https://github.com/SJananisenthilkumar/EXNO-6-DS/assets/144871139/1d7fa5a7-b91b-4696-b183-c2d18f3755aa)

# Result:

Thus, all the data visualization techniques of seaborn has been implemented.
