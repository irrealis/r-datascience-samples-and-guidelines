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



What characterizes the processed data of an analysis?

- Named so it's easy to see which script generated which processed data.
    - The script -> data mapping is described in README.
- Follows tidy rules:
    - One table per file.
    - One variable per column.
    - One observation per row.
    - Related tables associated via join columns.
    - Missing data coded with `NA`.
    - Censored data coded with `NA`, and also with `T` in added `censored` column.
    - Described in accompanying codebook.



What characterizes the exploratory figures of an analysis?

- Any relevant figures generated during exploration.
- Quick, rough, unpolished.
- Useful enough that you know what's going on.
- Often not used in final report.
- Reproducible.



What characterizes the final figures of an analysis?

- Polished, organized,  readable.
    - Careful axes, colors, annotations used to make figure clear.
- Possibly multiple panels.
- Usually small subset of original figures.
    - Typically 4-5 max are used in published papers.
        - They take lots of space.
        - Don't want to inundate people -- they'll get lost.
- Reproducible.



What characterizes the rough code of an analysis?

- Maybe less well-commented.
    - The more comments, the better...
- Maybe multiple versions.
- Maybe includes discarded analyses, dead ends, etc.



What characterizes the final code of an analysis?

- Clearly commented:
    - Small comments liberally: what, when, why, how.
    - Block comments for whole sections.
- Includes processing details.
- Only for analyses used in final writeup.



What characterizes markup files?

- Used to generate reports.
- Can be used in literate style for reproducibility.



What characterizes README files?

- Contains step-by-step instructions to reproduce analysis.
    - Not needed if literate style is used to generate analysis.
- Cites data sources.
- For webmined data, also gives access date, URL, and description.



What characterizes writeups?

- Includes:
    - Title
    - Introduction (motivation)
    - Methods
    - Results (including measures of uncertainty)
    - Conclusions (including potential problems)
- Tells a story.
- _Does not include every analysis performed._
- References included for statistical methods.
    - Including software/implementation details.
