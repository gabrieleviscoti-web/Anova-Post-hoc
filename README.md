# Anova post-hoc
This project applies one-way ANOVA (Analysis of Variance) to evaluate whether the variable petal_length differs significantly across the three Iris species: Setosa, Versicolor, and Virginica.
The analysis is designed to demonstrate skills in inferential statistics, assumption checking, data analysis, visualization, and interpretation of statistical results.
It serves as a complete, reproducible example suitable for a STEM portfolio, especially for roles in Data Analysis, Data Science, and Biomedical Engineering.

## Project Objective
Determine whether the mean petal length differs significantly across the three Iris species and identify which specific pairs of species show statistically significant differences using post-hoc Tukey HSD.

## Dataset
The Iris dataset contains 150 samples, 4 numerical features, and 3 species.
It is loaded directly from the seaborn library:

```python
import pandas as pd
import seaborn as sns

df = sns.load_dataset("iris")
``` 
## Analysis Pipeline
1. **Exploratory Data Analysis**<br>
- Descriptive statistics

- Distribution plots (histogram + KDE)

- Boxplots for group comparison

- Initial inspection of species differences

2. **Assumption Testing**<br>
Before running ANOVA, the following assumptions are checked:

    - Normality using Shapiro–Wilk test

    - Homogeneity of variances using Levene’s test

    If assumptions are violated, Welch ANOVA is used as a robust alternative.

3. **One-way ANOVA**<br>
A one-way ANOVA is performed to test whether the mean petal length differs across the three species.
The test evaluates the null hypothesis:

    H₀: The mean petal length is equal across all species.

4. **Post-hoc Analysis (Tukey HSD)** <br>
Since ANOVA indicates a significant difference, Tukey HSD is applied to determine which specific pairs of species differ.
This step provides pairwise comparisons and adjusted p-values.

5. **Visualization** <br>
The analysis includes several plots to support interpretation:

    - Histogram and KDE to visualize distribution differences

    - Boxplot to compare medians and variability

    - Tukey HSD summary plot to show pairwise differences

    - These visualizations help confirm statistical findings and highlight separation between species.

6. **Interpretation of Results** <br>
The results are interpreted in a scientific and rigorous way, explaining:

    - Which species differ

    - How large the differences are

    - Whether assumptions were met

    - How the statistical evidence supports the conclusions

## Key Results
- Petal length differs significantly across all three species.

- Tukey HSD confirms that all pairwise comparisons are statistically significant.

- Clear separation in distributions: <br>
    Virginica > Versicolor > Setosa

- All p-values < 0.001.

- Visualizations strongly support the statistical conclusions.

## Technologies Used
- Python

- Pandas

- NumPy

- SciPy

- Pingouin

- Matplotlib

- Seaborn

## Purpose of This Project 
This project demonstrates:

   - Correct application of inferential statistics

   - Proper assumption checking

   - Ability to run and interpret ANOVA

   - Understanding of post-hoc tests

   - Competence with the Python scientific stack

   - Ability to communicate statistical results clearly

   - Reproducible workflow suitable for real-world data analysis


## Possible Extensions

- MANOVA

- Effect size calculations

- Confidence intervals

- Additional variables from the Iris dataset

- Full PDF statistical report


