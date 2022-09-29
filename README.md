# Kings County Housing Home Sales
### Author: Susan Mungai

# BUSINESS UNDERSTANDING
## Project Overview

The project used to analyse home sales in King's County in Washington to help a Selling Sunset Real Estate agency, to help them advise thier clients on how to plan when they want to sell their homes. 
The business case is to determine what features of a home increase sales, whether it is by home renovations or target clients.


# DATA UNDERSTANDING 
## Data Description

The  dataset contained information about 21597 homes with almost 21 different home attributes like for example:
* The number of bedrooms and bathrooms
* Square footage of the living space and number of floors
* The condition of the house
* Whether the house has a waterfront and a view
* The grade of the house which is the quality of construction
* How old the house is and the year of renovation
* Location
Some columns were dropped that had a low correlation with the price which would not have been of relevant use in the analysis. 

From the business question, Price is our dependent variable and the other columns that have strong correlation to it include the square footage of the living space and and space above the basement.


# DATA ANALYSIS 
## Simple Linear Regression
The use of Ordinary  Least Regression to do analysis. For the first model, the simple linear regression model, only one variable was used, the one the highest correlation to price which was Square footage. From a scatter plot, we see that the relationship is somewhat linear but a not perfect linear relationship. 
The model proves this with an accuracy of 49.6% and the metric of the Root Squared Mean Error shows us by how far our model is off and in this case it is slightly above 260,000.
The price of the house is prediced to increase by 283.40 for each square foot added.
If the sqft_living was 0 we would predict a decrease 48604.077 in the price. 
The regression line would be;
price = -48604.077 + 283.40 sqftliving

The conditions of normality (of residuals) and homoscedasticity were clearly violated (The distribution of the residals) `sqft_living` and `price` may have a better linear relationshIp if they were log-transformed.
### The log transformed model
The transforming of the distribution to make it more linear using the logarithmic transformation. The accuracy improves to 53.6% 

## Multiple Linear Regression Model
The previous model had a lower accuracy and to improve it, I experimented with more independent variables. I concluded that the more the variables were added, the more accurate the model was. 

I used all the variables in the dataset except the ones that I already deemed unnecessary for the analysis. 
From the multiple linear regression model, I concluded:
The model was more fit than the baseline model, the accuracy incresed to 68% and I also noticed an improvement in the Root Squared Mean Error which shows it was less off than the previous models.

# CONCLUSION
The final model has an improved R-squared score of 0.600 and yields information that allows us to make useful inferences about the predicted sale price of a house, as well what actions a homeowner may take in order to increase it.

Square footage of the living space: Increasing the square footage is associated with a higher sale price.

Condition of the house (maintenance): The reference point for the model is a house with a condition of "Average." For a condition of "Fair", we expect an increase in the price by 1758

Grade of the house (quality of construction): Higher grades are associated with higher sale prices.

Waterfront and view: Houses that are on a waterfront and houses with nice views will tend to sell for higher than houses that don't have these features.


# RECOMMENDATIONS 
The analysis was done to determine the features that will ensure increase in sales in the homes by the Selling Sunset agency 
* From the analysis, we see that increase in the square footage of living space, the house is expceted to sell for more.


* Some maintenance to improve the condition of the house to any higher classification, the expected sale price should go up.


* Higher grades(quality of construction and finishing) will ensure an increase in price of the home. The agency should invest in a quality design of the house by the quality of contractors during renovation, the landscaping and planning dring construction.


* Houses with beautiful views and a waterfront would sell faster. then the real estate agency should emphasize these in the listing, photos, and any other marketing for the home sale with these feaures.


# LIMITATIONS 
The analysis was doen to determine the features that will ensure increase in sales in the homes by the Selling Sunset agency 
* From the analysis, we see that increase in the square footage of living space, the house is expceted to sell for more.


* Some maintenance to improve the condition of the house to any higher classification, the expected sale price should go up.


* Higher grades(quality of construction and finishing) will ensure an increase in price of the home. The agency should invest in a quality design of the house by the quality of contractors during renovation, the landscaping and planning dring construction.


* Houses with beautiful views and a waterfront would sell faster. then the real estate agency should emphasize these in the listing, photos, and any other marketing for the home sale with these feaures.

