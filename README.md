# IT Job Salaries Analysis

This project explores the factors influencing IT job salaries across Europe, using data from an anonymous 2019 survey. The original dataset included 999 records and 23 features. After cleaning and selecting relevant variables, the analysis focused on 837 records and 8 key features: Age, Gender, Seniority, Years of Experience, Main Programming Language, Company Size, Company Type, and Salary.

### Objectives

- Analyze how salary varies with Age, Seniority, and Experience.
- Assess the impact of Gender and other variables on salary prediction.
- Identify the most important quantitative and categorical predictors for salary.

### Data Preparation

- Removed columns with excessive missing values and dropped incomplete rows.
- Selected and renamed relevant variables for clarity.
- Encoded categorical variables for statistical modeling.

### Exploratory Analysis

- **Quantitative Variables:** Both Age and Experience are positively correlated with Salary, with Experience being the stronger predictor. Age and Experience themselves are also highly correlated.
- **Categorical Variables:** The dataset is predominantly male (85%), with limited female representation in higher seniority roles.
- **Gender Insights:** Males generally earn higher salaries, especially in the 30–40 age range. However, the gender imbalance limits deeper analysis.

### Modeling Approaches

- **Linear Models:** Explored relationships between Salary (log-transformed) and predictors like Age, Experience, Seniority, and Gender. Linear models were limited by non-linear trends and outliers.
- **LOESS:** Used to visualize non-linear relationships between Salary and quantitative predictors, revealing that salary increases with experience and age, but not strictly linearly.
- **Generalized Additive Models (GAM):** Provided the best fit, allowing for non-linear effects and inclusion of categorical variables. The optimal GAM included Age, Experience, Seniority, and their interaction, explaining about 31.5% of salary variance.

### Key Findings

- **Best Predictors:** Years of Experience (quantitative) and Seniority (categorical) are the strongest predictors of salary. Their interaction further improves model performance.
- **Gender Effect:** While initial plots suggested a gender pay gap, adding Gender to the model did not improve predictive power, likely due to the dataset’s gender imbalance.
- **Salary Trends:** Predicted salaries increase with both experience and seniority, but plateau or decline for some roles after 25+ years of experience, possibly due to career stagnation or retirement.

### Limitations

- Significant gender imbalance limits conclusions about gender effects.
- Outliers and limited data for some seniority levels affect model accuracy.
- The analysis is cross-sectional and does not account for changes over time.

### Conclusion

Seniority, years of experience, and age are the primary drivers of IT salaries in this European dataset. The best predictive model is a GAM incorporating these variables and their interactions. Gender, while visually associated with salary differences, was not a significant predictor in the final model due to data imbalance. Future work should use more balanced and longitudinal data to refine these insights.