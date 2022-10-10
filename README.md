# Amazon_Vine_Analysis

## Overview

The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this analysis, I’ll have access to approximately 50 datasets containing reviews for a specific product. I will pick one dataset and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, I'll use Pandas to determine if there is any bias toward favorable reviews from Vine members in my dataset. Finally, write a summary analysis for stakeholders.


# Analysis

Does a paid Vine review make a difference in the percentage of 5-star reviews?

I have chosen to do my analysis on a datset about shoe reviews from Amazon. Using Pandas, I will make a conclusion on whetehr or not there is bias toward favorable reviews from Vine memebers.

Ho: no difference in vine 5 star reviews (paid = unpaid)
Ha: there is a difference (paid <> unpaid)

Results: 


How many Vine reviews and non-Vine reviews were there?
<img width="400" alt="number_vine_reviews" src="https://user-images.githubusercontent.com/107652317/194785697-9da5131b-cc4d-4fe6-8123-8bb1d8032b91.PNG">

There were 
How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
<img width="618" alt="paid_5star" src="https://user-images.githubusercontent.com/107652317/194785786-67d75251-d4a4-459c-a191-766011862ee7.PNG">
<img width="648" alt="unpaid_5star" src="https://user-images.githubusercontent.com/107652317/194785794-dbf3f108-52e2-4fe1-9dad-0c02aeed32a4.PNG">



What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
<img width="537" alt="percentage_paid_5star" src="https://user-images.githubusercontent.com/107652317/194785752-2a1a0827-e3d9-4464-9e59-4f9503d75d8c.PNG">
<img width="548" alt="percentage_unpaid_5star" src="https://user-images.githubusercontent.com/107652317/194785772-423b2921-26e2-4360-a8c6-c372268c554d.PNG">


There is a bulleted list that addresses the three questions for unpaid and paid program reviews (7 pt)

Summary: 
* Percentage of paid (in the vine program) 5 star reviews: 59%
* Percentage of unpaid (not in vine program) 5 star reviews: 54%

In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.

There is a slight positivity bias for reviews in the Vine program. Seeing a 5% increase (59 - 54) in Vine 5 star reviews than non Vine memeber reviews makes me believe this bias. Also, there is reason to believe that the percentage of 5 star reviews is somehwat tied to whether the reviewer is paid or unpaid. 


Finding: There is a slight positive bias when comparing vine reviews to not_vine reviews. 

There is a reason to believe that 5star ratings are tied to whether reviewers are paid or unpaid.




# Resources 

* Google Colaboratory 
* PG Admin
* Amazon Web Services
* Jupyter Notebook
