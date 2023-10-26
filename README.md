# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:
```
1.Import the necessary packages using import statement.
2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().
3.Import KMeans and use for loop to cluster the data.
4.Predict the cluster and plot data graphs.
5.Print the outputs and end the program
```
## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: SHARAN MJ
RegisterNumber: 212222240097
import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("/content/Mall_Customers (1) (1).csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans
wcss = []

for i in range(1,11):
  kmeans = KMeans(n_clusters = i,init = "k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
  
  plt.plot(range(1,11),wcss)
plt.xlabel("No. of clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")

Km = KMeans(n_clusters = 5)
Km.fit(data.iloc[:,3:])

y_pred=Km.predict(data.iloc[:,3:])
y_pred

data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segmets")
*/

```

## Output:
![image](https://github.com/Harinimuthu17/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/130278614/0e538715-aca3-483b-87b2-b9664bbdc876)
![image](https://github.com/Harinimuthu17/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/130278614/6325d3e6-e138-4d34-9bf1-af1dddf98d84)
![image](https://github.com/Harinimuthu17/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/130278614/a01027bd-3904-4f8d-b6b1-0648a2af7402)
![image](https://github.com/Harinimuthu17/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/130278614/b94d9495-82fa-4849-a902-86f393c24cd7)
![image](https://github.com/Harinimuthu17/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/130278614/6d97c5f9-6029-4ed4-b1c0-83a7f2772769)
![image](https://github.com/Harinimuthu17/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/130278614/d80d492b-5c6a-4def-9dd9-3c8ae880837e)
![image](https://github.com/Harinimuthu17/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/130278614/3bce4af7-d576-4fa3-a7a8-3c8b09876607)
![image](https://github.com/Harinimuthu17/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/130278614/e82e260c-dbc0-4b6d-98c5-030b1af10580)



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
