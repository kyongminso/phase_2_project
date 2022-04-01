# Listing Price Predictor

Author: [Kyongmin](https://www.linkedin.com/in/kyongminso/), Meir, [Tyler](https://www.linkedin.com/in/tyler-wood-08a036216/)



## Overview

Using Multiple Linear Regression and other forms of statistical analysis, we used these practices to create a real estate price predictor for homes in King County. We created models that would show what factors can influence the housing prices in the county. These prediction models can be used to help any investors who are thinking about expanding on their real estate portfolio.

MKT LLC has a prominent presence in the real estate market in the greater Seattle area, we can provide a competitive edge through our housing price prediction model and can steer you in the right direction for growth and profit


---------------
## Business Problem 
With the increase in population, the real estate market is on the rise which means there is a potential for capitalization in this growing market and we believe that our model can provide an edge in the competitive market.

------------

## Understanding the numbers


All of our data came from a csv dataset that was provided for us from the county itself. The dataset contains thousands of detailed information of homes in the county ranging from square footage, bathrooms, bedrooms, and many other useful information. We had to dive into the data and do some data cleaning to make sure we were able to create our models. We were introduced to new tools, sklearn as well as use from the common tools we have used before:  pandas, numpy, seaborn, statsmodels, and matplotlib. All of these different tools were necessary in order for us to create a succesful model for this research. 

------
## Models 

When working on this project, we used two different types of modeling: predictive modeling and inferential modeling. 


### Inferential Models


Our target variable was price and the graphs below show us the correlation between the different features and the target. 


<img src="Images/bathroom_bar.png">

Looking at this graph, as the number of bathrooms increases, so does the price of the home. 

<img src="Images/sqft_living15_regplot.png">

The bigger your neighbor's houses are, the price of the houses will increase. 

<img src="Images/sqft_living_regplot.png">

The bigger your house is, the higher the price of the home will be. 



<img src="Images/view_bar.png">

The better the view, the higher the price of the home will be. 



<img src="Images/waterfront_bar.png">

If you have a waterfront view home, it will most likely drive up the value of your home. 

### Predictive Models

Our top predictive models uses the following features: 
- Sq.ft. living 
- Sq. ft. living 15 
- Bathrooms
- View 
- Waterfront 
- Zip Code 
- Quality 

We measured the success of our final model with these statistics: 

- Coefficient of Determination (R-Squared) = .86
- Root Mean Squared Error = ~ $132,000

#### What does this mean?
---
- 86% of the variance in the dependent variable is explained by the independent variable in our model.
- Our prediction will on average be off about $132,000. 
 

<img src="https://github.com/kyongminso/phase_2_project/raw/main/Images/preds_actual_regplot.png">

We see when we plot predicted value vs actual values the scatter plot clusters around the line of best fit, which has a slope of almost, nearly one. This tells us that our predicted values were close to our actual values. 



## Inferential Models 
The purpose of Inferential Model is to find the relationship between the price and the features, and see how the relationship can affect their values. 

- $170 increase in price per 1 sq ft
- $61 increase in price per 1 sq feet in nearest 15 neighbors
- $9,344 increase in price 1 bathroom increase
- $516,600 increase in price if it is waterfront
- $73,020 Decrease in price if no view
- $15, 880 increase in price if fair view 
- $101,400 increase in price if good view 
- $258,900 increase in excellent view  


## Recommendations 
-------
We recommend you explore these 3 points to consider for your benefit: 
- Use our model to accurately price the current inventory. 
- Use our model to find undervalued homes. 
- Use the model to find the best features to include in new home builds. 




## For more information
---
To see more of this research, please view the [presentation](https://docs.google.com/presentation/d/1yD90aYa58sU7afved1218I4qQN6k-hgGJ7FpRrDJ0fU/edit#slide=id.g120e22c8c1b_2_20) for more information. 


## Sources
---
The links down below is where we got some of our information. 

- [GeekWire](https://www.geekwire.com/2021/census-data-shows-seattles-population-surge-last-decade-fueled-part-tech-job-growth/)

- [Seattle Times](https://www.seattletimes.com/seattle-news/data/surprise-seattle-was-the-fastest-growing-big-u-s-city-in-2020/)