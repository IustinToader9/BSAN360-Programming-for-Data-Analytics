## BSAN 360 Final Project Report

## Project Title: AirBNB Pricing Model

## Student(s): Iustin Toader, Satchel Manchester, Nichalas Perrone, Brandon Yan

---

#### Background
---
Airbnb is rapidly disrupting the marketplace for hotels and other traditional forms of
rental lodging. Their unique business model and value proposition has attracted a steadily growing set of users. New travel markets like “staycations” or short-medium distance getaways are becoming more common, and Airbnb’s platform provides a great opportunity to meet this demand. Supply of lodging has grown in tandem with demand for leisure travel, as there are now close to 8 million homeowners and apartment owners look to capitalize on this demand.


### Problem
---
Airbnb’s industry disruption is no secret, although new hosts can encounter a variety of
problems when attempting to grow into the market. These issues could be legal, marketing, and a myriad of others. However, the factor that affects them the most is pricing. Airbnb allows hosts to set their base price upon which the user viewed price will be based on (user viewed price includes cleaning fees, platform fees, etc.). If hosts price too high, they run the risk of turning away potential renters and losing out on revenue and cash flow, but if they price too low, they could leave money on the table. The goal of this project was to create a pricing model to price an Airbnb listing based on quantitative and qualitative variables like availability, room type and location so new hosts can effectively price their properties.

### Data 
---
The dataset that was utilized for the project gave both qualitative and quantitative insights
into various properties. The dataset included listings and their corresponding 16 quantitative and qualitative variables. Broken down into numerical and categorical data, the team began drilling down to understand which factors were relevant and how they were going to be able to contribute to the pricing model.
As the analysis in R started, the ten variables that initial were neighborhood, latitude, longitude, room type, minimum nights (to book the lodging), number of reviews, reviews per month, host listings, availability, and city.

### Conclusion
---
The model that was utilized was a multi-linear regression model, and the intent of the
model was to predict the price of an Airbnb location given the various factors associated with the listing. From here, the model was intended to be utilized by new hosts on the platform where they’d be able to input their listing characteristics to arrive at a base price. This would be considered the “fair-market value” of the listing.
In this process, four models were utilized, each with varying degrees of success. The first model arrived at a 44% adjusted r-squared value, and from here, the goals of subsequent models were to raise that as much as possible. For model 2, the team removed the variable “city” from the model. This slightly (almost insignificantly) decreased adjusted r-squared, however the model was successful in the removal of collinear variables. Model 3 saw an exclusion of latitude and longitude because there were large GVIF values for them. The model saw small adjusted GVIF for all variables, but performance was not significantly improved their either. In model 4, interaction terms were included between all numeric variables, but no tangible performance was realized as a result of the variation. Thus, model 2 ended up being the most successful model, and the model upon which final conclusions were made.

### Results
A few next steps post presentation that the team looked to implement fell into 2 buckets.
The first was re-assessment of model performance, and the second was to understand where the model could be better. In terms of model performance, we ran some analyses to compare the actual prices of listings with the model price to understand if the model was consistently over or under-predicting price. If so, the next steps there would be to drill deeper and make the adjustments necessary to become more precise. We found that our model over and under- predicted prices, and there wasn’t really a trend for us to follow with it.
In regard to improving the model, one of the next steps that was suggested was the quantification of qualitative data. For example, the number of reviews is a factor that was available to use, but the content of that review was unknown. A customer is going to care significantly more about the content of a review than the quantity of reviews that a listing has, so being able to quantify those factors was something that we wanted to do. However, that data was not readily available to the team, but it is something that would be implemented if the project was to go further.
All in all, the model, the model did a mediocre job at predicting price. It gives a good base number for hosts to take into consideration, but this should not be the sole price that owners use for their listings.

### Next Steps
This version of the code builds on top of the final project for BSAN360, as part of my ongoing research collaboration with Professor Cameron Bale, by implementing Lasso, Ridge, and Net-Elastic Generalized Linear Regressions. 
