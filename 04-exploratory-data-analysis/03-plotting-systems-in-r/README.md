# R Data-Science Samples and Guidelines
## 04 Exploratory Data Analysis
### 03 Plotting Systems in R
#### Questions and Answers:

What are three core plotting systems for R?  
- Base
- "`lattice`"
- "`ggplot2`"

What's the general procedure for plotting using the Base system in R?  
- Start with blank canvas and build up from there.
- Start with plot function (or similar).
- Use annotation functions to add/modify ("`text`", "`lines`", "`points`", "`axis`").

What's the general procedure for plotting using the "`lattice`" system in R?  
- Plots are created with a single function call ("`xyplot`", "`bwplot`", etc.).

What's the general procedure for plotting using the "`ggplot2`" system in R?  
- Uses _Grammar_ of _Graphics_ graphing language.
- Splits the difference between Base and "`lattice`" in a number of ways.

What are pros and cons of the Base plotting system in R?  
- Pros:
  - Convenient "Artist's palette" model matches how we think of building plots and analyzing data.
  - Simple series of R commands.
- Cons:
  - To be able to reconstruct, must keep track of all commands used.
  - Can't go back once plot has started (i.e. to adjust margins).
  - Hard to "translate" plots to other systems (no graphical "language").

What are pros and cons of the "`lattice`" plotting system in R?  
- Pros:
  - Useful for conditioning plots: how Y changes with X across levels of Z.
  - Good for making many many plots at once.
- Cons:
  - Requires use of conditioning model.
  - Can be awkward to specify entire plot in one call.
  - Annotation can be nonintuitive.
  - Use of panel functions and subscripts is unwieldy, requires intense prep.
  - Cannot "add" to plot once created.

What are pros and cons of the "`lattice`" plotting system in R?  
- Pros:
  - Default mode makes many choices for your.
  - Highly customizable.
  - Automatically deals with spacings, text, titles.
  - Allows annotation by adding to a plot.
  - Superficial similarity to "`lattice`" but easier and more intuitive.
  - Useful for conditioning plots.
- Cons:
  - None mentioned by Peng.

Write R code to make a scatter plot of speed versus distance for the builtin dataset "`cars`", using the Base plotting system.  
```r
data(cars)
with(cars, plot(speed, dist))
```

Write R code to make panel of scatterplots of "`Income`" versus "`Life.Exp`" given "`region`" for the builtin dataset "`state`", using the "`lattice`" plotting system.  
```r
library(lattice)
data(state)
state <- data.frame(state.x77, region = state.region)
xyplot(Life.Exp ~ Income | region, data = state, layout = c(2, 2))
```

Write R code to make a scatterplot of "`displ`" versus "`hwy`" for the builtin dataset "`mpg`", using the "`ggplot2`" plotting system.  
```r
library(ggplot2)
data(mpg)
qplot(displ, hwy, data = mpg)
```
