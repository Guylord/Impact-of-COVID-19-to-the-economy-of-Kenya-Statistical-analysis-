# COVID-19 Impact on Kenya's Economy - Statistical Analysis

This project investigates the economic impact of COVID-19 on Kenya by analyzing multiple datasets related to government responses, COVID-19 cases and deaths, quarterly GDP figures, unemployment rates, and additional factors. The goal is to understand the relationship between pandemic-related variables and economic performance indicators in Kenya.

## Datasets

1. **OXFORD COVID-19 Government Response Data** (`oxford-government-response.csv`)
   - **Description**: Contains records of various government interventions to manage the pandemic, such as school closures, workplace closures, stay-at-home requirements, and public transport closures. The `stringency_index` measures the overall stringency of these responses.
   - **Usage**: Filtered for Kenya, with key indicators aggregated by quarter.

2. **COVID-19 Cases and Deaths in Kenya** (`covid19_cases_and_deaths_in_kenya.csv`)
   - **Description**: Weekly records of new COVID-19 cases and deaths in Kenya.
   - **Usage**: Cleaned and aggregated to quarterly totals.

3. **Quarterly GDP (Kenya)** (`Kenya-Quarterly GDP.csv`)
   - **Description**: Provides quarterly GDP data for Kenya.
   - **Usage**: Reshaped for consistency with other datasets.

4. **Kenya Unemployment Rate** (`Kenya-Unemployment-Rate.csv`)
   - **Description**: Quarterly records of the unemployment rate in Kenya.
   - **Usage**: Cleaned and prepared for integration.

5. **Kenya Inflation Rate** (`Kenya-Inflation-Rate.csv`)
   - **Description**: Contains quarterly data on the inflation rate in Kenya.
   - **Usage**: Cleaned and merged to examine its impact on GDP.

6. **Kenya Exchange Rate** (`Kenya-Exchange-Rate.csv`)
   - **Description**: Provides quarterly exchange rate data for Kenya.
   - **Usage**: Cleaned and integrated to assess its effect on the economy.

7. **Kenya Interest Rates** (`Kenya-Interest-Rates.csv`)
   - **Description**: Quarterly records of interest rates in Kenya.
   - **Usage**: Prepared for merging to evaluate its influence on economic performance.

## Process

### 1. Import Libraries
   - **Libraries Used**: `pandas`, `numpy`, `seaborn`, `matplotlib.pyplot`
   - **Purpose**: Essential for data manipulation, cleaning, and visualization.

### 2. Load and Clean Datasets
   - **Oxford Government Response Data**:
     - Filter data for Kenya.
     - Select relevant columns and aggregate by quarter.
   - **COVID-19 Cases and Deaths**:
     - Clean and aggregate data to quarterly totals.
   - **Quarterly GDP**:
     - Reshape data to ensure consistency.
   - **Unemployment Rate**:
     - Clean and prepare data for integration.
   - **Inflation Rate**:
     - Clean and aggregate quarterly data.
   - **Exchange Rate**:
     - Clean and prepare quarterly exchange rate data.
   - **Interest Rates**:
     - Clean and prepare quarterly interest rate data.

### 3. Merge Datasets
   - **Steps**:
     - Merge the cleaned datasets (government responses, COVID-19 cases and deaths, GDP, unemployment rate, inflation rate, exchange rate, and interest rates) on the quarter.
     - Ensure all datasets are aligned to the same quarterly timeline.
   - **Outcome**: A comprehensive dataset combining government responses, health impacts, economic indicators, and other relevant variables.

### 4. Analyze Data and Build Models

- **Objective**: Determine how government interventions, COVID-19 severity, and economic indicators influenced Kenya’s GDP.

- **Models**:
  - **Linear Regression**: 
    - **Purpose**: Assessed the impact of government measures, trade balance, government expenditure, and COVID-19 severity on GDP.
    - **Key Findings**:
      - Government measures had no significant impact.
      - Stringency Index and Trade Balance negatively affected GDP.
      - Government Expenditure positively influenced GDP.

  - **Correlation Analysis**:
    - **Purpose**: Investigated relationships between COVID-19 variables, trade balance, government expenditure, and GDP.
    - **Key Insights**:
      - Strong negative correlation between Stringency Index and GDP.
      - Significant negative correlation between Trade Balance and GDP.
      - Positive correlation between Government Expenditure and GDP.

     - 
   ## OLS Regression Results

**Dependent Variable**: GDP at Market Prices

- **R-squared**: 0.914
  - Indicates that 91.4% of the variance in GDP is explained by the model.
- **Adjusted R-squared**: 0.865
  - Adjusted for the number of predictors, showing a high fit of the model.
- **F-statistic**: 18.62
  - **Prob (F-statistic)**: 0.000781
  - The model is statistically significant.

**Coefficients**:

- **Constant**: 1.931e+06 (p-value: 0.000)
  - Significantly contributes positively to GDP.
- **Fiscal Measures**: 0.0003 (p-value: 0.952)
  - Not statistically significant.
- **Stringency Index**: -2428.0053 (p-value: 0.010)
  - Significant negative impact on GDP.
- **Trade Balance**: -3.8798 (p-value: 0.001)
  - Significant negative impact on GDP.
- **Government Expenditure**: 0.0222 (p-value: 0.011)
  - Significant positive impact on GDP.


## Visualizations

- **Plots and Charts**:
  - Correlation heatmaps displaying the strength of relationships between different variables.
  - Line graphs showing trends in COVID-19 cases, deaths, unemployment, inflation, exchange rates, interest rates, and GDP.

## Conclusion

This analysis provides insights into the impact of the COVID-19 pandemic and government interventions on Kenya's economy. The findings highlight the following:

- **Government Interventions**: The Stringency Index had a significant negative impact on GDP, indicating that stricter measures were associated with economic contractions. Conversely, government expenditure had a positive effect on GDP.
- **Economic Indicators**: The Trade Balance showed a significant negative correlation with GDP, suggesting that trade imbalances adversely affected economic performance.

These results underscore the economic challenges faced during the pandemic and offer valuable guidance for future policy decisions aimed at mitigating the impact of similar crises.
