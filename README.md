# PetMind

## Background
PetMind is a nationwide pet product retailer in the United States. PetMind sells products that are a mix of luxury items and everyday items. The company wants to increase sales by selling more everyday products repeatedly. They have been testing this approach for the last year. They now want a report on how repeat purchases impact sales.

### Customer Questions:
The marketing team would like to answer the following questions to help with the decision:
* How many products are being purchased more than once?
* Do the products being purchased again have better sales than others?
* What products are more likely to be purchased again for different types of pets?

## The Data
The dataset ([found here](https://github.com/vchow6/Pet-Box-Subscription/blob/main/pet_supplies_2212.csv)) was provided by DataCamp through their Data Analyst Associate Certification program.

### Data Validation

**Validation tasks performed**

The original data is 1500 rows and 8 columns. All columns were checked for missing data, and only the 'rating' column had 150 null or empty cells.

**product_id:** 
* Class of **product_id** was changed from "numeric" to "character".
* The column has all unique data and no missing values. 

**category:** 
* Class of **category** is "character", as per criteria.
* Data has 7 unique values
* Some missing data are labeled as '-'. The missing '-' data were replaced with 'Unknow' for clarification
* The unique values include: 'Equipment', 'Food', 'Toys', 'Medicine', 'Housing', 'Accessory', and 'Unknown'

**animal:** 
* Class of **animal** is "character", as per criteria.
* The data has 4 unique values, and no missing values.
* The unique values include: 'Cat', 'Fish', 'Dog', 'Bird'
* No changes were made to this data

**size:** 
* Class of **size** is "character", as per criteria
* The data has 9 unique values. Upon further inspection, the values are all formatted differently, thus creating more unecessary unique values (ie. 'small' vs 'SMALL' vs 'Small', which in this instance it creates 3 different distinct values). The data needs to be formatted properly in order categorize the data approriately for accurate data analysis
* The data values were changed to all have capitalized first letter, and lower case for the rest of the string
* The data now includes only 3 unique values: 'Small', 'Medium', 'Large'

**price:** 
* Class of **price** was changed from "object" to "numeric", per criteria.
* The data is all positive and there's no missing values. 

**sales:** 
* Class of **sales** is "float", as per criteria.
* There are no negative values and no missing data.
* No changes were made

**rating:** 
* Class of **rating** is "numeric", as per criteria.
* The 150 missing values where replaced to '0'.
* Converted the data type from 'float' to 'int'
* The data has 10 unique values, which is the rating from 0 to 9

**repeat_purchase:** 
* Class of **repeat_purchase** is "numeric", as per criteria.
* It has 2 unique values: 0 (represent single-purchase products) and 1 (represent multi-purchase products)
* No changes were made.


## Distribution of Sales

Looking at the graph,the equipment category has the most count of repeat purchases. The categories are unbalance across the board, with Equipment making the most number of repeat sales, while the Accessory and Unknown made the lowest amount of repeat sales.

![image](https://github.com/vchow6/PetMind/blob/main/Number%20of%20Repeat%20Purchases%20Count%20per%20Category.png) 

With the below graph, we can see that this is a normal distribution, with the average of sales at around 1,000 dollars. There are some outliers sales at 2,250 dollars.

![image](https://github.com/vchow6/PetMind/blob/main/Distribution%20of%20All%20Sales.png)


## Conclusion

Per the visual below, not repeat purchases had a higher amount of sales compared to sales of repeat purchases, however both interquartile ranges are close to similar to each other, with their mean almost exactly the same. This indicate that sales of repeat purchases were skewed slighlty more towards more expensive items than the sales of not repeat purchases. Further analysing the sales of repeat purchases in the second graph, while Equipment had the highest count number of repeat purchase under Task 1, Food, an everyday item, looks to have the highest amount of repeated sales in dollars, indicating that the company was able to achieve its goal of increase sales by selling more everyday products repeatedly.

![image](https://github.com/vchow6/PetMind/blob/main/Sales%20of%20Not%20Repeat%20vs.%20Repeat%20Purchases.png)

![image](https://github.com/vchow6/PetMind/blob/main/Sales%20of%20Repeat%20Purchase%20by%20Category.png)
