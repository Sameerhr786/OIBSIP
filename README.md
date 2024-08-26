# OIBSIP

**Customer Segmentation Project Report**
**Introduction**

This project focuses on customer segmentation, a powerful marketing technique that involves dividing a customer base into distinct segments based on shared characteristics, behaviors, or demographics. The primary purpose is to better understand and serve customers in a more personalized and targeted way. Exploratory Data Analysis (EDA) is a necessary preliminary step before using a segmentation algorithm.

**Data**
The dataset used in this analysis contains information about 2,205 customers and includes 39 columns. The dataset description is provided below:

Feature	Description	Comment
AcceptedCmp1	1 if customer accepted the offer in the 1st campaign, 0 otherwise	
AcceptedCmp2	1 if customer accepted the offer in the 2nd campaign, 0 otherwise	
AcceptedCmp3	1 if customer accepted the offer in the 3rd campaign, 0 otherwise	
AcceptedCmp4	1 if customer accepted the offer in the 4th campaign, 0 otherwise	
AcceptedCmp5	1 if customer accepted the offer in the 5th campaign, 0 otherwise	
AcceptedCmpOverall	overall number of accepted campaigns	This column was added from the list of actual columns
Response	1 if customer accepted the offer in the last campaign, 0 otherwise	
Complain	1 if customer complained in the last 2 years	
Customer_Days	number of days since registration as a customer	
education_2n Cycle	customer has secondary education	This column was added from the list of actual columns
education_Basic	customer has basic education	This column was added from the list of actual columns
education_Graduation	Customer has a bachelor degree	This column was added from the list of actual columns
education_Master	Customer has a masters degree	This column was added from the list of actual columns
education_PhD	Customer has a PhD	This column was added from the list of actual columns
marital_Divorced	1 if customer is divorced, 0 otherwise.	This column was added from the list of actual columns
marital_Married	1 if customer is married, 0 otherwise.	This column was added from the list of actual columns
marital_Single	1 if customer is single, 0 otherwise.	This column was added from the list of actual columns
marital_Together	1 if customer is in relationship, 0 otherwise.	This column was added from the list of actual columns
marital_Widow	1 if customer is a widow / widower, 0 otherwise	
Kidhome	number of small children in customer's household	
Teenhome	number of teenagers in customer's household	
Income	customer's yearly household income	
MntFishProducts	amount spent on fish products in the last 2 years	
MntMeatProducts	amount spent on meat products in the last 2 years	
MntFruits	amount spent on fruits products in the last 2 years	
MntSweetProducts	amount spent on sweet products in the last 2 years	
MntWines	amount spent on wine products in the last 2 years	
MntGoldProds	amount spent on gold products in the last 2 years	
NumDealsPurchases	number of purchases made with discount	
NumCatalogPurchases	number of purchases made using catalogue	
NumStorePurchases	number of purchases made directly in stores	
NumWebPurchases	number of purchases made through company's web site	
NumWebVisitsMonth	number of visits to company's web site in the last month	
Recency	number of days since the last purchase	
Z_CostContact	expected cost of the contact	
Z_Revenue	expected revenue of the contact

**Here is a sample of the data:**
AcceptedCmp1  AcceptedCmp2  AcceptedCmp3  AcceptedCmp4  AcceptedCmp5  AcceptedCmpOverall  Response  Complain  Customer_Days  education_2n Cycle  education_Basic  education_Graduation  education_Master  education_PhD  marital_Divorced  marital_Married  marital_Single  marital_Together  marital_Widow  Kidhome  Teenhome  Income  MntFishProducts  MntMeatProducts  MntFruits  MntSweetProducts  MntWines  MntGoldProds  NumDealsPurchases  NumCatalogPurchases  NumStorePurchases  NumWebPurchases  NumWebVisitsMonth  Recency  Z_CostContact  Z_Revenue
0            0             0             0             0             0                    0         0         0            2542                   0                 0                      1                 0              0                  0                1               0                   0               0           0           0   58138             88               193          54                 143         671             0                   2                      3                  4                 4                    5       28            9.0         3393.0
1            0             0             0             0             0                    0         0         0            7707                   0                 1                      0                 0              0                  1                0               0                   0               0           1           1   46344             92               138          71                 71          192             0                   1                      2                  2                 1                    1       58           11.0        11878.0
2            0             0             0             0             0                    0         0         0            1712                   1                 0                      0                 0              0                  0                1               0                   0               0           0           0   45828            193               699          42                 371         296             0                   4                      5                 10                 7                    3       16            8.0         3049.0
3            0             1             0             0             0                    1         0         0            1811                   1                 0                      0                 0              0                  0                1               0                   0               0           0           0    9450             19                31          10                 37          171             0                   2                      1                  1                 3                    4       54           13.0         2471.0
4            0             0             0             0             0                    0         0         0            1666                   0                 0                      1                 0              0                  0                1               0                   0               0           1           0   35288             10                30          10                 35          265             0                   1                      1                  2                 2                    4       28           13.0         3499.0

**Data Preparation and Cleaning**
The data was reviewed, and the following steps were taken:

Compared the dataset description to the actual columns in the dataset
Checked for missing values
Verified the data types of the columns
No major data quality issues were identified, and the dataset was deemed suitable for further analysis.

**Data Exploration**
Exploratory data analysis was conducted to gain a better understanding of the customer characteristics and behaviors. Key findings include:

The majority of customers have a bachelor's degree or higher education
Married customers make up the largest marital status group
Customers spend the most on meat and wine products
There is a wide range in the number of web visits and purchases made by customers
Feature Engineering
Based on the insights from the data exploration, the following new features were created:

TotalSpend: Total amount spent by the customer across all product categories
TotalPurchases: Total number of purchases made by the customer
AvgSpendPerPurchase: Average amount spent per purchase
K-Means Clustering
The K-Means clustering algorithm was applied to the dataset to segment the customers. The optimal number of clusters was determined to be 4 based on the elbow method and silhouette score.

Exploration of Clusters
The characteristics of the 4 identified clusters are as follows:

Cluster 1 (High Spenders): These customers have the highest income, spend the most across all product categories, and make the most purchases.
Cluster 2 (Medium Spenders): These customers have moderate income and spending levels, with a focus on meat and wine products.
Cluster 3 (Low Spenders): These customers have the lowest income and spending, with a preference for fruits and sweets.
Cluster 4 (Infrequent Buyers): These customers have the lowest number of purchases and web visits, indicating they are less engaged with the company.
Results
The customer segmentation analysis provided valuable insights into the different customer groups and their behaviors. The key findings are:

The company has a diverse customer base with varying spending patterns and product preferences.
Targeted marketing campaigns and product recommendations can be tailored to each customer segment to better meet their needs and increase engagement.
The high-spending customers should be the focus of retention efforts, while the low-spending and infrequent buyers may require more targeted acquisition strategies.
