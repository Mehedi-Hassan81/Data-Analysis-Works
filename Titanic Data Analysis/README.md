# Titanic – Exploratory Data Analysis (EDA)

End-to-end EDA on the classic Titanic dataset (Kaggle: Titanic – Machine Learning from Disaster) performed in Jupyter Notebook.

## Objective
Understand passenger characteristics, handle missing data, uncover patterns in survival, and visualize key relationships before modeling.

## Dataset
- **File**: https://www.kaggle.com/datasets/muhammadyasirsaleem/website?select=titanic_data.csv
- **Rows**: 891
- **Columns**: 12
- **Target**: Survived (0 = No, 1 = Yes)

## Tech Stack
- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Steps Performed

1. **Data Loading & Inspection**
   - Shape, info, describe, head/tail

2. **Data Cleaning**
   - Age: imputed missing values with median (~28–29 years)
   - Embarked: imputed 2 missing with mode ('S')
   - Cabin: dropped (77% missing)

3. **Univariate Analysis**
   - Distributions of Age, Fare, SibSp, Parch (histograms + box plots)
   - Categorical counts: Sex, Pclass, Embarked

4. **Bivariate & Multivariate Analysis**
   - Survival rate by Sex → females: 74.2%, males: 18.9%
   - Survival rate by Pclass → 1st: 63%, 2nd: 47%, 3rd: 24%
   - Survival by Embarked (Cherbourg highest)
   - Correlation heatmap (numerical features)

5. **Key Findings**
   - Strongest predictors: Sex and Pclass
   - Fare strongly correlates with class and survival
   - Majority traveled alone (SibSp = 0, Parch = 0)
   - Age shows weak negative correlation with survival

## Notebook Structure
- 01 – Data Loading & Cleaning
- 02 – Univariate Distributions
- 03 – Survival Analysis (Gender, Class, Port)
- 04 – Correlations & Visual Summary
- 05 - Survival Rate Visualizer with barplots and histograms(for future)

## How to Run
```bash
git clone https://github.com/[yourusername]/titanic-eda.git
cd titanic-eda
jupyter notebook "Titanic_EDA.ipynb"
