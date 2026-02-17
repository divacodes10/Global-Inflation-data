# Global-Inflation-data
Project Title

Global Inflation Analysis (1984–2024) | Python EDA & Panel Data Transformation

- Project Overview

This project analyzes global inflation data from 1984 to 2024 across multiple countries. The dataset was originally structured in a wide format (years as separate columns), which was transformed into a panel (long) format for effective exploratory data analysis and visualization.

The objective was to examine global inflation trends, identify distributional patterns, detect hyperinflation episodes, and understand cross-country macroeconomic instability.

- Objectives

Restructure wide-format macroeconomic data into panel format

Analyze overall inflation distribution across countries and time

Identify extreme inflation (hyperinflation) episodes

Examine skewness and outlier behavior in global inflation data

Generate visual insights using Python visualization libraries

 Dataset Structure
Original Format (Wide)

| Country | Indicator | 1984 | 1985 | ... | 2024 |

Each year was stored as a separate column, making time-series analysis difficult.

Transformed Format (Long / Panel Data)

| Country | Indicator | Year | Inflation Rate |

This transformation enabled:

Time-series analysis

Cross-country comparison

Distribution analysis

Panel data modeling

🔧 Tools & Libraries Used

Python

Pandas (data cleaning & reshaping)

NumPy

Matplotlib

Seaborn

- Data Transformation

The dataset was reshaped using pandas.melt() to convert year columns into a single time variable.

df_long = df.melt(
    id_vars=["Country Name", "Indicator Name"],
    var_name="Year",
    value_name="Inflation Rate"
)


This created a proper panel structure:

𝐼
𝑛
𝑓
𝑙
𝑎
𝑡
𝑖
𝑜
𝑛
𝑖
,
𝑡
Inflation
i,t
	​


Where:

𝑖
i = Country

𝑡
t = Year
--> Exploratory Data Analysis (EDA)
1. Overall Inflation Distribution

A histogram was plotted to examine the global inflation distribution (1984–2024).

Key Finding:

The distribution is highly right-skewed due to extreme hyperinflation episodes in certain economies.

Most observations lie within 0–20%, but a small number of extreme cases stretch the distribution significantly.

2️. Hyperinflation Detection

Extreme inflation values (above 1,000% and even 10,000%) were identified, indicating historical macroeconomic crises.

These extreme values caused compression of normal inflation ranges in the visualization, highlighting the importance of:

Outlier analysis

Log-scale visualization

Data filtering for focused interpretation

 Key Insights

Global inflation exhibits strong positive skewness.

Most countries maintain moderate inflation levels.

A few economies experienced extreme hyperinflation episodes.

Panel data restructuring significantly improves analytical flexibility.

 Visualization Adjustments

Due to extreme outliers, visualization techniques such as:

X-axis limiting

Outlier filtering

Log-scale transformation

were applied to improve interpretability.

 Economic Interpretation

The presence of hyperinflation reflects:

Currency collapses

Political instability

War and crisis periods

Structural macroeconomic imbalances

This dataset provides insight into global macroeconomic volatility over four decades.

 Future Scope

Country-wise volatility ranking

Time-series trend analysis

Crisis-period comparison (Pre/Post 2008)

Panel regression modeling

Inflation forecasting using ARIMA
