# Inference and Prediction of PM2.5 Exposure on Youth’s Mobility Outcomes

## Overview
This project investigates the relationship between air quality (measured through PM2.5 levels) and socioeconomic mobility across California counties. By combining environmental and economic datasets, we aim to understand how exposure to poor air quality during childhood influences long-term economic outcomes. Our analysis employs causal inference and predictive modeling techniques to assess and quantify these relationships.

## Project Structure
- **Data Sources**:
  - PM2.5 Air Quality Data (2001-2014): Sourced from the Centers for Disease Control and Prevention (CDC).
  - Socioeconomic Data: Obtained from the Opportunity Atlas, featuring county-level trends in economic mobility, parental income, and demographic covariates.
  - Additional Context: Variables include poverty rates, per capita income, foreign population percentage, and educational attainment levels.
  
- **Research Questions**:
  1. Is there a causal relationship between air quality at the county level and the socioeconomic mobility of residents?
  2. Can air quality data predict future income mobility outcomes for county residents?

- **Key Methods**:
  - **Causal Inference**: Propensity Score Weighting and Outcome Regression to measure the impact of PM2.5 levels on income mobility.
  - **Predictive Modeling**: Generalized Linear Models (GLMs) and Random Forests to predict income ranks based on PM2.5 exposure.

## Key Findings
1. **Causal Inference**:
   - A weak negative causal relationship exists between poor air quality and upward mobility, with Average Treatment Effects (ATE) ranging from -0.11 to -0.19 across income groups.
   - Outcome Regression was inconclusive due to the lack of linearity between air quality and socioeconomic outcomes.

2. **Predictive Modeling**:
   - Air quality can predict income mobility outcomes, with Random Forests achieving better performance (RMSE ~0.02) than GLMs.
   - The predictive power is weaker for high-income groups compared to low-income groups.

3. **Insights**:
   - Poor air quality correlates with wider wealth gaps and reduced variability in income ranks.
   - Unaccounted confounders like incarceration rates and systemic inequalities likely influence outcomes.

## Limitations
- **Data Granularity**: Aggregated county-level data may obscure intra-county disparities and neighborhood-level variations.
- **Confounders**: Limited variables in the dataset make it difficult to account for all potential confounders (e.g., housing quality, crime rates).
- **Single Outcome Variable**: Mobility is measured only by income rank; future analyses could include indicators like education or health outcomes.

## Future Directions
1. Collect more granular data at the ZIP code or neighborhood level.
2. Incorporate additional confounders such as crime rates, incarceration rates, and housing quality.
3. Expand analyses to include multiple generations and socioeconomic indicators.
4. Implement advanced causal inference methods to account for non-linear relationships.

## Technical Requirements
- **Dependencies**:
  - `pandas`, `numpy`, `scikit-learn`, `statsmodels`, `matplotlib`
- **How to Run**:
  1. Clone the repository.
  2. Download the required datasets and notebook into the `Final Code\` folder.
  3. Run all cells in the notebook sequentially

## Recommendations
- Advocate for policies targeting high-risk counties with poor air quality.
- Address systemic inequities (e.g., poverty, incarceration rates) that amplify the effects of poor environmental conditions on mobility.
- Educate communities about the long-term economic and health benefits of cleaner air.

## Authors
Lan Dinh, Faith Dennis, Huy Dao, Anand Shankar  
University of California, Berkeley

## References
- Centers for Disease Control and Prevention (CDC). "Daily County Level PM2.5 Concentrations, 2001-2014."
- Opportunity Insights. "The Opportunity Atlas."
- Kingsbury Lee, Sophie-An, et al. "Childhood PM2.5 Exposure and Upward Mobility in the United States." *PNAS*, 2024.
- O’Brien, Rourke L., et al. "Prenatal Exposure to Air Pollution and Intergenerational Economic Mobility." *Social Science & Medicine*, 2018.
