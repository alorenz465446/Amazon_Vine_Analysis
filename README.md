# Amazon_Vine_Analysis

## Overview

The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this analysis, I’ll have access to approximately 50 datasets containing reviews for a specific product. I will pick one dataset and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, I'll use Pandas to determine if there is any bias toward favorable reviews from Vine members in my dataset. Finally, write a summary analysis for stakeholders.


## Analysis

Does a paid Vine review make a difference in the percentage of 5-star reviews?

I have chosen to do my analysis on a datset about shoe reviews from Amazon. Using Pandas, I will make a conclusion on whetehr or not there is bias toward favorable reviews from Vine memebers.

Ho: no difference in vine 5 star reviews (paid = unpaid) </br>
Ha: there is a difference (paid <> unpaid)

**Finding: The percentage of 5 star reviews is slightly skewed when comparing the results** 

### Results: 

<img width="400" alt="number_vine_reviews" src="https://user-images.githubusercontent.com/107652317/194785697-9da5131b-cc4d-4fe6-8123-8bb1d8032b91.PNG">

* 22 Vine reviews 
* 26,987 non-Vine reviews


<img width="618" alt="paid_5star" src="https://user-images.githubusercontent.com/107652317/194785786-67d75251-d4a4-459c-a191-766011862ee7.PNG">
<img width="648" alt="unpaid_5star" src="https://user-images.githubusercontent.com/107652317/194785794-dbf3f108-52e2-4fe1-9dad-0c02aeed32a4.PNG">

* 13 Vine reviews were 5 stars 
* 14,475 non-Vine reviews were 5 stars


<img width="537" alt="percentage_paid_5star" src="https://user-images.githubusercontent.com/107652317/194785752-2a1a0827-e3d9-4464-9e59-4f9503d75d8c.PNG">
<img width="548" alt="percentage_unpaid_5star" src="https://user-images.githubusercontent.com/107652317/194785772-423b2921-26e2-4360-a8c6-c372268c554d.PNG">

* Percentage of paid (in the vine program) 5 star reviews: 59%
* Percentage of unpaid (not in vine program) 5 star reviews: 54%


### Summary: 

There is a positivity bias for reviews in the Vine program. There was still a 5% increase in Vine 5 star reviews than non Vine memeber reviews, even though non Vine memeber ratings tremendously outnumbered Vine memeber ratings. Also, there is reason to believe that the percentage of 5 star reviews is somehwat tied to whether the reviewer is paid or unpaid. 

To do a quantative analysis, the hypothesis test would need to be evaluated comparing the proportion of 5 star reviews among the two samples.


#### Resources 

* Google Colaboratory 
* PG Admin
* Amazon Web Services
* Jupyter Notebook
