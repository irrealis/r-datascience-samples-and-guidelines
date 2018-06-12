# R Data-Science Samples and Guidelines
## 05 Reproducible Research
### 04 Organizing Your Analysis
#### Questions and Answers:


'Overview'
How are data analyses typically organized?

```
analysis/
├── code
│   ├── final/
│   │   ├── analysis/
│   │   └── processing/
│   ├── markup/
│   └── rough/
├── data
│   ├── processed/
│   └── raw/
├── figures/
│   ├── exploratory/
│   └── final/
└── text
    ├── READMEs/
    └── writeups/
```



What characterizes the raw data of an analysis?

- In the README:
    - The source is cited and described.
    - Any upstream preprocessing is described.
    - When mined from the Web, the following are provided:
        - The URL used to access the raw data.
        - The date the data was accessed.
- Following the tidy-data rule, it has not been altered since obtained.
