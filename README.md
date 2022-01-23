# Amazon_Vine_Analysis

## Overview
The purpose of this project was to choose one dataset out of fifty that all contain reviews of a specific project (my dataset was in the product category of musical instruments). We then performed the ETl process of extracting the dataset, transforming the data, connecting to an AWS RDS instance, and finally loading the data into pgAdmin. We used PySpark in order to determine if there is any bias towards favorable reviews from Vine members.

## Resources
- Data: Amazon Review Datasets
- Tools: AWS RDS instance/ pgAdmin / Google Colab / PySpark

## Results
Below, we can see two filtered DataFrames (only showing the top ten rows). The first showing only Vine reviews, and the second showing only non-Vine reviews.

![VineReviews](https://github.com/RyleeJensen/Amazon_Vine_Analysis/blob/main/Images/Vine_Reviews.png)

![NonVineReviews](https://github.com/RyleeJensen/Amazon_Vine_Analysis/blob/main/Images/NonVine_Reviews.png)

We can answer a few questions from our analysis:
  - Total Vine Reviews: 60
  - Total Non-Vine Reviews: 14477
  - 5-Star Vine Reviews: 34
  - 5-Star non-Vine Reviews: 8212
  - Percentage of Vine Reviews that were 5-Star: 56.67%
  - Percentage of Non-Vine Reviews that were 5-Star: 56.72%

## Summary
Although there is a large difference of total Vine reviews and total non-Vine reviews, we can see from the percentage of reviews that were 5-stars are practically the same. This means that we can conclude that there is no positivity bias for the reviews in the Vine program. People will not give a 5-star review just because they were paid to test a product, if they did then the percentage of 5-star reviews from the Vine program would be much higher than 56.67%. If we wanted to dig deeper, it would be a good idea to look closer at the actual review text. We could use Natural Language Processing to filter out the text and compare Vine reviews to non-Reviews. Do the Vine reviews actually give criticism or praise to the product? Or is the person simply selecting a random star review to give the product? This might be a helpful analysis to dive into for the future.
