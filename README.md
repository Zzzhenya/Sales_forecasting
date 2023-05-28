# Sales/Demand forecasting

## Dataset 


You are provided with daily historical sales data. The task is to forecast the total amount of products sold in every shop for the test set. The test set must be created using the train dataset's last month (October) without the target (item_cnt_day). **You need to forecast the sales for the shops and products of the resulting dataset for October 2015.** This allows you to compare the each method's forecasted data with actual data. Note that the list of shops and products slightly changes every month. Creating a robust model that can handle such situations is part of the challenge.

### File descriptions

  
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

4. Forecasting

	1. Moving average

	2. Regression
