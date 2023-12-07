# Iris-Flower-Classification-using-Machine-learning
# **README: Iris Flower Classification**

---



> **Name: Bharath S**

> **Batch: November**

> **Domain: Data Science**

**Aim**

This project seeks to create a model capable of categorizing iris flowers into distinct species by analyzing their sepal and petal measurements.

**Libraries Used**
The following important libraries were used for this project:

numpy

*   Pandas

*   Sklearn.Cluster.KMeans

*  matplotlib.pyplot
*  seaborn

*   Dataset

The iris dataset was loaded using seaborn's load_dataset function, which contains information about iris flowers, including sepal length, sepal width, petal length, petal width, and species.

**Data Exploration and Preprocessing**

1) The dataset was loaded into a DataFrame using seaborn's load_dataset function, and the initial five rows were showcased via df.head().

2) Numeric encoding was applied to the 'species' column of the DataFrame using pd.factorize(df['species']).

3) Descriptive statistics of the dataset were presented using df.describe().

4) Examination of missing values in the dataset was performed through df.isna().sum().

**Data Visualization**

1) Utilizing matplotlib.pyplot and mpl_toolkits.mplot3d.Axes3D, 3D scatter plots were generated to illustrate the connections among species, petal length, and petal width, as well as among species, sepal length, and sepal width.

2) Seaborn.scatterplot was employed to craft 2D scatter plots, offering a visual depiction of the correlation between species and sepal length, as well as between species and sepal width.

**Applying Elbow Technique for K-Means Clustering**

1) The Elbow Technique was employed to ascertain the optimal number of clusters (K) by evaluating the sum of squared errors (SSE).

2) The KMeans algorithm was initiated with varying values of K (ranging from 1 to 10), and SSE was calculated for each K value.

3) A matplotlib.pyplot plot illustrating the relationship between K values and SSE was generated to pinpoint the "elbow point," signifying the optimal number of clusters.
   
**Applying K-Means Algorithm**

1)The KMeans algorithm was applied to the dataset with the optimal number of clusters (K=3) obtained from the Elbow Technique.

2)The cluster labels were predicted for each data point in the dataset using km.fit_predict(df[['petal_length','petal_width']]).

**Accuracy Measure**

1) The accuracy of the KMeans clustering was assessed by computing the confusion matrix.

2) The confusion matrix was visually represented by creating a plot using matplotlib.pyplot.imshow and plt.text, illustrating the true and predicted labels.
