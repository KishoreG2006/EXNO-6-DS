# Name:KISHORE G
# Register NO: 212223040099
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
df=sns.load_dataset("tips")
df
```
<img width="573" height="315" alt="image" src="https://github.com/user-attachments/assets/84962889-7349-4191-a50a-62ed144afc68" />

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="solid",legend="auto")
```

<img width="568" height="375" alt="image" src="https://github.com/user-attachments/assets/46650412-6d26-47af-8552-b9abecf9e56b" />

```
x = [1, 2, 3, 4, 5]
y1 = [3, 5, 2, 6, 1]
y2 = [1, 6, 4, 3, 8]
y3 = [5, 2, 7, 1, 4]

sns.lineplot(x=x, y=y1, label='Line 1')
sns.lineplot(x=x, y=y2, label='Line 2')
sns.lineplot(x=x, y=y3, label='Line 3')

plt.title("Multi-Line Plot")
plt.xlabel("X Label")
plt.ylabel("Y Label")
plt.legend()
plt.show()
```

<img width="553" height="366" alt="image" src="https://github.com/user-attachments/assets/cd798bd6-44c2-4c6e-931e-f83762cfc27a" />

```
tips=sns.load_dataset("tips")
avg_total_bill=tips.groupby("day")["total_bill"].mean()
avg_tip=tips.groupby("day")["tip"].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label="Total Bill")
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label="tip")
plt.xlabel("Day of the week")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Day")
plt.legend()
plt.show()
```

<img width="630" height="449" alt="image" src="https://github.com/user-attachments/assets/ea8398a3-25fc-4d76-be9d-cbb7022befbd" />

```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label="Total Bill",width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label="Tip",width=0.4)
plt.xlabel("Time of the day")
plt.ylabel("Amount")
plt.title("Average Total bill and Tip by Time of the day")
plt.legend()
```

<img width="589" height="403" alt="image" src="https://github.com/user-attachments/assets/0b00f1d4-a64b-48bd-9b18-48611573dc91" />

```
import seaborn as sns
df=sns.load_dataset("tips")
sns.barplot(x="day",y="total_bill",hue="sex",data=df,palette='Set3')
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Total Bill by Day and Gender")
```

<img width="637" height="395" alt="image" src="https://github.com/user-attachments/assets/88d97d4d-7b2b-4516-b7d4-1b0e3760e00c" />

```
import seaborn as sns
df=sns.load_dataset("tips")
sns.scatterplot(x="total_bill",y="tip",hue="sex",data=df,palette="Set1")
plt.xlabel("Total Bill")
plt.ylabel("Tip")
plt.title("Scatter Plot of Total Bill vs Tip Amount")
```


<img width="623" height="397" alt="image" src="https://github.com/user-attachments/assets/11d20bd2-7497-4ac1-a9fe-8edee072ddda" />

```
import seaborn as sns
import matplotlib.pyplot as plt

sns.histplot(data=df, x="total_bill", hue="smoker", kde=True, palette="Set1")
plt.xlabel("Total Bill")
plt.ylabel("Frequency")
plt.title("Distribution of Total Bill by Smoker Status")
plt.show()
```

<img width="614" height="398" alt="image" src="https://github.com/user-attachments/assets/6b7ce1f1-05c7-4e35-b664-10590160131b" />

```

df=sns.load_dataset('tips')
sns.boxplot(x='day', y='total_bill', hue='sex', data=df, palette='Set2')


```

<img width="630" height="376" alt="image" src="https://github.com/user-attachments/assets/ccaacd9d-02eb-4941-ae62-2e887011c2cf" />

```
sns.boxplot(
    x='day',
    y='total_bill',
    hue='smoker',
    data=df,
    linewidth=2,
    width=0.6,
    fliersize=7
)

```

<img width="715" height="397" alt="image" src="https://github.com/user-attachments/assets/fbd4bf50-00a6-46f2-84c0-a8a9380b73dd" />

```
sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,palette='Set1',inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```

<img width="690" height="403" alt="image" src="https://github.com/user-attachments/assets/5ab632fb-62e4-4942-8042-8e9b72eaed79" />

```

sns.set(style="whitegrid")
tip=sns.load_dataset('tips')
sns.violinplot(x='day',y='tip',data=tip,palette="Set2")
```


<img width="613" height="389" alt="image" src="https://github.com/user-attachments/assets/1eac3842-2b56-41d8-af44-531f144795a2" />


```
sns.set(style="whitegrid")
tip=sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"],palette="Set1")
```

<img width="584" height="390" alt="image" src="https://github.com/user-attachments/assets/0580a5aa-5fa1-4331-a5f4-a4a118c0c5bb" />

```
sns.set(style="whitegrid")
tips = sns.load_dataset("tips")

sns.violinplot(x="tip", y="day", data=tips, palette="rainbow")
plt.show()
```


<img width="643" height="376" alt="image" src="https://github.com/user-attachments/assets/a38c1a5e-296c-43c0-b8cc-7154c35265da" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple="layer",linewidth=3,palette='Set2',alpha=0.8)
```

<img width="705" height="387" alt="image" src="https://github.com/user-attachments/assets/9c28bd7c-a765-4830-b23e-35ea01a0b9a0" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set3',alpha=0.8)

```


<img width="669" height="400" alt="image" src="https://github.com/user-attachments/assets/42a1deed-d03f-45db-a4ec-781d4a35ff62" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set1',alpha=0.8)
```


<img width="624" height="401" alt="image" src="https://github.com/user-attachments/assets/f74e10fc-1c27-4f4e-aadc-88b8157fb3ad" />

```
import seaborn as sns
import matplotlib.pyplot as plt

tips = sns.load_dataset('tips')

# Select numeric columns
num = tips.select_dtypes(include=['float64','int64']).columns

# Compute correlation
corr = tips[num].corr()

# Plot heatmap
sns.heatmap(corr, annot=True, cmap="YlGnBu")
plt.show()

```


<img width="526" height="342" alt="image" src="https://github.com/user-attachments/assets/b8b7cae7-9c93-421a-8119-8e29db4065ff" />

```
sns.heatmap(corr, annot=True, cmap="YlGnBu")
```

<img width="629" height="371" alt="image" src="https://github.com/user-attachments/assets/74ec422d-df44-476f-960b-2aa8808b6264" />

# Result:
The Program has been verified successfully
