# R Data-Science Samples and Guidelines
## 03 Getting and Cleaning Data
### 01 Components of Tidy Data
#### Questions and Answers:

What are the components of reproducible data?  
- Original *raw data*.
- Processed *tidy data*.
- *Code book* describing tidy data.
- *Reproducible instructions* for processing raw to tidy.

What criteria must raw data meet?  
- You ran no software on the raw data.
- Nothing was changed.
- Nothing was removed.
- Nothing was added. In particular, no summary.

What criteria must tidy data meet?  
- One variable per column. Descriptive column names.
- One observation per row.
- One observational unit per table & file. Multiple tables require join columns.
- Missing data coded as "`NA`".
- Censored data coded as "`NA`" with "`T`" in added "`Censored`" column.

What must a code book include?  
- Variable names/datatypes/units.
- Study design used.
- Data-collection procedures used.
- Summary choices made.
- Reasons for censored data.

What criteria must reproducible instructions meet?  
- Converts raw input to tidy output.
- Ideally, provides analysis script taking no parameters.
- Otherwise, provides separate instructions/parameters for each sample/processing stage.
- Describes where to obtain software used.
- Describes exact software and OS versions used.
