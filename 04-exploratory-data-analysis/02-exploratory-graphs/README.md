# R Data-Science Samples and Guidelines
## 04 Exploratory Data Analysis
### 02 Exploratory Graphs
#### Questions and Answers:

What are some advantages of exploratory plots?
- They're quick and dirty.
- They quickly summarize data, highlighting broad features.
- They explore basic questions/hypotheses (perhaps rule them out).
- They suggest subsequent modeling strategies.

What are five simple one-dimensional summaries of data useful in exploratory analysis?  
- Five-number summary
- Boxplot and overlay
- Histogram, rug, and overlay
- Density plot (kernel density estimation)
- Barplot

What's a simple two-dimensional summary of data useful in exploratory analysis?  
Scatterplot.

Describe a traditional five-number summary.  
The traditional five numbers are:
- Minimum
- First quartile
- Median
- Third quartile
- Maximum
- **Note: R summaries include a sixth number, the mean.**

Describe a boxplot.  
The boxplot graphically shows:
- A box whose lower and upper boundaries indicate first and third quartiles.
- The median, indicated by a line usually inside the quartile box.
- Extremes, indicated usually by bars or dots above and below the quartile box.
  - **Note: R boxplot extremes exclude outliers.**
- "Whisker" lines, drawn between the quartile box and the extremes, help to locate the extremes visually.

How are barplots used?  
Barplots are good for summarizing categorical data.

**To do: Describe a histogram.**

**To do: Describe a density plot.**

Write R code download and load the table at https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv, with column classes ("numeric", "character", "factor", "numeric", "numeric"), storing the result in "`pollution`".  
```r
pollution <- read.csv("https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv", colClasses = c("numeric", "character", "factor", "numeric", "numeric"))
```

Write R code to compute a five-number summary of the U.S. EPA's annual mean fine particle pollution (PM2.5), given as a table named "`pollution`". (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
summary(pollution$pm25)
```

Write R code to display a boxplot of the U.S. EPA's annual mean fine particle pollution (PM2.5), given as a table named "`pollution`". (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
boxplot(pollution$pm25)
```

Write R code to display a boxplot of the U.S. EPA's annual mean fine particle pollution (PM2.5), given as a table named "`pollution`", including an overlay at 12 (the EPA standard limit). (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
boxplot(pollution$pm25)
abline(h = 12)
```

Write R code to display a histogram of the U.S. EPA's annual mean fine particle pollution (PM2.5), given as a table named "`pollution`". (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
hist(pollution$pm25)
```

Write R code to display a histogram of the U.S. EPA's annual mean fine particle pollution (PM2.5), given as a table named "`pollution`", with 100 bars. (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
hist(pollution$pm25, breaks = 100)
```

Write R code to display a histogram of the U.S. EPA's annual mean fine particle pollution (PM2.5), given as a table named "`pollution`", including rug. (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
hist(pollution$pm25)
rug(pollution$pm25)
```

Write R code to display a histogram of the U.S. EPA's annual mean fine particle pollution (PM2.5), given as a table named "`pollution`", including overlays at 12 (the EPA standard limit) and the median (in magenta). (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
hist(pollution$pm25)
abline(v = 12)
abline(v = median(pollution$pm25), col = "magenta")
```

Write R code to display a kernel density estimation of the U.S. EPA's annual mean fine particle pollution (PM2.5), given as a table named "`pollution`". (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
plot(density(pollution$pm25))
```

Write R code to display a barplot of number of counties in each region for the U.S. EPA's annual mean fine particle pollution data, given as a table named "`pollution`". (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
barplot(table(pollution$region), main = "Number of Counties in Each Region")
```

Write R code to display a scatterplot of "`latitude`" (X axis) versus "`pm25`" (Y axis) for the U.S. EPA's annual mean fine particle pollution data, given as a table named "`pollution`". (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
with(pollution, plot(latitude, pm25))
```

Write R code to display a scatterplot of "`latitude`" (X axis) versus "`pm25`" (Y axis) for the U.S. EPA's annual mean fine particle pollution data, given as a table named "`pollution`", using color to indicate "`region`" (a factor variable). (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
with(pollution, plot(latitude, pm25, col = region))
```

Write R code to display a column of two histogram of the U.S. EPA's annual mean fine particle pollution (PM2.5), for regions "`east`" and "`west`" respectively, given as a table named "`pollution`". (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
par(mfrow = c(2, 1))
hist(subset(pollution, region == "east")$pm25)
hist(subset(pollution, region == "west")$pm25)
```

Write R code to display row of two scatterplots of "`latitude`" (X axis) versus "`pm25`" (Y axis) for the U.S. EPA's annual mean fine particle pollution data, for regions "`east`" and "`west`", respectively, given as a table named "`pollution`". (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
par(mfrow = c(1, 2), mar = c(5, 4, 2, 1))
with(subset(pollution, region == "west"), plot(latitude, pm25, main = "West"))
with(subset(pollution, region == "east"), plot(latitude, pm25, main = "East"))
```
