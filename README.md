# 1.0 The Company

(fictitious) Rossmann operates over 3,000 drug stores in 7 European countries. After the success of the expansion strategy of opening +240 drugstores in 2021 and with the good reaction of investors after the presentation of 3Q21 results, Rossman executives decided: +260 drugstores in 2022, maintaining the current geographic diversification and segmentation of customers. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance.  Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied.

# 2.0 Challenge
The CFO perceives the importance of having a more quantitative approach when taking decisions, reason why a small team of data scientists was hired and allocated with a clear objective in mind: predicting their daily sales for up to six weeks in advance to project the budget to renoval stores.

# 3.0 Delivarables
1. Explore the data – be creative and pay attention to the details. You need to provide the financials team a better understanding of the characteristic features of sales;
2. Create and describe a predictive model which allows the executives makes best decision to business growth and reach strategies goals.
3. How does the sales forecast model perform?
3. What is the best sales forecast for each store and worst case scenario.
4. What is the total revenue forecast for all stores, in terms of revenue, for the company?

# 4.0 The data

Files
train.csv - historical data including Sales

test.csv - historical data excluding Sales

sample_submission.csv - a sample submission file in the correct format

store.csv - supplemental information about the stores

Data fields

Most of the fields are self-explanatory. The following are descriptions for those that aren't.

Id - an Id that represents a (Store, Date) duple within the test set

Store - a unique Id for each store

Sales - the turnover for any given day (this is what you are predicting)

Customers - the number of customers on a given day
Open - an indicator for whether the store was open: 0 = closed, 1 = open

StateHoliday - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None

SchoolHoliday - indicates if the (Store, Date) was affected by the closure of public schools

StoreType - differentiates between 4 different store models: a, b, c, d

Assortment - describes an assortment level: a = basic, b = extra, c = extended

CompetitionDistance - distance in meters to the nearest competitor store

CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened

Promo - indicates whether a store is running a promo on that day

Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating

Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2

PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store

# 5.0 Solution Strategy  Development 
The strategy adopted was the following:

Step 01. Data Description: I searched for NAs, checked data types (and adapted some of them for analysis) and presented a statistical description.

Step 02. Feature Engineering: New features were created to make possible a more thorough analysis.

Step 03. Data Filtering: Entries containing no information or containing information which does not match the scope of the project were filtered out.

Step 04. Exploratory Data Analysis: I performed univariate, bivariate and multivariate data analysis, obtaining statistical properties of each of them, correlations and testing hypothesis (the most important of them are detailed in the following section).

Step 05: Data Preparation: Here I chose to scaling features by removing the mean and scaling to unit variance using StandardScaler method in sklearn.

Step 06. Feature selection: I used the Boruta package to find features with more importances.

Step 07. Machine learning modelling: Some machine learning models were trained. The one that presented best results after cross-validation went through a further stage of hyperparameter fine tunning to optimize the model's generalizability.

Step 08. Model-to-business: The models performance is converted into business values.

# 6.0 Conclusion

I used the XGBoost model to learn all the behavior of the data, after that, I trained and validated the model separating the dataset between test and validation, where the validation set is the 6 week subtraction of the original dataset, where I used to make the predictions.

After the entire process of implementing the model, training and perfomance evalute, I chose the XGB and with it I made the predictions.

I evaluated the model through 3 performance measurements: MAE, MAPE and RMSE. To facilitate understanding for the business users, I brought the results as best and worst predicted for each store.

In addition to the table of results for each store, it also brought a table that shows the total performance of the stores, in the best and worst scenario.

I also brought 4 graphs that our graphic model also presents our model, the first is a comparison of real sales and our model predictions, in the second it is possible to identify if the model is overestimating or estimating the performance of the stores, in the third lower left graph , deals with a bit of machine learning and shows us that the error follows a normal distribution, and finally, the fourth bottom right graph, shows an error analysis that we use in machine learning, where the points must be allocated in an 'imaginary tube '.

# 7.0 Next Step

1. Improve Model Accuracy by 5%
2. Implementation of the Model for Production
3. Model Workshop for People Business Users
4. Collect Model Usability feedback

REFERENCES
https://www.baass.com/blog/why-forecasting-is-important-for-business-success