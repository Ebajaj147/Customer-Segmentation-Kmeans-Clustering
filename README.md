In this project, I've worked on a real-world e-commerce sales data and segmented its customer base with Python, [scikit-learn library](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html) and [Plotly](https://plot.ly/python/plotly-express/). 

**The workflow of the project is as follows:**

1. **Business Case**
Primary Question: Can the customer date base be grouped to develop customized relationships?
This question will be tackled from a behavioural aspect to better understand customers’ spending and ordering habits with the following features: Number of products ordered, average return rate and total spending.

2. **Data Preparation**
There are approximately 25000 unique customers combined with their order information in the raw dataset. NA values have been filtered out.

3. **Segmentation with K-means Clustering**
We are going to use this algorithm since it is easy to understand, fits well to large datasets in terms of computing times and guarantees convergence. However, when centroids are initialized randomly, algorithm may not assign the points to the groups in the most optimal way. Hence Hyperparameter Tuning will be done next.

4. **Hyperparameter Tuning**
While selecting k, we are going to decide against the optimization criteria of the K-means, inertia, using the elbow method. We are going to build different K-means models with k values 1 to 15, and save the corresponding inertia values. At k=4, the descent stabilizes and continues linearly afterwards, forming an elbow at k=4. This points out the optimal number of customer group is 4.

5. **Visualization and Interpretation of the Results**
We approached the customer segmentation problem from a behavioural aspect with the number of products ordered, average return rate and total spending for each customer. Use of these 3 features helped us with the understandability and visualization of the model.
All in all, the dataset was apt to perform an unsupervised machine learning problem. 
At first, we only had customers data with order information and did not know if they belonged to any group. With the K-means clustering, patterns in the data were found and extended further into groups. We carved out strategies for the formed groups, making meaning out of a dataset that was a dust cloud initially.

The notebook has comments added to make the context of usage easier to understand.

**Outputs -**
1. Cluster Magnitude - Bar graph
<img width="1119" alt="Cluster Magnitude - Bar graph" src="https://user-images.githubusercontent.com/46665472/129740329-88a5b7ab-e998-4a3e-a899-acdcd420a3fc.png">

2. Scatter 3d - log_transformation customer segments with a 3D plot
<img width="1119" alt="Scatter 3d - log_transformation customer segments with a 3D plot" src="https://user-images.githubusercontent.com/46665472/129740368-faac2c76-38d9-437d-8b58-fa5281de8a15.png">

3. Subplots - 
<img width="793" alt="Subplots" src="https://user-images.githubusercontent.com/46665472/129740395-bcbe0885-f918-4831-970f-e8451d6d6d0a.png">

4. Within Cluster Sum of Squared Distances VS K Values - 
<img width="1162" alt="Within Cluster Sum of Squared Distances VS K Values" src="https://user-images.githubusercontent.com/46665472/129740439-0f1e44f6-b661-44da-8e1c-8ca08faf1e8b.png">


