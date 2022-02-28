# Amazon_Vine_Analysis

### Overview of the analysis: Explain the purpose of this analysis.

analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review. 
In this project, we have access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. we need to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next,we use PySpark to determine if there is any bias toward favorable reviews from Vine members in your dataset. 


### Results: Using bulleted lists and images of DataFrames as support, address the following questions:

After loading DataFrames to tables in pgAdmin, we run a query to check that the tables have been populated.

![This is an image](sql1.png)

![This is an image](sql2.png)

How many Vine reviews and non-Vine reviews were there?

- total Vine reviews : 22
- total non-Vine reviews : 26987

![This is an image](q1.png)

How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

- 5 stars Vine reviews : 13
- 5 stars non-Vine reviews : 14475

![This is an image](q2.png)

What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

- percentage of 5 stars Vine reviews : 59.09090909090909
- percentage of 5 stars non-Vine reviews : 53.63693630266425

![This is an image](q3.png)

### Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.

As we can see the majority of reviews are coming from non-Vine reviews which is 26987. overall of 5 stars reviews are from non-Vine reviews which is 14475. and percentage of 5 stars Vine reviews is 59 which is greater than non-Vine reviews.that shows that even though we have less vine reviews but it has a better percentage. the positivity analysis is biased towards Vine reviews with greater percentage but less reviews.
we could compare the number of Vine and non-Vine reviews without or smaller filters. we could count the total votes which are greater than 20 for Vine and non-Vine reviews and the same thing when we were calculating helpful votes. 