# Amazon_Vine_Analysis
Big Data Analysis Using AWS RDS and S3

### Overview

The purpose of this project was to analyze Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this project, access was given to approximately 50 datasets. Each one containing reviews of a specific product, from clothing apparel to wireless products. From these datasets, one was chosen - Pet Products - and PySpark was used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Then, Pyspark was used to determine if there is any bias toward favorable reviews from Vine members in the Pet Products dataset. 

### Results

The results of this answered the following questions: 

- _How many Vine reviews and non-Vine reviews were there?
- How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?_

Based on the results derived with Pyspark from the vine_table dataset, of the **38,010** helpful reviews (with 20 or greater total votes and 50% or greater of helpful votes) that were analyzed, **170** reviews were from the Vine program, while **37,840** were non-Vine reviews. 

<p align=center> <img src="https://user-images.githubusercontent.com/95978097/167303684-bcc88c03-6a5b-48d3-bd25-18348d8b7e77.png"> </p> 

From the Vine reviews, **65** of the 170 helpful reviews were 5 star reviews - or **38.24%**, while **20,612** of the 37,840 were 5 star unpaid reviews - or **54.47%**.  

<p align=center> <img src="https://user-images.githubusercontent.com/95978097/167303771-5154072e-5e17-4c09-8a53-cf9c468f82cb.png"> </p> 

### Summary

Based on the results, there does **not** appear to be positivity bias within the Vine (paid) program. Of the 170 *helpful* Vine reviews, only 38.24% of those gave 5 star ratings whereas, of the 20,612 helpful unpaid reviews, 54.47% of those gave 5 star reviews. It could be assumed that the Vine program encourages reviewers to have discretion when leaving 5 star reviews and perhaps consider a certain criteria when leaving reviews on Amazon items.

An additional analysis that could be run to support the conclusion that the vine program does not derive positive review results, could be to determine the rating breakdown percentage; finding the percentage of helpful reviews that received 1-star, 2-stars, 3-stars, and 4-stars. While the tests that were conducted determined that this is not a positively biased program, it could be informative to determine if the program derives negativity bias or subpar results.

