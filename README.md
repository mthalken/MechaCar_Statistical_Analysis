# MechaCar_Statistical_Analysis

## The purpose of this analysis is to analyze data to help produce insights for MechaCar's production team. 

## Project Overview:
1. Use linear regression to predict mpg
2. Find the summary statistics on suspension coils
3. Determine the t-tests on suspension coils
4. Design a study to compare MechaCar to the competition

## Resources
- Source of data: [MechaCar_mpg.csv](https://github.com/mthalken/MechaCar_Statistical_Analysis/blob/main/data/MechaCar_mpg.csv), [Suspension_Coil.csv](https://github.com/mthalken/MechaCar_Statistical_Analysis/blob/main/data/Suspension_Coil.csv)
- Software: R 4.1.2, RStudio, Conda 4.10.3, Visual Studio Code 1.60.2
- Please see the refactored code [here](https://github.com/mthalken/MechaCar_Statistical_Analysis/blob/main/MechaCarChallenge.R).

## The analysis
### Linear Regression to Predict MPG

- Both the Vehicle Length and Ground Clearance provided a non-random amount of variance to the mpg values indicating they have a significant impact on mpg. The intercept was also shown to be statistically significant indicating there are factors not within the dataset that contribute to the mpg value. 

- The slope of the linear model is not considered to be zero because of the significant differences between the independent variables and must reject the null hypothesis.

- The linear model does predict mpg prototypes effectively (shown in the R-Squared value of 0.7149) at 71% accuracy. 

![png](https://github.com/mthalken/MechaCar_Statistical_Analysis/blob/main/images/Linear%20Regression%20to%20Predict%20MPG.png)

### Summary Stiatistics on Suspension Coils

- In the total summary statistics we can see that the variance is definitely under the 100 pounds per square inch, but there is an issue with one of the lots as seen in the lot summary statistics. Lot 3 has a variance of 170.2861224 which is well over the accepted threshold. 

![png](https://github.com/mthalken/MechaCar_Statistical_Analysis/blob/main/images/Total%20Summary.png)

![png](https://github.com/mthalken/MechaCar_Statistical_Analysis/blob/main/images/Lot%20Summary.png)


### T-Tests on Suspension Coils

- Looking at the T-Test results we can see that all lots, lot 1, and lot 2 show that they are not significantly different from the mean and the p-values are not low enough to reject the null hypothesis. While lot 3 shows that they are slightly different from the mean the p-value is low enough to reject the null hypothesis. With that being said we could see that we may have to discard or remove lot 3 or be looked at closer. 

![png](https://github.com/mthalken/MechaCar_Statistical_Analysis/blob/main/images/TTests.png)


### Study Design: MechaCar vs Competition

- While there can be multiple factors and variables that individuals look at when purchasing a car, looking at hauling/carrying capacity on mpg compared to competitors' vehicles. 

    - Metrics
        - We would need to look at the total interal or cabin space, trunk or bed space, hauling capacity, and miles per gallon on 3 different weight levels: light, medium, heavy. 
    - Hypothesis
        - Null: MechaCar's vehicles get the same mpg in light, medium, and heavy weights based on overall towing capacity. 
        - Alternate: MechaCar's vehicles get the statistically better mpg in light, medium, and heavy weights based on overall towing capacity.
    - Statistical Test
        - The best statistical test would be to use the ANOVA (Analysis of Variance). 
    - Data
        - To perform this study we would need information on MechaCar's and competitors towing/hauling capacity and total internal or bed space. We already have data on MechaCar's vehicle weight and mpg but would need to get the competitors as well as run tests on mpg based on weight capacities. 

