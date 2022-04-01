<img src= "https://github.com/kyongminso/phase_2_project/raw/main/Images/01-velo-header-seattle-needle.webp">




# Listing Price Predictor

Author: [Kyongmin](https://www.linkedin.com/in/kyongminso/), Meir, [Tyler](https://www.linkedin.com/in/tyler-wood-08a036216/)



## Overview

Using Multiple Linear Regression and other forms of statistical analysis, we created a real estate price predictor for homes in King County. Our final model explicitly shows the top house features and their influence on the listing price. This predictive model can be used to help any investors who are thinking about expanding on their real estate portfolio.

MKT LLC has a prominent presence in the real estate market in the greater Seattle area, and as such, our predictive model can steer you in the right direction for growth and profit.


---------------
## Business Problem 
With the increase in population, the real estate market is on the rise which means there is a potential for capitalization in this growing market. Our model can provide an competitive edge in this growing environment. 
Seattle has a fast growing population, flush with wealthy individuals moving to the area to work for high-paying technology jobs. This setting provides a great opportunity for capitalization given that your company has the tools to differentiate yourself from the competition. Being an early adopter of powerful technologies is a great way to acquire that competitive edge, and our model could help propel your business' portfolio to the top.

------------

## Understanding the numbers


All of our data came from a csv dataset that was provided for us from the county itself. The dataset contains extensive detailed information on homes in the county ranging from square footage, bathrooms, bedrooms, etc. We had to dive into the data and do some data cleaning to make sure we were able to create our models.

------
## Models 

When working on this project, we used two different types of modeling: predictive modeling and inferential modeling. 



## Simple Linear Regression 

### Heatmap


<img src= "https://github.com/kyongminso/phase_2_project/raw/main/Images/heatmap.png">

The 'sqft_living' variable had the highest correlation with price. This is a great option for our first simple linear regression. The Pearson Correlation Coefficient of sq_ft living compared to price is .70. We can consider values .70 and above to be a significant linear correlation between two variables.

## Train-Test Split 

We performed a train-test split with:  y = target and X = housing features.  
We performed imputations to address the null values and properly scaled the data. We set up a dummy regressor to use as our first baseline comparison. Our first simple model outperformed the dummy regressor. For our train data, it gave us a value of .44 which means there is room for significant improvement. 



## Multiple Linear Regression 
Adding multiple feautures to our model allows us to more accurately predict the price. This adds complexity to the model, however, we have to be cautious that we aren't over complicating it. This allows us to determine the variance of the model as we progress through our iteration, as well as determing the relative contribution of each feature to the price. 

## Final Predictive Model

### mlr_9
After multiple iterations, some of which used recursive feature selection, we created our final predictive model, mlr_9, which gave us a train R-Squared value of .854 and gave us an test R-Squared  of .859. These values are similar, so this model was neither over fit or underfit. Additionally, our model scored an RMSE value of 131,810, which is our lowest error of all the models. This shows that mlr_9 is the most accurate model for predicting y (housing price).


### Predictive Model

Our top predictive model uses the following features: 
- Sq.ft. living 
- Sq. ft. living 15 
- Bathrooms
- View 
- Waterfront 
- Zip Code 
- Quality 

We measured the success of our final model with these statistics: 

1. Coefficient of Determination (R-Squared) 
- R^2 Trained = .854
- R^2 Test = .854
2. Root Mean Squared Error = ~ $132,000



#### What does this mean?
---
- 85% of the variance in the dependent variable is explained by the independent variable in our model.The similarity of the Test and Train R^2 values shows a lack of underfitting and overfitting. 
- Our prediction will on average be off about $132,000. 
 

<img src=https://github.com/kyongminso/phase_2_project/raw/main/Images/preds_actual_regplot.png>

The plot of predicted value vs. actual values shows a cluster around the line of best fit, which nearly has a slope of one. This tells us that our predicted values were close to our actual values. 

## Inferential Model

### mlr_10 (unscaled)

The purpose of Inferential Model is to find the relationship between the price and the features, and see how the relationship can affect their values. We chose mlr_10 unscaled as our inferential model. The inferential model uses the exact same features as our predictive model except that it is not scaled and we didn't use the log of the price. Although it provides lower R-squared values of .792 for our train, and .792 for test, we can still see that we are not overfitting or underfitting. The residuals show homoskedasticity, a normal curve, and qq plot that breaks one assumption. The Durbin Watson score is 1.96 which is close to 2, indicating minimal auto correlation. 

The graphs below show us the correlation between the different features and the target.


<img src="Images/sqft_living_regplot.png">

The bigger your house is, the higher the price of the home will be. 


<img src="Images/sqft_living15_regplot.png">

The bigger your neighbor's houses are, the price of the houses will increase. 


<img src="Images/bathroom_bar.png">

Looking at this graph, as the number of bathrooms increases, so does the price of the home. 




<img src="Images/view_bar.png">

The better the view, the higher the price of the home will be. 



<img src="Images/waterfront_bar.png">

If you have a waterfront view home, it will most likely drive up the value of your home. 



<img src= https://github.com/kyongminso/phase_2_project/raw/main/Images/Phase%202%20Presentation.png>






# Conclusion 
## Recommendations 
-------

These recommendations show specific actions that stakeholders should take to leverage our results. 

1. Use our model to accurately price the current inventory.  
- The housing market is inefficient. Often, there are multiple bids for one ask.
- Sometimes, houses are priced in an arbritrary manner due to emotion and sentimentality. 
- Our Model forgoes these drawbacks and provides a data-backed pricing tool.


2. Use our model to find undervalued homes.
- When growing a portfolio, it is crucial for new acquisitions to be profitable. 
- Our model offers an accurate listing price, allowing the stakeholder to acquire undervalued properties which can be sold for a profit. 


3.  Use the model to find the best features to include in new home builds. 
- When growing the porfolio through constructing new homes, our model accurately depicts the impact that the above featuires will have on the price. 
- This steers the stakeholder in the proper direction, allowing the stakeholder to make better choices in regards to the house features, which they will include in the new builds. 


Overall, all the model building and data cleaning gave us the RMSE value of about $132,000. The model can be more precise with a lower RMSE, but the model is accurate in that it will predict the price within the range. 
As seen by the qq plot, the linearity assumption is violated. With further data collection and research, the model can be improved. 
The focus should be on square foot living because of its affect on price.

## Next Steps
While our model is very capable of predicting prices for different houses, there are still many more opportunities that could be explored given funding for further research.
One thing that our model does not currently account for is inflation and housing market fluctuations, implementing these could improve the generalizability of our model and reduce model drift. 
One of the largest factors in our model was location, but if we were given more funding, we could use machine learning techniques to provide even more granular location data.
We could also further improve the explanatory power of our model by creating and collecting more novel variables and paring down the model to the bare essentials.


## For more information
---
To see more of this research, please view the [presentation](https://docs.google.com/presentation/d/1yD90aYa58sU7afved1218I4qQN6k-hgGJ7FpRrDJ0fU/edit#slide=id.g120e22c8c1b_2_20) for more information. 


## Sources
---
The links down below is where we got some of our information. 

- [GeekWire](https://www.geekwire.com/2021/census-data-shows-seattles-population-surge-last-decade-fueled-part-tech-job-growth/)

- [Seattle Times](https://www.seattletimes.com/seattle-news/data/surprise-seattle-was-the-fastest-growing-big-u-s-city-in-2020/)