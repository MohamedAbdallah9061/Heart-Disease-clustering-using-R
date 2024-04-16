# Heart-Disease-clustering-using-R
## R Program to clustering heart disease based on different features

### • Pre-processing
##### removed dublicated rows.
##### removed (id) column from dataset as it not important feature.
##### replaced null values in (slope) column by mode (most frequent value) which defined in the script.
##### converted (age) column to categories based on specific intervals.
##### converted the (age) and (oldpeak) columns to integer as age is factor.
##### Dealt with outliers based on box plot visualization:
##### - (trestbps) column contained outliers when value > 170.
##### - (chol) column contained outliers when value > 360.
##### - (thalach) column contained outliers when value < 100.
##### then replaced outliers by median.

##### then based on correlation matrix that was calculated and visualized (sex, fbs, chol) columns had removed as they had low correlation value compared with other features.

### • Models
##### three clustering models had applied are:
##### 1) Kmeans
##### Kmeans result when using K = 5 based on (thalach, trestbps) features:
![Picture1](https://github.com/MohamedAbdallah9061/Heart-Disease-clustering-using-R/assets/100321888/71410035-f0d0-486b-8291-3016f905cb18)
##### 2) Dbscan
##### Dbscan result when using eps = 6, MinPts =  5 based on (thalach, trestbps) features:

![Picture2](https://github.com/MohamedAbdallah9061/Heart-Disease-clustering-using-R/assets/100321888/fe440fd5-05de-456a-bb9a-2013cebe0dd5)

##### Dbscan clustered the data into 8 clusters.

##### 3) hierarchical clustering: there is 2 linkage types are complete and single hierarchical clustering models:

##### •	complete link: link 2 clusters based on the max distance between 2 elements.


![Picture6](https://github.com/MohamedAbdallah9061/Heart-Disease-clustering-using-R/assets/100321888/5b52a507-3e4e-48ec-a94f-0a968f917041)

##### •	single link: link 2 clusters based on the min distance between 2 elements.

![Picture4](https://github.com/MohamedAbdallah9061/Heart-Disease-clustering-using-R/assets/100321888/55cfdc0f-6424-4658-8245-b1b5421e5bb7)

##### complete or single link clustered the data into 5 clusters but complete hierarchical clustering model gived better perfomance.
