# Sales_Analytics

This project is a playground of time series and regression models, the data was got in a courera competition in Kaggle,that provided with daily historical sales data. 
My goal for this project was creating a Machine Learning model to forescast the main invoice resource in Games Market in the Russia using economics exogenous variables as GDP, Unemployment Rate, Moex and the RUB value in Dollar.

File descriptions
sales_train.csv - the training set. Daily historical data from January 2013 to October 2015.
test.csv - the test set. You need to forecast the sales for these shops and products for November 2015.
sample_submission.csv - a sample submission file in the correct format.
items.csv - supplemental information about the items/products.
item_categories.csv  - supplemental information about the items categories.
shops.csv- supplemental information about the shops.

Data fields
ID - an Id that represents a (Shop, Item) tuple within the test set
shop_id - unique identifier of a shop
item_id - unique identifier of a product
item_category_id - unique identifier of item category
item_cnt_day - number of products sold. You are predicting a monthly amount of this measure
item_price - current price of an item
date - date in format dd/mm/yyyy
date_block_num - a consecutive month number, used for convenience. January 2013 is 0, February 2013 is 1,..., October 2015 is 33
item_name - name of item
shop_name - name of shop
item_category_name - name of item category

## This project was splitted in 6 parts based in the Data Science methodology:
1 - Translate all the dataset to English
It was done using a Google Translate API called googletrans, that I needed to get around the API request Limits.

2- Data Understanding/Exploratory
In this stage we will understanding our Datasets, see how they fit, search for some NAN, missing values, type of my vars and the plot it in a table and graphs and identify the quality of our data.
Using bar plots, describe functions to find the 3 mains invoice sources and plot the time serie of them.

3- Features Preparation
 The treatment of the exogenous data the them sources. It was used RUB in Dollar data, Russia GDP, Unemployment Rate, Moscow Exchange data. where I used polynomial models to resample my independent variables.

4- Data Analysis
 In this stage we will modeling the data and try understanding the impact of the exogenous attributes in the sales using Pearson Correlation Coefficient with the goal of discovering some useful for our Machine Learning model. Was used heatmap, boxplot and regplot in the seaborn to extracting insights about the data.

5- Creating the Models
 Here was created 3 Machine Learning models with Scikit Learn, Linear Regression, Ridge Regression and Random Forest Regression. Using Pipeline with 2 transformers (StandarScaler and PCA).

6- Tuning Random Forest Regressor
 In this Final Stage I have used Grid Search to optimize the hyperparameter of my Random Forest Model, where I get 0.81 of Pearson Correlation.


*All another files is dataset used or created in the codes.

