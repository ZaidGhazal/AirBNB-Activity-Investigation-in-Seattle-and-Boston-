# AirBNB-Activity-Investigation-in-Seattle-and-Boston-
## Introduction
Airbnb is an online marketplace that connects people who want to rent out their homes with people who are looking for accommodations in that locale. It currently covers more than 100,000 cities and 220 countries worldwide. People who own properties are called hosts.  Customers usually look for accommodation in the desired area and choose what they prefer according to facilities, price/night, transportation availability, and so on. In this project, we will discover and analyze the data provided by Airbnb for 2 famous cities, Seattle and Boston in the US to answer some business questions related to Airbnb activities, using Python.

## Libraries Used:
- **Pandas**: Fast, powerful, flexible, and easy to use open-source data analysis and manipulation tool. It will help us to view, clean, and apply analysis techniques to the datasets.
- **NumPy**: NumPy is a library for the Python programming language, adding support for large, multi-dimensional arrays and matrices. It will help us in the mathematical calculation and data analysis.
- **Matplotlib & Seaborn**: These two libraries are so powerful in visualizing data and showing the relationship between features.
- **Scikit-learn & XGBoost**: Fabulous tools for predictive data analysis. They will lead us to create a fantastic Machine Learning model predicting a continuous-valued attribute as we will see later. 


## Boston and Seattle Datasets 
The data (for both cities) contain 92 numerical, categorical, and DateTime features. In this project, we will answer 3 questions using these features and records:

**- How To Be a Superhost** (Superhosts are experienced hosts who provide a shining example for other hosts, and extraordinary experiences for their guests. See https://www.airbnb.com/help/article/828/what-is-a-superhost for more details)

**- How the Price/Night Change Over the Year in Both Cities**

**- Predicting Property Price/Night in Seattle & Boston Using Machine Learning Model**

The data has many null values, irrelated and dependant features. As a result, we started with a data wrangling process where we dropped the out-of-interest features, mostly null columns, and records, and imputed the others using median and mode depending on the column (feature) type.

*Note:*There are 2 files for each city, `listings_Seattle.csv / listings_Boston.csv` and `calendar_Seattle.csv / calendar_Boston.csv` where `listings_` has the 92 features about hosts, properties details, and prices and they are used to figure out How To Be a Super Host and Predicting Property Price/Night in Seattle & Boston Using Machine Learning Model. `calendar_` files contain the price/night for each property during a period of time and they are used for identifying the Price/Night Change Over the Year in Both Cities. 

## Data Analysis:
After overviewing and cleaning the data we applied the analysis and visualization techniques to understand our data deeper and infer the relationship between features. The following results illustrate some of the main points regarding our analysis:
- Gaining high reviews in all sectors seems to be the major part of being a superhost.
- At all, as the response time decreases, the host will be more eligible to get the super badge.
- We could see that both cities have fluctuating prices over the year.
- Prices in July, June, and August become higher than the rest of the year months in both cities.
- Both cities have traffic peaks in summer due to tourism, medication, or business.

*Note*: Pandas and Matplotlib are mainly used with NumPy and Seaborn in this step. 

## Modeling:
In this step, we created a Machine Learning model to predict property price/night in Seattle & Boston. After many trials that took hours using different sklearn ML algorithms and scaling techniques, we achieved the best model with **r^2 = 0.55**  

- XGBoostRegressor was the best algorithm as we could apply the grid search and use GPU to make finding the best params is possible (actually with CPU it took ages).
- Not only XGBoostRegressor is used, but we tried many algorithms with the grid search.
- We might get better results if we build 2 models for each city.

#### Finally, welcome to the article I published on [Medium](https://medium.com/@zaid.eng2018/lets-be-a-superhost-on-airbnb-616afa7fae4f)  illustrating the project results in simple language.
     
     
## References:
 - Boston Data: https://www.kaggle.com/airbnb/boston
 - Seattle Data: https://www.kaggle.com/airbnb/seattle/data
