# R Data-Science Samples and Guidelines
## 03 Getting and Cleaning Data
### 01 Components of Tidy Data
#### Questions and Answers:

What are the components of reproducible data?
- Original, *raw data*.
- Processed, *tidy data*.
- *Code book* describing tidy data.
- *Reproducible instructions* for processing raw to tidy.

What criteria must raw data meet?
- You ran no software on the raw data.
- You did not manipulate any of the raw data.
- You did not remove any of the raw data.
- You did not add anything to the raw data (in particular, no summary).

What criteria must tidy data meet?
- Each variable has descriptive name and forms a column.
- Each observation forms a row.
- Each type of observational unit forms a table and file.
- Multiple tables have join columns.
- Handling of missing/censored data:
  - Missing/censored data is coded as "`NA`".
  - Censored data is coded as "`T`" in added "`Censored`" column.

What must a code book include?
- Variable names, data types, units.
- Info about study design and data-collection procedures used.
- Info about summary choices made.
- Reason for any censored data.

What criteria must reproducible instructions meet?
- Raw input, tidy output.
- Ideally, provides analysis script taking no parameters.
- Otherwise, provides specific instructions including:
  - Separate instructions and exact parameters for each sample and processing stage:
  - Where to obtain software.
  - Exact software and OS versions used.

