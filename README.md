# 1.0 Context

(fictitious) Rossmann operates over 3,000 drug stores in 7 European countries. After the success of the expansion strategy of opening +240 drugstores in 2021 and with the good reaction of investors after the presentation of 3Q21 results, Rossman executives decided: +260 drugstores in 2022, maintaining the current geographic diversification and segmentation of customers. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance.  Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied.

# 2.0 Challenge
The CFO perceives the importance of having a more quantitative approach when taking decisions, reason why a small team of data scientists was hired and allocated with a clear objective in mind: predicting their daily sales for up to six weeks in advance.

# 3.0 Delivarables
1. Explore the data – be creative and pay attention to the details. You need to provide the financials team a better understanding of the characteristic features of sales;
2. Create and describe a predictive model which allows the executives makes best decision to business growth and reach strategies goals.

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

# 6.0 Conclusion

# 7.0 Lesson Learned

# 8.0 Next Step

REFERENCES
https://www.baass.com/blog/why-forecasting-is-important-for-business-success