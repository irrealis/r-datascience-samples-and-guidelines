# R Data-Science Samples and Guidelines
## 04 Exploratory Data Analysis
### 07 Lattice Plotting System
#### Questions, Answers, Exercises:


What are the main plotting functions in the Lattice plotting system for R?  
- "`xyplot`": this is the main function for creating scatterplots
- "`bwplot`": box-and-whiskers plots (“boxplots”)
- "`histogram`": histograms
- "`stripplot`": like a boxplot but with actual points
- "`dotplot`": plot dots on "violin strings"
- "`splom`": scatterplot matrix; like "`pairs`" in base plotting system
- "`levelplot`", "`contourplot`": for plotting "image" data


Explain the _formula notation_ of the form "`y~x|f*g`" used by "`xyplot`" in the Lattice plotting system for R.  
- On the left of the "`~`" is the Y-axis variable, on the right is the X-axis variable.
- "`f`" and "`g`" are optional  _conditioning variables_; the "`*`" indicates an interaction between them.

Write R code to load the builtin "`airquality`" dataset, then scatterplot "`Wind`" versus "`Ozone`" using the Lattice plotting system.  
```r
library(lattice)
data(airquality)
xyplot(Ozone ~ Wind, data = airquality)
```

Write R code to load the builtin "`airquality`" dataset, then scatterplot "`Wind`" versus "`Ozone`" with a regression line, using the Lattice plotting system.  
```r
library(lattice)
data(airquality)
xyplot(
  Ozone ~ Wind,
  data = airquality,
  panel = function(x, y, ...){    
    panel.xyplot(x, y, ...) ## First call default panel function
    panel.lmline(x, y) ## Overlay a simple linear regression line
  }
)
```

Write R code to load the builtin "`airquality`" dataset, convert "`Month`" to a factor variable, then scatterplot "`Wind`" versus "`Ozone`", conditioned on "`Month`", using the Lattice plotting system.  
```r
library(lattice)
data(airquality)
airquality <- transform(airquality, Month = factor(Month))
xyplot(Ozone ~ Wind | Month, data = airquality)
```
