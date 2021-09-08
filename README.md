#The Impact of  Childhood Environment on Employment Outcomes

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


