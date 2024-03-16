# chicago_socioeconomic_status

# Dataset 

The dataset sourced from the City of Chicago Data Portal was collected by the US Census Bureau spanning the year 2008-2012. The datasets reports six socioeconomic factors for 77 Chicago Community Area: 
*Percent of Crowded Housing (with more than one person per room) 
*Percent of Households Below Poverty Level
*Percent over 25+ without a High School Diploma
*Percent Aged Over 18 or Under 64
*Per Capita Income 
*Hardship Index (not clearly defined in the remaining documentation and excluded from the analysis) 

*Note: It is a limitation that the dataset only reflects 2008-2012. This project can be used for historical insight, but it is limited in its application compared to more recent data about socioeconomic status and poverty levels.* 

# Research Question
During 2008 - 2012, which socioeconomic factor is most strongly correlated with the highest levels of poverty in the Chicago area?

# Data Cleaning
I dropped the Community Area Number and Hardship Index column since these were excluded from the analysis. 

# Exploratory Data Analysis

I generated histograms to visualize the distribution of poverty levels. The histogram skewed to the left with a bimodal peak in the 20% bin. The histogram shows that the average poverty levels across community groups is ~20% (21.74% according to the summary statistics) and that 30 community areas’ poverty levels are in the 20% range.

I also created a pairplot to visualize linear relationships between variables.  

# Correlation Coefficient and Linear Regression 
I created a correlation coefficient matrix, which shows that the correlation coefficient for unemployment and poverty levels is closest to 1 at .80. This indicates a strong linear relationship, suggesting that reducing unemployment levels may have a more significant impact on lowering poverty levels compared to decreasing crowded housing, increasing high school diploma rates, or raising per capita income

Per capita income is lowest at -.57. It does not have a linear relationship with poverty level.  

I performed linear regression analysis to investigate the association between poverty rates and unemployment rates, high school diploma rates, crowded housing rates, and per capita income. Upon comparing the slopes of the four models, unemployment has the highest slope, meaning that lowering unemployment levels is likely to have the most significant impact on lowering poverty levels. For every percentage point that the unemployment rate increases, the poverty percentage increases by 1.22 percentage points. 

Unemployment: y = 1.22x + 2.99
High School diploma: y = 0.41x + 13.33
Crowded housing: y = 1.0x + 16.82
Per Capita Income: y = -0.0x + 32.68

# Conclusions 

Unemployment has the strongest positive linear relationship with poverty levels when compared to crowded housing, high school diploma, and per capita income. Lowering levels of unemployment may lower poverty levels at a more effective rate than reducing crowded housing rates, increasing high school diploma rates, or increasing per capita income. However, correlation does not equal causation and there may be confounding factors. 

I would suggest rerunning this analysis with more recent data to compare how the socioeconomic factors have changed over time and if the results of this analysis hold true. 
