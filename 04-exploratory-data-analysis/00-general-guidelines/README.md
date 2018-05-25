# R Data-Science Samples and Guidelines
## 04 Exploratory Data Analysis
### 00 General Guidelines for Exploratory Data Analysis
#### Questions and Answers:

Broadly, what are the main steps in exploratory data analysis? 
1. Formulate questions to ask of the data.
2. Explore individual dimensions using histograms and smooth densities. Look for subsets with different distributions, and separate their histograms/densitiies using colors or facets.
3. Explore relationships between dimensions using scatterplots and smooth extrapolations (generally linear regressions). Look for subsets with different relationships, and separate their scatterplots/extrapolations/regressions using colors or facets.


What are the characteristics of good questions to ask of the data? 
**To Do**


What are some things to watch for when exploring individual dimensions? 
Do the histograms and densities make sense? If not, good place to explore!
- Are the histograms/densities bell-shaped? poisson-shaped?
- Are the histograms/densities multimodal? with different means/medians/variances? or totally different distributions?
- Brainstorm potential reasons.
- Look for subsets with different distributions, and separate their histograms using colors or facets.
  - Guided by brainstorms and intuitions about potential subsets having different distributions.
  - If can't separate by category, try creating categories.
- Explore relationships using scatterplots and smooth extrapolations (generally linear regressions).
  - Guided by brainstorms and intuitions about potential relationships.
  - Do the relationships make sense? If not, good place to explore!
    - E.g., linear? log-linear? polynomial?
    - E.g., unexpected slopes?
    - Brainstorm potential reasons.
- Look for subsets with different relationships, and separate their scatterplots, extrapolations, and regressions using colors or facets.
  - Guided by intuitions about potential subsets having different relationships.
  - If can't separate by category, try creating categories.

