# The Impact of  Childhood Environment on Employment Outcomes

## Background: Gender Gap Hypothesis
* Motivation of this analysis comes from Childhood Environment and Gender Gaps in Adulthood (2016) by Chetty, Hendren et al 
* Gender employment gap reversed for children in poor families, boys in poor families have lower employment than girls 
* Adverse outcomes largest for boys in poor single parent families 
* Low income boys in high poverty & high minority areas work less than girls possibly because areas have higher crime rates, suggests that boys in concentrated poverty substitute from employment to crime
* Data is analyzed by Commuting zones (agglomerations of counties that approximate local labor markets)
* We assume that hypothesis that gender gap is reversed for poor single parent families is true and narrow our focus for employment outcome for boys 

## Dataset & Objectives
* Dataset derived from database of tax returns from 1996-2021 
* Interested in Employment rates, by commuting zone (CZ) at age 30 for boys whose parents are "permanent residents" 
* Outcome Variable is Earnings Q1: Whether boy reports positive W2 earnings or they or their spouse reports positive self employment income given that this boy belonged to the bottom quintile of income distribution growing up  
* Independent Variables of Interest: Fraction of Black individuals, Racial Segregation in CZ
* Interested in the impact of Racial Segregation on Employment Outcomes of African American Males 

## Data Preprocessing & Initial Analysis
* Data loaded, variables of interest selected
* Variables with too many NA values dropped (College Graduation Rate, Tuition, High School Dropout Rate, College Per Capita), all remaining NAs dropped
* Mean Proportion of Individuals reporting positive earnings calculated
* 78.29% in the bottom quantile reported positive earnings while 84.25% for 2nd, 88.43% for 3rd and 90.6% for the fourth, and 90.94% for 5th

![This is a alt text.](/Images/Mean_Earnings.PNG)

## Data Exploration

### Scatterplots 

![This is a alt text.](/Images/reg_line_EarningsQ1_Segregation.png)

* Earnings by Segregation in CZ clearly show that as Segregation reduces, employment outcomes improve for Bottom Quantile, 
* Sharp, downward sloping Regression Line

![This is a alt text.](/Images/reg_line_EarningsQ1_Black.png)

* Earnings by Fraction of African Americans in CZ clearly shows that as proportion of African Americans in CZ increase earnings decrease, 
* Sharp steady decrease, clearly shows income disparities and inequality due to Racial Wealth Gap 

### Heatmap 

![This is a alt text.](/Images/Heatmap.png)

### Analysis 

![This is a alt text.](/Images/Pearson_Segregation.PNG)
![This is a alt text.](/Images/Pearson_ProportionAA.PNG)

* Scatterplots show clear correlation between Employment outcomes (Earnings Q1) by Racial Segregation and Proportion of African Americans in a CZ
* Further verified with Pearson Correlation, which show statistically significant strong negative correlations in both cases  (African Americans: -0.575, Segregation: -0.415)  
* Heatmap shows a strong relationship between outcome variable and variable of interest with Violent Crime, Proportion of Single Mothers, African Americans, Racial Segregation and Social Capital Index showing strong correlation with absolute values greater than 0.4 for Earnings Q1

## Regression Analysis & Outcome 

![This is a alt text.](/Images/Regression_Results.PNG)

* We conduct a regression of Employment outcomes on Racial Segregation and Proportion of African Americans with 6 covariates, low R-Squared of 0.541
* Except for Violent Crime and Married Parents, all variables are statistically significant
* All other factors remaining constant, a unit increase in racial segregation leads to on average a 1.3% decrease in Employment outcomes for boys 
* Single Mothers, Proportion of African Americans and Social Capital Index play important role in Employment Outcomes

### Further Analysis Recommendations 

Due to the time constraints we could only recognize few patterns, we can explore this data further by: 

* Exploring relationship amongst covariates to address multicollinearity 
* Conducting geospatial analysis of data to better understand the regional disparities in employment outcomes and find which areas are more vulnerable 
* Finding other relevant variables that might increase R-Squared
* Exploring other statistical methods such as Weighted Least Squares or Robust Estimates
* Exploring the data further and ensure removal of any outliers that might skew the model
* Exploring county level and national level data to further understand demographic trends

## Conclusions 
* Overwhelming evidence shows that racial wealth and income disparities, and lack of social and parental support may be a large reason behind poor employment outcomes in for boys in bottom quintile of income distribution growing up 
* Heatmap showed that the correlation between Social Capital Index and Proportion of African Americans was a staggering -0.49, further indicating racial disparities and lack of infrastructure and support in these communities 
* The statistical insignificance of violent crime variables in our regression indicates that majority of this variable can be accounted for by other variables such as proportion of single mothers, indicating that low income families with lack of parental support could be the primary reason employment outcomes are low in these areas, as boys turn towards crime as an alternative to formal employment 

### Tools and Resources
Python software was utilized for the analysis in this presentation. The relevant libraries used were:
* Data Preprocessing and Analysis: Numpy, Pandas
* Data Visualization: Seaborn
* Statistical Analysis: Scipy, Statsmodels

* Resources utilized for this analysis:
https://opportunityinsights.org/paper/gendergaps/


