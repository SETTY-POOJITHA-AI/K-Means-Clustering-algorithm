# Implementation of K-Means Clustering Algorithm
## Aim
To write a python program to implement K-Means Clustering Algorithm.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation

## Algorithm:

### Step1
import the necessary packages.

### Step2
read the csv file.

### Step3
scatter plot the applicant income and loan amount.

### Step4
obtain the kmean clustering for 2 classes.

### Step5
predict the cluster groupm of  applicant income and loanamount.

## Program:
```
import pandas as pdimport matplotlib.pyplot as plt
from sklearn.cluster import KMeans
import seaborn as sns

X1 = pd.read_csv('clustering.csv')
print (X1. head (2))
X2= X1.loc[:, ['ApplicantIncome', 'LoanAmount']] 
print(X2.head(2))

X=X2.values
sns.scatterplot(X[:,0], X[:, 1])
plt.xlabel('Income')
plt.ylabel('Loan')
plt.show()

kmean=KMeans(n_clusters=4)
kmean.fit(X)

print('Cluster Centers:', kmean.cluster_centers_)
print('Labels:', kmean.labels_)

#predict the class for ApplicantIncome 9000 and Loanamount 120 
predicted_class= kmean.predict([[9000, 120]])
print('The cluster group for ApplicantIncome 9000 and Loanamount 120 is', predicted_class)
```
## Output
![githublogo](clust.jpg)
![githublogo](clust1.jpg)
![githublogo](clust2.jpg)

## Result
Thus the K-means clustering algorithm is implemented and predicted the cluster class using python program.