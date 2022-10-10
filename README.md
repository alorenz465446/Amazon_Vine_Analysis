# Amazon_Vine_Analysis

## Overview

The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this analysis, I’ll have access to approximately 50 datasets containing reviews for a specific product. I will pick one dataset and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, I'll use Pandas to determine if there is any bias toward favorable reviews from Vine members in my dataset. Finally, write a summary analysis for stakeholders.

This new assignment consists of two technical analysis deliverables and a written report. You will submit the following:

Deliverable 1: Perform ETL on Amazon Product Reviews
Deliverable 2: Determine Bias of Vine Reviews (python, pandas, or sql to do analysis)
Deliverable 3: A Written Report on the Analysis (README.md)

# Analysis
For this analysis, you'll determine if having a paid Vine review makes a difference in the percentage of 5-star reviews.

Overview of the analysis of the Vine program:

The purpose of this analysis is well defined (3 pt)

Results: Using bulleted lists and images of DataFrames as support, address the following questions:

How many Vine reviews and non-Vine reviews were there?
<img width="400" alt="number_vine_reviews" src="https://user-images.githubusercontent.com/107652317/194785697-9da5131b-cc4d-4fe6-8123-8bb1d8032b91.PNG">

How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
<img width="618" alt="paid_5star" src="https://user-images.githubusercontent.com/107652317/194785786-67d75251-d4a4-459c-a191-766011862ee7.PNG">
<img width="648" alt="unpaid_5star" src="https://user-images.githubusercontent.com/107652317/194785794-dbf3f108-52e2-4fe1-9dad-0c02aeed32a4.PNG">



What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
<img width="537" alt="percentage_paid_5star" src="https://user-images.githubusercontent.com/107652317/194785752-2a1a0827-e3d9-4464-9e59-4f9503d75d8c.PNG">
<img width="548" alt="percentage_unpaid_5star" src="https://user-images.githubusercontent.com/107652317/194785772-423b2921-26e2-4360-a8c6-c372268c554d.PNG">


There is a bulleted list that addresses the three questions for unpaid and paid program reviews (7 pt)

Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.

The summary states whether or not there is bias, and the results support this statement (2 pt)
An additional analysis is recommended to support the statement (2 pt)

Ho: no differences in vine 5star vine reviews (paid vs. unpaid)
Ha: there is a difference 

finding: The percentage of 5 star ratings is the same when comparing vine reviews to not_vine reviews 

There is a reason to believe that 5star ratings are tied to whether reviewers are paid or unpaid




# Resources 

* Google Colaboratory 
* PG Admin
* Amazon Web Services
* Jupyter Notebook
