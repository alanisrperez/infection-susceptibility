# Project 4: Infection Susceptibility
Team Members, Group 5: Eduardo Almonte, Mark Bishoff, Alanis Perez, Nishi Thapliyal

Project Overview
-------------------------
This project aims to predict infectious disease vulnerability across U.S. counties, focusing on COVID-19 as a case study. We seek to identify which counties are most susceptible to disease outbreaks and understand the environmental, demographic, and healthcare factors contributing to this risk. Our analysis could inform public health interventions by highlighting vulnerable areas and identifying potential factors that elevate susceptibility.


Project Questions
-------------------------
Which U.S. counties are the most susceptible to infectious disease outbreaks?
* What environmental, demographic, & healthcare factors contribute to their vulnerability?


Sources & Data Wrangling
-------------------------
* Environmental Factors: Climate data (average, minimum, and maximum temperatures by county) from the National Center for Environmental Data (NCEI)
* Demographic Factors: Population density (per 100k) and age data from U.S. Census (2020-2023) (Census)
* Healthcare Factors: COVID-19 vaccination and death rates (per 100k) from U.S. Department of Health & Human Services (Vaccination rates, Death rates)


Analysis
-------------------------
Our analysis attempted two approaches:
* Classification: Categorizing counties into low, medium, and high susceptibility levels.
* Regression: Estimating a numerical susceptibility score for each county.
Data cleaning, feature selection, and aggregation were performed using Python in Jupyter Notebook. The cleaned dataset was then transferred to Google Colab for machine learning analysis. For visualization, we used Tableau to map geographic data and examine the correlation between temperature and COVID-19 death rates, using geographic fields for state and county. We built color-coded maps to visualize mortality rates, highlighting regions with higher death counts. We then layered temperature data as a contextual factor to explore potential correlations between warmer climates and increased COVID-19 deaths, providing a visual basis for deeper analysis. The models applied include Decision Tree Regression, Random Forest, Neural Networks, Linear Regression, and K-Means Clustering. We explored the relationship between COVID-19 death counts (target variable) and features including average temperature, vaccination count, and population density. After scaling and splitting the data into training and testing sets, we applied multiple machine learning models to identify patterns and assess susceptibility to COVID-19. 

Results
-------------------------
Machine Learning models - high Mean Squared Errors and low R² scores indicate weak predictive power across models:
* Decision Tree Regression: MSE = 1,778,541, R² = -0.2168
* Random Forest: MSE = 984,501, R² = 0.1005
* Neural Networks: MSE = 14,029,814
* Linear Regression: MSE = 1,242,681, R² = 0.0009
K-Means clustering provided limited insights:
* Lower vaccination rates showed some correlation with higher death rate variability
* Smaller populations displayed a tendency for higher death rates
* No consistent relationship was observed between average temperature and COVID-19 death rates, although moderate to warm temperatures were weakly associated with higher death rates
Tableau visualizations
* Western states show fewer counties with high death counts, which can reflect lower population density relative to other regions
* Higher death counts are seen on the West and Southeast, but there is a broader spread of death counts across Midwest & Northeast
* Warmer regions (in South & Southeast) show higher death rates
Overall, these weak results suggest that additional factors and refined models may be necessary to improve predictive accuracy. Over or underfitting as well as noise in the data may explain poor performance.


Future Considerations
-------------------------
To enhance the predictive power of models and gain a deeper understanding of disease vulnerability, future research could include the following factors:
Environmental Factors
* Flight Paths and Traffic Flow: High traffic flow or proximity to major flight paths may give an insight on environmental impact (for example, the air quality and pollution levels of a given region)
* Seasonal Patterns: Other seasonal variables, like humidity and precipitation, and seasonal changes could provide valuable insight into how climate influences illness susceptibility trends across regions and time
Demographic Factors
* Gender and Race/Ethnicity: Future research could benefit from analyzing gender and race/ethnicity, as these groups may experience different health outcomes, healthcare access, and predispositions to health concerns
* Socioeconomic Factors: Including data on poverty rates and household income would provide a more nuanced understanding of how socioeconomic disparities play a role in both the spread of infection and recovery rates
Healthcare Factors
* Vaccination Rates and Access: Further exploration into regional vaccination rates, access, and hesitancy could yield more accurate insights. As well as assessing disparities in vaccination access by geographic or socioeconomic status
* Healthcare Infrastructure: Healthcare infrastructure, such as hospital capacity, ICU availability, and access to primary care may show us how infection susceptibility interacts with mortality and recovery rates
* Pre-existing Conditions and Holistic Medicine Use: Understanding how pre-existing conditions and varying healthcare practices, such as the use of holistic or alternative medicine, would deepen the analysis

Conclusion
-------------------------
Our machine learning models—Decision Tree Regression, Random Forest, Neural Networks, and Linear Regression—demonstrated limited success in predicting COVID-19 death rates per 100k across U.S. counties. K-means clustering suggested weak trends, such as an association between lower vaccination counts and higher death rates and a pattern of smaller population sizes correlating with higher death rates. Moderate to warm temperatures were loosely associated with increased death rates. Future studies could improve these models by incorporating additional, relevant factors that capture more of the complexity underlying disease susceptibility.
