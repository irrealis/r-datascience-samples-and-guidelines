# R Data-Science Samples and Guidelines
## 04 Exploratory Data Analysis
### 02 Exploratory Graphs
#### Questions and Answers:

- What are five simple summaries of data?

What are five simple summaries of data useful in exploratory analysis?  
- Five-number summary
- Boxplot and overlay
- Histogram, rug, and overlay
- Barplot
- Density plot

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

**To do: Describe a density plot.**

Write R code to compute a five-number summary of the U.S. EPA's annual mean fine particle pollution (PM2.5), given as a table named "`pollution`". (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
summary(pollution$pm25)
```

Write R code to display a boxplot of the U.S. EPA's annual mean fine particle pollution (PM2.5), given as a table named "`pollution`". (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
boxplot(pollution$pm25, col = "blue")
```

Write R code to display a boxplot of the U.S. EPA's annual mean fine particle pollution (PM2.5), given as a table named "`pollution`", including an overlay at 12 (the EPA standard limit). (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
boxplot(pollution$pm25, col = "blue")
abline(h = 12)
```

Write R code to display a histogram of the U.S. EPA's annual mean fine particle pollution (PM2.5), given as a table named "`pollution`". (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
hist(pollution$pm25, col = "green")
```

Write R code to display a histogram of the U.S. EPA's annual mean fine particle pollution (PM2.5), given as a table named "`pollution`", with 100 bars. (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
hist(pollution$pm25, col = "green", breaks = 100)
```

Write R code to display a histogram of the U.S. EPA's annual mean fine particle pollution (PM2.5), given as a table named "`pollution`", including rug. (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
hist(pollution$pm25, col = "green")
rug(pollution$pm25)
```

Write R code to display a histogram of the U.S. EPA's annual mean fine particle pollution (PM2.5), given as a table named "`pollution`", including overlays at 12 (the EPA standard limit) and the median (in magenta). (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
hist(pollution$pm25, col = "green")
abline(v = 12)
abline(v = median(pollution$pm25), col = "magenta")
```

Write R code to display a barplot of number of counties in each region for the U.S. EPA's annual mean fine particle pollution data, given as a table named "`pollution`". (If needed, download from https://raw.githubusercontent.com/DataScienceSpecialization/courses/master/04_ExploratoryAnalysis/exploratoryGraphs/data/avgpm25.csv.)  
```r
barplot(table(pollution$region), col = "wheat", main = "Number of Counties in Each Region")
```

**To do: Code for making a density plot.**
