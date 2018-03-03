# R Data-Science Samples and Guidelines
## 03 Getting and Cleaning Data
### 03 Reading and Writing Flat Files
#### Exercises:

Write R code to download and read the table stored in "https://raw.githubusercontent.com/irrealis/r-datascience-samples-and-guidelines/master/03-getting-and-cleaning-data/03-rw-flat-files/cars.txt" into variable "`cars`". Note that "cars.txt" contains headers.
```R
u <- "https://raw.githubusercontent.com/irrealis/r-datascience-samples-and-guidelines/master/03-getting-and-cleaning-data/03-rw-flat-files/cars.txt"
cars <- read.table(u, header = T)
```

Write R code to load the builtin "`cars`" dataset, then write the table into "cars.txt" without row names.
```R
data("cars")
write.table(cars, "cars.txt", row.names = F)
```

Write R code to download and read the table stored in "https://raw.githubusercontent.com/irrealis/r-datascience-samples-and-guidelines/master/03-getting-and-cleaning-data/03-rw-flat-files/cars.csv" into variable "`cars`".
```R
u <- "https://raw.githubusercontent.com/irrealis/r-datascience-samples-and-guidelines/master/03-getting-and-cleaning-data/03-rw-flat-files/cars.csv"
cars <- read.csv(u)
```

Write R code to load the builtin "`cars`" dataset, then write the table into "cars.csv" without row names.
```R
data("cars")
write.csv(cars, "cars.csv", row.names = F)
```

Write R code to download and read the table stored in "https://raw.githubusercontent.com/irrealis/r-datascience-samples-and-guidelines/master/03-getting-and-cleaning-data/03-rw-flat-files/cars.csv2" into variable "`cars`". Note that "cars.csv2" uses "`;`" as separator, and "`,`" as decimal point.
```R
u <- "https://raw.githubusercontent.com/irrealis/r-datascience-samples-and-guidelines/master/03-getting-and-cleaning-data/03-rw-flat-files/cars.csv"
cars <- read.csv(u)
```

Write R code to load the builtin "`cars`" dataset, then write the table into "cars.csv2" without row names, using "`;`" as separator and "`,`" as decimal point.
```R
data("cars")
write.csv2(cars, "cars.csv2", row.names = F)
```

