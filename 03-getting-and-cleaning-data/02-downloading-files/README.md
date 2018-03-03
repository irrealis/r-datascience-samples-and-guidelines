# R Data-Science Samples and Guidelines
## 03 Getting and Cleaning Data
### 02 Downloading Files
#### Exercises:

Write R code to test whether directory "fubar" exists.
```R
file.exists("fubar")
```

Write R code to create directory "fubar".
```R
dir.create("fubar")
```

Write R code to download "https://raw.githubusercontent.com/irrealis/r-datascience-samples-and-guidelines/master/03-getting-and-cleaning-data/02-downloading-files/README.md" to file "README.md".
```R
u <- "https://raw.githubusercontent.com/irrealis/r-datascience-samples-and-guidelines/master/03-getting-and-cleaning-data/02-downloading-files/README.md"
download.file(url = u, destfile = "README.md", method = "curl")
```
