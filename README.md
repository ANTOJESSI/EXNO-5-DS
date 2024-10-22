# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
 Include the necessary coding and corresponding screenshots
 # -*- coding: utf-8 -*-
"""ExNo5DS.ipynb

Automatically generated by Colab.

Original file is located at
    https://colab.research.google.com/drive/15YF_yP48Du0jWexlp4IVBOld2l2pGMXQ
"""

import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

x_values = [0,1, 2, 3, 4, 5]
y_values = [0,1,4,9,16,25]
plt.plot(x_values,y_values)

plt.show()
![image](https://github.com/user-attachments/assets/9085d16f-6a1c-4b20-a016-299d40b7270f)


x1 = [1,2,3]
y1 = [2,4,1]
plt.plot(x1,y1)
![image](https://github.com/user-attachments/assets/b3ceccb1-e60b-4538-99d6-cc2e3cd8c922)

plt.plot(x1,y1)
plt.ylabel('y-axis')
plt.xlabel('x-axis')
plt.title('My first graph!')
![image](https://github.com/user-attachments/assets/f99b77c3-ed23-4d02-b5ba-cf68dc79473d)

x1 = [1,2,3]
y1 = [2,4,1]
x2 = [1,2,3]
y2 = [4,1,3]
plt.plot(x1,y1,label="line 1")
plt.plot(x2,y2,label="line 2")
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Two lines on same graph')
plt.legend()
plt.show()
![image](https://github.com/user-attachments/assets/8ca50282-2749-47dd-a45b-a59904a2b68a)

x = [0,1, 2, 3, 4, 5]
y = [0,1,4,9,16,25]
plt.plot(x,y,color='green',linestyle='dashed',linewidth=3,marker='o',markerfacecolor='blue',markersize=12)
plt.ylim(1,8)
plt.xlim(1,8)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
![image](https://github.com/user-attachments/assets/be80fa27-5b95-40af-899b-4bcb4d9f3ab3)

# Scatter Plot example
x = [1, 2, 3, 4, 5]
y = [10, 20, 25, 30, 40]

plt.scatter(x, y, color='r')
plt.title('Scatter Plot')
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.show()
![image](https://github.com/user-attachments/assets/6c4d1a72-6187-4c21-a503-9651568c26ff)

# Area Chart example
x = [1, 2, 3, 4]
y = [10, 20, 30, 40]

plt.fill_between(x, y, color='green', alpha=0.5)
plt.title('Area Chart')
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.show()
![image](https://github.com/user-attachments/assets/74d15711-8714-42ca-9e15-af6c911539d3)

# Box Plot example
data = [7, 13, 23, 45, 10, 15]

plt.boxplot(data)
plt.title('Box Plot')
plt.show()
![image](https://github.com/user-attachments/assets/c3987ca8-c7dd-4d23-9355-b6042a46270d)

import numpy as np
import matplotlib.pyplot as plt
from scipy.interpolate import make_interp_spline

# Original data
x = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
y = np.array([2, 4, 5, 7, 8, 8, 9, 10, 11, 12])

# Creating a cubic spline interpolation
x_smooth = np.linspace(x.min(), x.max(), 300)
y_smooth = make_interp_spline(x, y)(x_smooth)
![image](https://github.com/user-attachments/assets/a6de4127-96a6-4bf1-adba-b03c365147c1)

# Plot
plt.plot(x_smooth, y_smooth)
plt.title('Cubic Spline Interpolation')
plt.show()

import matplotlib.pyplot as plt

# Data for bar graph
values = [5, 6, 3, 7, 2]
names  = ["A", "B", "C", "D", "E"]
colors = ['red', 'green', 'blue', 'purple', 'orange']

# Plotting the bar graph
plt.bar(names, values, color=colors)
plt.xlabel('Categories')
plt.ylabel('Values')
plt.title('Bar Graph Example')
plt.show()
![image](https://github.com/user-attachments/assets/db604d4e-d55a-497c-afc7-8a481a0745de)

import seaborn as sns
import matplotlib.pyplot as plt

# Loading a dataset
df = sns.load_dataset("tips")

# Calculating average values
avg_total_bill = df.groupby("day")["total_bill"].mean()
avg_tip = df.groupby("day")["tip"].mean()

# Plotting stacked bar chart
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
![image](https://github.com/user-attachments/assets/aaa09be4-1853-426e-9f7a-d76e81f414d2)

# Set the labels and title
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
plt.show()

import matplotlib.pyplot as plt

# Defining labels and slices
activities = ['Eat', 'Sleep', 'Work', 'Play']
slices = [3, 7, 8, 6]
colors = ['r', 'y', 'g', 'b']

# Plot pie chart
plt.pie(slices, labels=activities, colors=colors, startangle=90, shadow=True, explode=(0, 0.1, 0, 0), autopct='%1.1f%%')
![image](https://github.com/user-attachments/assets/30e3ea06-c6cd-48e8-9ae8-1893f59e8269)

# Set the title
plt.title('Pie Chart Example')
plt.show()

import matplotlib.pyplot as plt

# x and y axis values
x = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
y = [2, 4, 5, 7, 6, 8, 9, 11, 12, 12]

# Scatter plot with custom marker
plt.scatter(x, y, label="stars", color="green", marker="*", s=30)

# Set x and y axis labels
plt.xlabel('x-axis')
plt.ylabel('y-axis')

# Title and legend
plt.title('Scatter Plot Example')
plt.legend()
plt.show()

![image](https://github.com/user-attachments/assets/e4428627-10a4-4c26-958f-0e81677c1a6b)


# Result:
 Data Visualization using matplot python library for the given datas is successfully performed.
