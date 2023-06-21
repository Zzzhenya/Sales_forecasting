# Sales/Demand forecasting

## Dataset 

The initial purpose of the dataset was to forecast the total amount of products sold in every shop for the test set. The test set must be created using the train dataset's last month (October) without the target (item_cnt_day). **You need to forecast the sales for the shops and products of the resulting dataset for October 2015.** This allows you to compare each method's predicted data with actual data. Note that the list of shops and products slightly changes every month. Creating a robust model to handle such situations is part of the challenge.

While keeping the initial purpose in mind, here I am using daily historical sales data to learn time series forecasting methods. Instead of using the test dataset provided ( which does not contain the target data), I am using the last month of the training dataset as the test/validation data for the model.

### CSV files
  
1. sales_train.csv - the training set. Daily historical data from January 2013 to October 2015.

2. items.csv - supplemental information about the items/products.

3. item_categories.csv - supplemental information about the items categories.

4. shops.csv- supplemental information about the shops.

### Data fields

1. shop_id - unique identifier of a shop
2. item_id - unique identifier of a product
3. item_category_id - unique identifier of item category
4. item_cnt_day - number of products sold. **You are predicting a monthly amount of this measure**
5. item_price - current price of an item
6. date - date in format dd/mm/yyyy
7. date_block_num - a consecutive month number, used for convenience. January 2013 is 0, February 2013 is 1,..., October 2015 is 33
8. item_name - name of item ( In Russian)
9. shop_name - name of shop ( In Russian)
10. item_category_name - name of item category (In Russian)

## Process

1. Exploratory Data Analysis
2. Feature Engineering
3. Post-Feature-Engineering EDA
4. Prediction accuracy measurement
5. Forecasting
	1. Moving average
	2. ARIMA
	3. SARIMA
	4. Exponential Smoothing
	5. Regression

## Tools and libraries

* Python / Pandas / Numpy / matplotlib
* Jupyter-Lab
* sklearn.metrics
* statsmodels
* pmdarima

## References

* https://machinelearningmastery.com/moving-average-smoothing-for-time-series-forecasting-python/
* https://www.kaggle.com/code/carlmcbrideellis/time-series-a-simple-moving-average-ma-model
* https://medium.com/@josemarcialportilla/using-python-and-auto-arima-to-forecast-seasonal-time-series-90877adff03c
* https://machinelearningmastery.com/sarima-for-time-series-forecasting-in-python/
* https://machinelearningmastery.com/arima-for-time-series-forecasting-with-python/
* https://stackoverflow.com/questions/46146537/error-in-threading-sarimax-model
* https://www.tutorialspoint.com/why-do-time-series-have-to-be-stationary-before-analysis
* https://medium.com/analytics-vidhya/interpreting-acf-or-auto-correlation-plot-d12e9051cd14
* https://github.com/fabryandrea/forecasting-intro/blob/main/forecasting-intro.ipynb
* https://machinelearningmastery.com/time-series-data-stationary-python/
* https://barnesanalytics.com/sarima-models-using-statsmodels-in-python/
* https://machinelearningmastery.com/gentle-introduction-autocorrelation-partial-autocorrelation/
* https://www.statsmodels.org/dev/generated/statsmodels.tsa.statespace.sarimax.SARIMAX.html
* https://www.studocu.com/en-gb/document/loughborough-university/business-forecasting/lecture-8-decomposition-with-arima/18305535
* https://ademos.people.uic.edu/Chapter23.html#5_using_correlograms_and_partial_correlograms_to_determine_our_p_and_q_values
* https://github.com/fabryandrea/forecasting-exp-smoothing/blob/master/timeseries_exp_sm_statsmodels.ipynb
* https://www.dummies.com/article/technology/information-technology/data-science/big-data/autocorrelation-plots-graphical-technique-for-statistical-data-141241/
* https://otexts.com/fpp2/MA.html
* https://www.influxdata.com/blog/autocorrelation-in-time-series-data/
* https://otexts.com/fpp2/moving-averages.html
* https://www.datasciencesmachinelearning.com/2019/01/arimasarima-in-python.html
