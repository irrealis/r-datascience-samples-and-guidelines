# R Data-Science Samples and Guidelines
## 04 Exploratory Data Analysis
### 08 ggplot2 Plotting System - `qplot`
#### Questions, Answers, Exercises:


Write R code to load the builtin "`mpg`" dataset, then scatterplot "`displ`" versus "`hwy`", using "`qplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
qplot(displ, hwy, data = mpg)
```


Write R code to load the builtin "`mpg`" dataset, then scatterplot "`displ`" versus "`hwy`" separating "`drv`" by color, using "`qplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
qplot(displ, hwy, data = mpg, color = drv)
```


Write R code to load the builtin "`mpg`" dataset, then plot "`displ`" versus "`hwy`" as both points and smoothing (via LOESS by default), using "`qplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
qplot(displ, hwy, data = mpg, geom = c("point", "smooth"))
```


Write R code to load the builtin "`mpg`" dataset, then plot a histogram of "`hwy`", using "`qplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
qplot(hwy, data = mpg)
```


Write R code to load the builtin "`mpg`" dataset, then plot a histogram of "`hwy`" separating "`drv`" by fill color, using "`qplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
qplot(hwy, data = mpg, fill = drv)
```


Write R code to load the builtin "`mpg`" dataset, then plot a row of conditional scatterplots of "`displ`" versus "`hwy`" conditioned on "`drv`", using "`qplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
qplot(displ, hwy, data = mpg, facets = . ~ drv)
```


Write R code to load the builtin "`mpg`" dataset, then plot a column of conditional histograms of "`hwy`" conditioned on "`drv`", using "`qplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
qplot(hwy, data = mpg, facets = drv ~ .)
```


Write R code to load the builtin "`mpg`" dataset, then estimate a smooth density of "`hwy`", using "`qplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
qplot(hwy, data = mpg, geom = "density")
```


Write R code to load the builtin "`mpg`" dataset, then estimate a smooth density of "`hwy`" separating "`drv`" by fill color, using "`qplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
qplot(hwy, data = mpg, geom = "density", color = drv)
```


Write R code to load the builtin "`mpg`" dataset, then plot the values of "`hwy`" in the order in which they occur in "`mpg`", separating "`drv`" by fill color, using "`qplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
qplot(y = hwy, data = mpg, color = drv)
```


Write R code to load the builtin "`mpg`" dataset, then boxplot "`hwy`" versus "`mpg`", using "`qplot`" from the ggplot2 plotting system.  
```r
qplot(drv, hwy, data = mpg, geom = "boxplot")
```


Write R code to load the builtin "`mpg`" dataset, then boxplot "`hwy`" versus "`mpg`", separating "`manufacturer`" by color, using "`qplot`" from the ggplot2 plotting system.  
```r
qplot(drv, hwy, data = mpg, geom = "boxplot", color = manufacturer)
```
