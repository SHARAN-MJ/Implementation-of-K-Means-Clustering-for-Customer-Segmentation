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
![Screenshot 2023-10-26 091920](https://github.com/SHARAN-MJ/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119560305/e8f246bf-63bc-4ab1-b168-c5e2a85afdc0)
![Screenshot 2023-10-26 091931](https://github.com/SHARAN-MJ/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119560305/3a5fdc44-f974-478c-9311-b005fff9b4c1)
![Screenshot 2023-10-26 091939](https://github.com/SHARAN-MJ/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119560305/865bea15-918e-45d0-b0fc-ef778270122e)
![Screenshot 2023-10-26 091955](https://github.com/SHARAN-MJ/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119560305/c767f326-b01b-47f3-8225-234082c1002a)

![Screenshot 2023-10-26 092053](https://github.com/SHARAN-MJ/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119560305/b7428319-a32e-4e97-b1ec-da7f87ae4b4d)
![Screenshot 2023-10-26 092040](https://github.com/SHARAN-MJ/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119560305/9ed9835f-213a-4136-8fb5-ec60a5196f96)
![Screenshot 2023-10-26 092114](https://github.com/SHARAN-MJ/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119560305/778bff40-90e3-40a0-b5db-67bf8d43467d)

![Screenshot 2023-10-26 092122](https://github.com/SHARAN-MJ/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119560305/1ce5ec4e-3562-480e-b16f-e16f2dfbcef2)





## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
