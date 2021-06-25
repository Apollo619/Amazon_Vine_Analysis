# Amazon_Vine_Analysis

## Overview of Analysis:

Analyze Amazon reviews written by members of the paid ***Amazon Vine*** program and generate a written report for Jennifer to submit to the ***SellBy*** stakeholders. 

### Purpose

Using **PySpark** to perform the ETL process to extract the dataset, transform the data, and connect to an **AWS RDS** instance, and load the transformed data into **pgAdmin** we will determine if there is any bias toward favorable reviews from the Vine members in the selected dataset.

## Results: 

To perform this analysis a script was created to pull the data and clean up nulls. Next additional tables were used to split out the reviews of Vine *(paid)* versus non-Vine *(unpaid)*. The following questions were asked with results posted… 

1. How many Vine reviews and non-Vine reviews were there?
   - Based on the results of the script (see image below) we can tell that there were only *332* total vine reviews versus *61,614* for non-vine reviews. 

![]( https://github.com/Apollo619/Amazon_Vine_Analysis/blob/main/resources/paid%20vs%20unpaid.PNG)

2. How many Vine reviews, and non-Vine reviews were 5 stars?
   - Of the 334 paid reviews, *139* were 5-star ratings and *32,665* of the 61,614 unpaid reviews gave 5-star ratings. (See highlighted values in image below)

![]( https://github.com/Apollo619/Amazon_Vine_Analysis/blob/main/resources/5%20star%20paid%20vs%20unpaid.PNG)


3. Lastly, what percentage of Vine reviews, and non-Vine reviews were 5 stars?
   - With the total number of rating for both paid and unpaid reviews, as well as the total number of 5-star ratings, we were able to calculate what percentage for each type of review was responsible for 5-star ratings. See below image for results highlighted in yellow.

![]( https://github.com/Apollo619/Amazon_Vine_Analysis/blob/main/resources/percentage%20paid%20vs%20unpaid.PNG)

## Summary:

Based on the results of the analysis we can say that there was **no bias** detected toward favorable reviews from the Vine members in the selected dataset. This is determined by the **41.62%** observed for the *Paid* reviews that received 5-star ratings. Considering more than half of the reviews that received 5-stars are from *Unpaid* reviewers, we are confident in our analysis.

An additional recommended analysis to support the above statement would be to determine how many *Paid* Vine reviews for 4-star plus 5-star ratings account for the total number of votes versus *Unpaid* Vine reviews. This additional data will help provided a better understanding of the dataset. 
