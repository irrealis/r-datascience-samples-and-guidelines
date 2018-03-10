# R Data-Science Samples and Guidelines
## 04 Exploratory Data Analysis
### 04 Base Plotting System
#### Questions, Answers, Exercises:


Write R code to load the builtin "`airquality`" dataset, then plot a histogram of "`Ozone`" using the base plotting system.  
```r
data(airquality)
hist(airquality$Ozone)
```

Write R code to load the builtin "`airquality`" dataset, then scatterplot "`Wind`" versus "`Ozone`" using the base plotting system.  
```r
data(airquality)
with(airquality, plot(Wind, Ozone))
```

Write R code to load the builtin "`airquality`" dataset, convert "`Month`" to a factor variable, then boxplot "`Ozone`" as a function of "`Month`" using the base plotting system.  
```r
data(airquality)
airquality <- transform(airquality, Month = factor(Month))
boxplot(Ozone ~ Month, airquality)
```

Write R code to load the builtin "`airquality`" dataset, scatterplot "`Wind`" versus "`Ozone`", then set the main title to "Ozone and Wind in New York City" using the base plotting system.  
```r
data(airquality)
with(airquality, plot(Wind, Ozone))
title(main = "Ozone and Wind in New York City")
```

Write R code to load the builtin "`airquality`" dataset, scatterplot "`Wind`" versus "`Ozone`" with main title "Ozone and Wind in New York City", using the base plotting system.  
```r
data(airquality)
with(airquality, plot(Wind, Ozone))
title(main = "Ozone and Wind in New York City")
```

Write R code to load the builtin "`airquality`" dataset, scatterplot "`Wind`" versus "`Ozone`", and then use blue to redraw those points for which the month is May, using the base plotting system.  
```r
data(airquality)
with(airquality, plot(Wind, Ozone))
with(subset(airquality, Month == 5), points(Wind, Ozone, col = "blue"))
```


Write R code to load the builtin "`airquality`" dataset, then make an empty scatterplot of "`Wind`" versus "`Ozone`" using the base plotting system.  
```r
data(airquality)
with(airquality, plot(Wind, Ozone, type = "n"))
```

Write R code to load the builtin "`airquality`" dataset, make an empty scatterplot of "`Wind`" versus "`Ozone`", and then use blue to add those points for which the month is May, and red to add the remaining points, using the base plotting system.  
```r
data(airquality)
with(airquality, plot(Wind, Ozone, type = "n"))
with(subset(airquality, Month == 5), points(Wind, Ozone, col = "blue"))
with(subset(airquality, Month != 5), points(Wind, Ozone, col = "red"))
```

Write R code to load the builtin "`airquality`" dataset, make an empty scatterplot of "`Wind`" versus "`Ozone`", then add a legend to the top right with a blue circle for "May" and a red circle for "Other Months", using the base plotting system.  
```r
data(airquality)
with(airquality, plot(Wind, Ozone, type = "n"))
legend(
  "topright",
  pch = c(1,1),
  col = c("blue", "red"),
  legend = c("May", "Other Months")
)
```

Write R code to load the builtin "`airquality`" dataset, scatterplot "`Wind`" versus "`Ozone`", and then add a regression line, using the base plotting system.  
```r
data(airquality)
with(airquality, {
  plot(Wind, Ozone)
  abline(lm(Ozone ~ Wind))
})
```

Write R code to load the builtin "`airquality`" dataset, then create a panel of two scatterplots in a row of "`Wind`" versus "`Ozone`", and "`Solar.R`" versus "`Ozone`", using the base plotting system.  
```r
data(airquality)
par(mfrow = c(1, 2))
with(airquality, {
  plot(Wind, Ozone)
  plot(Solar.R, Ozone)
})
```
