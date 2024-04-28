# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas and matplotlib.pyplot  
2.Read the dataset and transform it  
3.Import KMeans and fit the data in the mode
4.Plot the Cluster graph 

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: lokesh khanna R
RegisterNumber: 212222040088
import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("/content/Mall_Customers (1) (1).csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss = [] #Within-Cluster sum of square.
for i in range(1,11):
  kmeans=KMeans(n_clusters = i,init = "k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km = KMeans(n_clusters = 5)
km.fit(data.iloc[:,3:])
y_pred = km.predict(data.iloc[:,3:])
y_pred
data["cluster"] = y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-
100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-
100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-
100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-
100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-
100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segments")
*/
```

## Output:
## data.head()
![image](https://github.com/Abinavsankar/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119103734/5593cd83-800e-413b-83ef-c555adc904c3)

## data.info()
![image](https://github.com/Abinavsankar/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119103734/baee0130-e9fb-431d-a4dd-913b7ac2fe73)

## data.isnull()
![image](https://github.com/Abinavsankar/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119103734/d745e5fb-e0e0-465f-bfc2-850e81944391)

## Elbow method Graph
![image](https://github.com/Abinavsankar/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119103734/c6c77bd1-f687-42b3-9d9d-c06799845566)

## Kmeans cluster
![image](https://github.com/Abinavsankar/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119103734/7fa2c429-c84f-4159-9012-fd27028e94bd)

## Cluster segments Graphs
![image](https://github.com/Abinavsankar/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119103734/c49ec1bc-8695-4f8d-b44f-05fb5e99ad53)



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
