# PetMind

## Background
PetMind is a retailer of products for pets. They are based in the United States. PetMind sells products that are a mix of luxury items and everyday items. Luxury items include toys. Everyday items include food. The company wants to increase sales by selling more everyday products repeatedly. They have been testing this approach for the last year. They now want a report on how repeat purchases impact sales.

## The Data
The dataset ([found here](https://github.com/vchow6/Pet-Box-Subscription/blob/main/pet_supplies_2212.csv)) was provided by DataCamp through their Data Analyst Associate Certification program.

## Data Validation
The original data is 1500 rows and 8 columns. I utilized Python for data validation and cleaning, with changes of each column noted in the below: 

**product_id:** data type of **product_id** was changed from "numeric" to "character". The column has unique data and no missing values. 

**category:** data type of **category** is "character", as per criteria. Data has repeate values, with 7 unique values. Some missing data are labeled as '-'. The missing '-' data were replaced with 'Unknow' for clarification

**animal:** the data type of **animal** is "character", as per criteria. The data has repeate values (with 4 unique values), and no missing values. No changes were made

**size:** the data type of **size** is "character", as per criteria, with repeated values, and no missing values. However, the repeated values were all in different formats (all capitalized vs. all lower case vs. a mix of lower and upper cases, etc), making it several extra unnecessary categories. To fix this, the data was changed to all having a proper capitalization (upper case for the first letter of each value) 

**price:** the data type of **price** was changed from "object" to "numeric", per criteria. The data is all positive and there's no missing values. 

**sales:** the data type of **sales** is "numeric"/"float", as per criteria. There are no negative values and no missing data. No changes were made

**rating:** the data type of **rating** is "numeric", as per criteria. There were 150 missing data, thus they were replaced to '0'. I have also converted the data type from 'float' to 'int' within Pandas in Python

**repeat_purchase:** the data type of **repeat_purchase** is "numeric", criteria. It has repeate values and no missing data. No changes were made


## Distribution of Sales

Looking at the graph,the equipment category has the most count of repeat purchases. The categories are unbalance across the board, with Equipment making the most number of repeat sales, while the Accessory and Unknown made the lowest amount of repeat sales.

![image](https://github.com/vchow6/PetMind/blob/main/Number%20of%20Repeat%20Purchases%20Count%20per%20Category.png) 

With the below graph, we can see that this is a normal distribution, with the average of sales at around 1,000 dollars. There are some outliers sales at 2,250 dollars.

![image](https://github.com/vchow6/PetMind/blob/main/Distribution%20of%20All%20Sales.png)


## Conclusion

Per the visual below, not repeat purchases had a higher amount of sales compared to sales of repeat purchases, however both interquartile ranges are close to similar to each other, with their mean almost exactly the same. This indicate that sales of repeat purchases were skewed slighlty more towards more expensive items than the sales of not repeat purchases. Further analysing the sales of repeat purchases in the second graph, while Equipment had the highest count number of repeat purchase under Task 1, Food, an everyday item, looks to have the highest amount of repeated sales in dollars, indicating that the company was able to achieve its goal of increase sales by selling more everyday products repeatedly.

![image](https://github.com/vchow6/PetMind/blob/main/Sales%20of%20Not%20Repeat%20vs.%20Repeat%20Purchases.png)

![image](https://github.com/vchow6/PetMind/blob/main/Sales%20of%20Repeat%20Purchase%20by%20Category.png)
