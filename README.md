# Workshop-Multivariate-analysis
## Aim
To perform Bivariate/Multivariate EDA on the given data set.

## Explanation 
Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

## Algorithm
## Step 1
Import built-in libraries required to perform EDA.

## Step 2
Read the given csv file.

## Step 3
Convert the file into a dataframe and get info of the data.

## Step 4
Return the objects containing counts of unique values using (value_counts()).

## Step 5
Plot the counts in the form of Histogram or Bar Graph.

## Step 6
Use seaborn the bar graph comparison of data can be viewed.

## Step 7
Find the pairwise correlation of all columns in the dataframe.corr()


## Types of bivariate analyis

1. Numerical & Numerical (Scatter plot)
2. Numerical & Categorical (Bar plot,Box plot,Dist plot)

## Program
```python
Developed by : UDAYAKUMAR R
Reg No: 212222230163

import pandas as pd
import numpy as py
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv('FlightInformation.csv')
df.head()
plt.xticks(rotation = 90)
sns.scatterplot(x=df['Airline'],y=df['Price'],data=df)
df.info()
states=df.loc[:,["Source","Price"]]
states=states.groupby(by=["Source"]).sum().sort_values(by="Price")
sns.barplot(x=states.index,y="Price",data=states)
plt.xticks(rotation = 0)
plt.xlabel=("Source")
plt.ylabel=("Price")
plt.show()
df.corr()
sns.heatmap(df.corr(),annot=True)
```
## Output

### DATA HEAD
![image](https://user-images.githubusercontent.com/118708024/230123562-647c6182-fb8a-4ece-8c1f-8ee790c54088.png)
### DATA INFO
![image](https://user-images.githubusercontent.com/118708024/230124197-ec56d54f-f006-4e73-865f-5951924dc791.png)
### SCATTER PLOT
![image](https://user-images.githubusercontent.com/118708024/230124370-e8d24485-b54f-4888-83b8-eaff6012fad2.png)
### BAR PLOT
![image](https://user-images.githubusercontent.com/118708024/230124524-11ce881b-24ce-4460-a27d-9dab22696441.png)
### CORRELATION
![image](https://user-images.githubusercontent.com/118708024/230125973-1bb10a60-2d92-468c-b114-5feff8846419.png)
### HEATMAP
![image](https://user-images.githubusercontent.com/118708024/230125799-5597a906-1df9-45a0-bd7a-3ccb645c091e.png)

## Result
Thus we have performed Bivariate/Multivariate EDA on the given data set.







