# dimensionality-reduction-on-microbiome-dataset
I performed PCA and t-SNE on the microbiome dataset and visualized the data in 2D space. I also report what I learned from the PCA and t-SNE analyses.

## Dataset
The dataset includes the microbiome profiles of 344 people, some with type 2 diabetes, and others without. The microbiome profile for a person stores the relative abundance of different bacterial specie found in the stool sample collected from that person. The last column shows the class (with diabetes or not), and the other columns are for the relative abundances.

## Dimensionality Reduction

### PCA
Principal Component Analysis (PCA) is a technique through which it is possible to visualize data of higher dimensional space in a lower dimensioanl space. Here dimesions are nothing but features. It is a linear dimensionality reduction technique that preserves the essential parts that have more variation of the data and removes the less essential parts that have less variation of the data. It orthogonally transforms the set of values of possibly correlated variables into a set of values of linearly uncorrelated variables that are known as principal components.

### t-SNE
T-Distributed Stochastic Neighbouring Entities (t-SNE) is a probabilistic technique to visualize the high dimensional data sets. It is also a technique for dimensionality reduction, but it is a non-linear one. Two distributions play a role here. One of them measures pairwise similarities of the input objects and the other one measures pairwise similarities of the corresponding low-dimensional points in the embedding. This way, mapping of the multi-dimesnional data to a lower dimensional space is carried out by t-SNE where it attempts to find patterns in the data by identifying clusters based on similarity of data points with multiple features. Also, the input features are not identifiable after the output of t-SNE is generated.

## Analyses

### PCA
- The microbiome dataset had a huge number of dimensions i.e. 572 dimensions. It would have been extremely difficult to analyze the data set and also, plotting so many attributes would have been cumbersome. When a threshold value is surpassed by the number of dimensions, then the accuracy decreases. This leads to the Curse of Dimensionality.
- To deal with the above stated issue, the approach of Principal Component Analysis helped in the reducing the dimensionality of this data set from 572 dimensions to 2 dimensions.
- The principal component 1 holds 5.77% of the information where as the principal component 2 holds 3.88 % of the information. While projecting data from 572 dimensions to 2 dimensions, 90.35% of the information was lost. Hence, we were not able to retain almost all of the variance.
- This shows that PCA was not a good approach for this data set.
- Cluster of people can be seen according to the status of their disease i.e. red for people who have type 2 diabetes and green for people who do not have diabetes. However, the clusters are linearly not separable as they almost overlap with each other in the 2D space. A few users from the green cluster (no diabetes) are scattered in the 2D space.

### t-SNE
- The microbiome dataset had a huge number of dimensions i.e. 572 dimensions. It would have been extremely difficult to analyze the data set and also, plotting so many attributes would have been cumbersome. When a threshold value is surpassed by the number of dimensions, then the accuracy decreases. This leads to the Curse of Dimensionality.
- To deal with the above stated issue, the approach of t-SNE helped in the reducing the dimensionality of this data set from 572 dimensions to 2 dimensions.
- The relevant information is in the relative distances between low dimensional points. t-SNE captures structure such that the neighboring points in the input space will tend to be neighbors in the low dimensional space.
- Since the identified clusters are almost overlapping with each other, t-SNE cannot be considered as a good approach for this data set.
- Cluster of people can be seen according to the status of their disease i.e. red for people who don't have diabetes and blue for people who have type 2 diabetes. However, the clusters are linearly not separable as they almost overlap with each other in the 2D space. A few users from the blue and red clusters are scattered in the 2D space.
