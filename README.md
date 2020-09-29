# baltimore-city-employment-rate-2015
## Background
Explored how accurately Baltimore City's employment rate can be predicted by variables: job density, job growth, poverty rate, median HH income, and commute time. Interested in this problem because Baltimore City is experiencing similar but worse employment trends over the past few years. If Baltimore is to address this issue, it's important to understand some of the possible predictors.    
![alt text](https://github.com/matthewprk/baltimore-city-employment-rate-2015/blob/master/BEA_Balt_vs_US_employment.png)
Access and/or economic conditions were the variable categories I focused on and they can be addressed to improve Baltimore's employment rate. For example, neighborhoods in poverty receive [1.5x less investment than the average neighborhood in Baltimore](https://www.baltimoresun.com/opinion/editorial/bs-ed-0207-baltimore-poverty-20190205-story.html). If there's a significant relationship between poverty and employment rates, then policies like this need to be reconsidered. 
## Business Question
How can Baltimore City's predict and increase its employment rate by examing factors such as job desnity, job growth, poverty rate, median HH income, and commute time?
## Data Sources
- [Opportunity Atlas](https://www.opportunityatlas.org/) - Baltimore-City tract data for outcome + independent variables
  - [Annualized Job Growth](https://github.com/matthewprk/baltimore-city-employment-rate-2015/blob/master/shown_tract_ann_avg_job_growth_2004_2013.xls)
  - [Job Density](https://github.com/matthewprk/baltimore-city-employment-rate-2015/blob/master/shown_tract_job_density_2013.xls)
  - [Household Median Income](https://github.com/matthewprk/baltimore-city-employment-rate-2015/blob/master/shown_tract_kfr_rP_gP_pall.xls)
  - [Poverty Rates](https://github.com/matthewprk/baltimore-city-employment-rate-2015/blob/master/shown_tract_poor_share2016.xls)
  - [Commute Time <15min](https://github.com/matthewprk/baltimore-city-employment-rate-2015/blob/master/shown_tract_traveltime15_2016.xls)
  - [Employment Rates](https://github.com/matthewprk/baltimore-city-employment-rate-2015/blob/master/baltimore_working_rP_gP_pall.xls)
## Data Analysis
The data questions that the analysis will answer:
- Initial regression table shows that job density and job growth do not explain employment rate (p>0.05)
![alt text](https://github.com/matthewprk/baltimore-city-employment-rate-2015/commit/ae82633f7204e4845eb398dc863d423f6100d682)
- Revised regression table shows that commute time <15min, poverty rate, and median HH income can be predictors of employment rate (p<0.05)
  - The equation used to predict employment rate is: Employment Rate = - 0.1278(traveltime15_2016) - 0.0680(poverty rate) + 2.0810E-06(median HH Income) + 0.6897
![alt text](https://github.com/matthewprk/baltimore-city-employment-rate-2015/blob/master/baltimore_working_rP_gP_pall.xls)
- Linear Regession for Employment Rate and Poverty Rate Visualization
  - Rsquared = 0.2294 -> less than a quarter of the observed relationship is explained by poverty rate
  - Slope = -0.1913 -> for every 1 unit increase in poverty rate, employment rate decreases by -0.1913
![alt text](https://github.com/matthewprk/baltimore-city-employment-rate-2015/blob/master/linreg_povertyrate.png)

## Summary and Next Steps
