# Anova post-hoc

This project applies one-way ANOVA (Analysis of Variance) to evaluate whether the variable petal_length differs significantly across the three Iris species: Setosa, Versicolor, and Virginica. The goal is to demonstrate skills in inferential statistics, assumption checking, data analysis, visualization, and interpretation of statistical results.

## Project Objective
Determine whether the mean petal length is significantly different across the three species in the Iris dataset.

## Dataset
The Iris dataset contains 150 samples, 4 numerical features, and 3 species. It is loaded directly from the seaborn library:

```python
import pandas as pd
import seaborn as sns

df = sns.load_dataset("iris")
```
## Analysis pipeline
Exploratory data analysis (descriptive statistics, distribution plots, boxplots).

Assumption checks:

1. Shapiro–Wilk test for normality.

2. Levene’s test for homogeneity of variances.

3. One-way ANOVA using scipy.stats and pingouin.

4. Tukey HSD post-hoc test to identify which species differ from each other.

5. Visualization using seaborn and matplotlib.

## Key results

- ANOVA returned a p-value < 0.001, indicating significant differences in petal length across species.

- Tukey HSD confirmed that all species pairs differ significantly.

- Virginica shows the highest mean petal length, Setosa the lowest.






