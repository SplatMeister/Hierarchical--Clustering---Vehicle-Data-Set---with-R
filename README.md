# Hierarchical--Clustering---Vehicle-Data-Set---with-R
Based on the analysis on the vehicle data set, hierarchical clustering is performed to group similar items and identify natural groupings among the data set. Since the data set is a large data set, by performing hierarchical clustering, to identify the groupings and clusters.
Hierarchical Clustering
Introduction

Based on the analysis on the vehicle data set, hierarchical clustering is performed to group similar items and identify natural groupings among the data set. Since the data set is a large data set, by performing hierarchical clustering, to identify the groupings and clusters.
Prior to performing the clustering, the data set is preprocessed and remove any outliers. To do so using z score method to remove outliers. The below box plot visualizes the outliers in the original vehicle data set (Appendix 2.2.1).
 
Figure 1 Box Plot (Original)
The below box plot visualizes the outliers removed. From846 observations, the data set is reduced to 824. This process will help in providing more accurate result in performing clustering. 







Thereafter the data set needs to be scaled for better analysis and compare results.
 
Figure 2 Box Plot (After Removing Outliers)
 
2.2.1 Performing Hierarchical Clustering

To perform hierarchical clustering can be broken to several methods based and will be applied for the data set.
Single Linkage clustering

The single linkage clustering methods clustering takes the distance between the closest two data points in other cluster and measure the similarity. 
Based on the clustering there is a large of number clusters that are generated and there is a large noise in the visual therefore, resulting in deciding the right number of clusters. Therefore, based on the single linkage clustering, the cutoff is set at 0.5. Where it provides a moderate level of clustering and cannot garner any large insights. The set cut off is set too low, there will be many clusters. However, based on the demarcation there are large number of overlapping clusters (Appendix 2.2.1.a). 
 
Figure 3 Dendrogram Single Linkage

















Complete Linkage Clustering

The linkage clustering method usus the maximum distance between two data points in other clusters. 
Based on the results of complete linkage dendrogram based on the results the clusters are more uniform at the cut off mark of 0.5. Based on the dendrogram there are 10 clusters that are visible (Appendix 2.2.1.b).
 
Figure 4 Dendrogram Complete Linkage








Average Link Clustering

Average link clustering involves using the average distance between all pairs in different clusters as the criterion for merging clusters.
Based on the output the clusters are more compact and balanced. Since this quite a large data set, the output is unified. In relation to the number of clusters, the cut off mark places the number of clusters at 15 (Appendix 2.2.1.c).
 
Figure 5 Dendrogram Average Linkage
 











Ward’s linkage Clustering

This method takes the sum of squared difference between the data points in other clusters as the criterion for merging clusters. The clusters are compact in nature and the method uses bottom-up approach. Based on the output there are 3 visible clusters (Appendix 2.2.1.d). 
 
Figure 7 Dendrogram Ward's Linkage









2.2.2 Cophenetic Correlation

By using cophenetic correlation is useful to validate the clusters. This will help identify similarities between the original pairwise distance between data points and the distance against the dendrograms. After performing single, complete, average and ward’s clustering methods. The dendrograms can be calculated the cophenetic correlation between each pair (Appendix 2.2.2.a).  
	Single 	Complete 	Average 	Ward's 
Single 	1.0000000	0.2218542	0.2663212	0.1055871
Complete 	0.2218542	1.0000000	0.7745512	0.6321823
Average	0.2663212	0.7745512	1.0000000	0.7298611
Ward's 	0.1055871	0.6321823	0.7298611	1.0000000

Based on the above output, the quality of the dendrogram can be evaluated and compare the different clustering methods. Higher value of cophenetic correlation generally indicate better quality in the clustering. The complete and average correlation value of 0.7745512 has the highest relationship.










2.2.3 Coorplot Function

Based on the out put and generating the cophenetic correlation, it is important to visualize to derive insights (Appendix 2.2.3).
 
Figure 8 Coorplot
The coorplot, generates a matrix with correlations to better visualize the output of cophenetic correlation. Overall, the values for all four methods against the same are high. Therefore, this will not give us any insights. However, Single linkage has the lowest cohpetic correlation among the four. Therefore, single linkage is the least effective than other methods. Furthermore, complete linkage and average linage similar cophenetic correlation. Therefore, average linkage is more effective than complete linkage. 
