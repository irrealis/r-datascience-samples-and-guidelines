# R Data-Science Samples and Guidelines
## 03 Getting and Cleaning Data
### 02 Downloading Files
#### Exercises:

ite R code to test whether directory "fubar" exists.
```R
file.exists("fubar")
```

Write R code to create directory "fubar".
```R
dir.create("fubar")
```

Write R code to download "https://github.com/irrealis/r-datascience-samples-and-guidelines/raw/master/03-getting-and-cleaning-data/02-downloading-files/README.md" to file "fubar/README.md".
```R
download.file(url = "https://github.com/irrealis/r-datascience-samples-and-guidelines/raw/master/03-getting-and-cleaning-data/02-downloading-files/README.md", destfile = "fubar/README.md", method = "curl")  
```
