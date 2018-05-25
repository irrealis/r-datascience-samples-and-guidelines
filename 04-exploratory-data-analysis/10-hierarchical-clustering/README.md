# R Data-Science Samples and Guidelines
## 04 Exploratory Data Analysis
### 10 Hierarchical Clustering
#### Questions and Answers:


What are two primary requirements of hierarchical clustering? 
- Distance metric
- Merging procedure


What are three commonly used distance/similarity metrics? 
- Euclidean distance
- Correlation similarity
- Manhattan distance


Generate hierarchical clusters using _Euclidean metric_ and _complete linkage_ for the following dataframe: 
```r
set.seed(0)
df <- data.frame(x=rnorm(12, y=rnorm(12))
plot(df,pch=19,cex=0.3)
text(df+0.02,labels=as.character(1:12))
```
```r
d <- dist(df, method="euclidean")
h <- hclust(d, method="complete")
plot(h)
```
