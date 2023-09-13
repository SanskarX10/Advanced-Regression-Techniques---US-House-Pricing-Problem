# Advanced-Regression-Techniques---US-House-Pricing-Problem
Identifying and Solving US House Pricing Problem

##### <span style="color: blue;">**The housing market in the United States has long been a subject of interest and concern for various stakeholders, including homeowners, real estate professionals, economists, and policymakers**</span>

##### <span style="color: blue;">**This case study aims to explore the multifaceted landscape of factors that affect housing prices in the United States. By delving into a comprehensive analysis of these factors, we can gain valuable insights into the dynamics of the housing market, helping both individuals and organizations make more informed decisions.**</span>

### Data Collection

##### Below are the factors that i chose for creation of the Model

1. **GDP Index**
   - Source: [S&P Global](https://www.spglobal.com/marketintelligence/en/mi/products/us-monthly-gdp-index.html)
   - Description: The GDP Index is used as a proxy for the economic health of the United States, which can impact housing prices.

2. **Income**
   - Source: [St. Louis Fed](https://fred.stlouisfed.org/series/PI)
   - Description: Total income earned by all individuals in the United States, indicating the overall financial capacity of potential homebuyers.

3. **Monthly Supply of New Houses**
   - Source: [St. Louis Fed](https://fred.stlouisfed.org/series/MSACSR)
   - Description: Represents the ratio of houses sold to the total number of houses available for sale each month, indicating the demand and supply dynamics of the housing market.

4. **Unemployment**
   - Source: [St. Louis Fed](https://fred.stlouisfed.org/series/UNRATE)
   - Description: The unemployment rate, indicating the percentage of the labor force without jobs, can impact housing demand and affordability.

5. **Population**
   - Source: [St. Louis Fed](https://fred.stlouisfed.org/series/POPTHM)
   - Description: Monthly estimates of the total population in the United States, influencing the demand for housing.

6. **New Privately-Owned Housing Units Under Construction**
   - Source: [St. Louis Fed](https://fred.stlouisfed.org/series/UNDCONTSA)
   - Description: Data on the number of new housing units authorized and under construction, reflecting the pace of new housing supply.

7. **Mortgage Rates**
   - Source: [Freddie Mac](https://www.freddiemac.com/pmms)
   - Description: The average 30-Year Fixed Rate Mortgage in the United States, affecting the affordability and financing options for potential homebuyers.



## Results


<font color="#006400"><h2>Most Important Factors:</h2></font>

| Variable                                     | Normalized Correlation | Pearson Correlation | Explanation                                        |
|----------------------------------------------|-------------------------|---------------------|----------------------------------------------------|
| Income                                       | 0.8                     | 0.75                | Strong positive correlation with housing prices.   |
| GDP Index                                    | 0.8                    | 0.75                | Strong positive correlation with housing prices.   |
| New Privately-Owned Housing Units Under Construction | 0.6            | 0.64                | Moderate positive correlation with housing prices. |
| Population                                   | 0.6                    | 0.63                | Moderate positive correlation with housing prices. |


<font color="#006400"><h2>Less Important Factors:</h2></font>

| Variable        | Normalized Correlation | Pearson Correlation | Explanation                                        |
|-----------------|-------------------------|---------------------|----------------------------------------------------|
| Unemployment    | -0.5                    | 0.51                | Moderate negative correlation with housing prices. |
| Mortgage        | -0.3                    | 0.3                 | Weak negative correlation with housing prices.     |
| ForSale_Sold    | -0.1                    | 0.084                | Very weak negative correlation with housing prices.|

<font color="#006400"><h2>Top Performing Models:</h2></font>

| Model Name                | Train RMSE | Test RMSE | Test Std | Time     |
|---------------------------|------------|-----------|----------|----------|
| Elasticnet                | 0.028412   | 0.046087  | 0.029836 | 0.111171 |
| Lasso                     | 0.028398   | 0.046754  | 0.030323 | 0.028566 |
| GradientBoostingRegressor | 0.005390   | 0.048369  | 0.055786 | 5.621939 |
| XGBRegressor              | 0.000692   | 0.050595  | 0.055145 | 0.869652 |
