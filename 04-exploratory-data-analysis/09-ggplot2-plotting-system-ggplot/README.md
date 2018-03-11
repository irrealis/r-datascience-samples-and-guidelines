# R Data-Science Samples and Guidelines
## 04 Exploratory Data Analysis
### 09 ggplot2 Plotting System - `ggplot`
#### Questions, Answers, Exercises:


What are the basic components of plot in the ggplot2 plotting system for R?  
- A **data frame** as input.
- **aesthetic mappings**: how data are mapped to color, size.
- **geoms**: geometric objects like points, lines, shapes.
- **facets**: for conditional plots.
- **stats**: statistical transformations like binning, quantiles, smoothing.
- **scales**: what scaling anaesthetic map uses (example: male = red, female = blue).
- **coordinate system**


Write R code to load the builtin "`mpg`" dataset, then scatterplot "`displ`" versus "`hwy`", using "`ggplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
g <- ggplot(mpg, aes(displ, hwy))
g + geom_point()
```


Write R code to load the builtin "`mpg`" dataset, then scatterplot "`displ`" versus "`hwy`" separating "`drv`" by color, using "`ggplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
g <- ggplot(mpg, aes(displ, hwy, color = drv))
g + geom_point()
```


Write R code to load the builtin "`mpg`" dataset, then plot "`displ`" versus "`hwy`" as both points and smoothing (via LOESS by default), using "`ggplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
g <- ggplot(mpg, aes(displ, hwy))
g + geom_point() + geom_smooth()
```


Write R code to load the builtin "`mpg`" dataset, then plot "`displ`" versus "`hwy`" as both points and linear regression, using "`ggplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
g <- ggplot(mpg, aes(displ, hwy))
g + geom_point() + geom_smooth(method = lm)
```


Write R code to load the builtin "`mpg`" dataset, then plot a histogram of "`hwy`", using "`ggplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
g <- ggplot(mpg, aes(hwy))
g + geom_histogram()
```


Write R code to load the builtin "`mpg`" dataset, then plot a histogram of "`hwy`" separating "`drv`" by fill color, using "`ggplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
g <- ggplot(mpg, aes(hwy, fill = drv))
g + geom_histogram()
```


Write R code to load the builtin "`mpg`" dataset, then plot a row of conditional scatterplots of "`displ`" versus "`hwy`" conditioned on "`drv`", using "`ggplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
g <- ggplot(mpg, aes(displ, hwy))
g + geom_point() + facet_grid(. ~ drv)
```


Write R code to load the builtin "`mpg`" dataset, then plot a column of conditional histograms of "`hwy`" conditioned on "`drv`", using "`ggplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
g <- ggplot(mpg, aes(hwy))
g + geom_histogram() + facet_grid(drv ~ .)
```


Write R code to load the builtin "`mpg`" dataset, then estimate a smooth density of "`hwy`", using "`ggplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
g <- ggplot(mpg, aes(hwy))
g + geom_density()
```


Write R code to load the builtin "`mpg`" dataset, then estimate a smooth density of "`hwy`" separating "`drv`" by fill color, using "`ggplot`" from the ggplot2 plotting system.  
```r
library(ggplot2)
data(mpg)
g <- ggplot(mpg, aes(hwy, color = drv))
g + geom_density()
```


Write R code to load the builtin "`mpg`" dataset, then estimate a smooth density of "`hwy`" separating "`drv`" by fill color, using "`ggplot`" from the ggplot2 plotting system. Use a white background with gray graticule, "Highway Mileage" as X label, "Probability Density" as Y label, "Drive Type" as legend title, and "Highway Mileage Distributions" as title.
```r
library(ggplot2)
data(mpg)
g <- ggplot(mpg, aes(hwy, color = drv))
g +
  geom_density() +
  theme_bw() +
  labs(x = "Highway Mileage") +
  labs(y = "Probability Density") +
  guides(color = guide_legend(title = "Drive Type")) +
  labs(title = "Highway Mileage Distributions")
```
