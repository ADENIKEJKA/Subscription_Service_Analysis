# Subscription_Service_Analysis

### Project Title: Customer Segmentation for A Subscription Service 

[Project Overview](#project-overview)

[Data Sources](#data-sources)

[Tools Used](#tools-used)

[Data Cleaning and Preparations](#data-cleaning-and-preparations)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Analysis](#data-analysis)

[Inferences](#inferences)

[Conclusion](#conclusion)

### Project Overview
---
The purpose of this project work is to analyze customer data for a subscription service done in two years. This analysis helps to identify important trends and segments based on customer behaviors and also cancelations and renewals of subscriptions. 

### Data Sources
---
The primary source of this data was provided by the subscription service provided based on infromation gotten from their various customers in different regions where their service is provided. The data was presented in an excel document.

### Tools Used
---
- MIcrosoft Excel; [Download here](https://www.microsoft.com)
  1. For Data Cleaning
  2. Analysis
  3. Visualization
 
- SQL - Structured Query Language for Querying of Data
- Power BI for Data cleaning, Analysis and Presentation
- GitHub for Portfolio building

### Data Cleaning and Preparations
---
The following tasks were executed during the first stage of data cleaning and preparations:
1. Data loading and examination
2. Removal of Duplicate information in the data
3. Formatting and data cleaning

### Exploratory Data Analysis
---
EDA involved looking at the data to find important insights like:
-What are the subscription types?
-What is the average subscription duration?
-What are the subscription patterns and trends?

### Data Analysis
---
Here, we included some of the DAX expressions used in the study along with a few simple lines of code or queries;
```SQL
SELECT Region, COUNT(CustomerID) AS TotalCustomers
FROM Customers
GROUP BY Region
ORDER BY Region;

SELECT TOP 1 SubscriptionType, COUNT(CustomerID) AS TotalCustomers
FROM Customers
GROUP BY SubscriptionType
ORDER BY TotalCustomers DESC;

SELECT [CustomerName]
FROM [dbo].[SUB DATA]
WHERE [Canceled] IS NOT NULL
  AND DATEDIFF(day,[SubscriptionStart] , [Canceled]) <= 180;

SELECT TOP 3 Region,
       COUNT(*) AS Cancellation_count
FROM [dbo].[SUB DATA]
WHERE [Canceled] IS NOT NULL
GROUP BY Region
ORDER BY Cancellation_count DESC;
```
### Data Visualization
---
![SUB TYPES](https://github.com/user-attachments/assets/198a7a9a-5273-4894-a786-322dcc318cb0)

![ANNUAL REVENUE   CANCELED SUBS](https://github.com/user-attachments/assets/46c665e4-f90d-4462-a7f1-b4c1baa690d6)

![SUB REVENUE BY MONTHS](https://github.com/user-attachments/assets/919c1bf4-d712-4e02-b410-4e460e9ef0bf)

![EXCEL PROJECT 2](https://github.com/user-attachments/assets/30d4c8cd-0da0-4181-a46f-3c9201dbf7ae)

![EXCEL PROJECT](https://github.com/user-attachments/assets/5f1af952-f296-448d-9957-6259732b544a)

![Subscription service customer analysis PBI](https://github.com/user-attachments/assets/29a97467-2960-4157-b7fd-7e545e82d242)

### Inferences
---
1. Basic Plan: The Basic subscription generates the most income, suggesting that it probably has the greatest user base. This shows that the Basic plan is popular with many people, maybe because it is inexpensive and seen as valuable. In order to encourage Basic members to upgrade to higher tiers, the service may take into account upselling chances.
2. High Value from Premium Subscribers: Premium is the second-largest source of revenue, indicating a sizable customer base prepared to pay more for more advanced capabilities. Premium customers could be the most involved and devoted, therefore catering to their needs with special offers or extra incentives could help keep and even expand this market.
3. Standard Plan underperformance: The Standard plan generates the least amount of money, which may indicate that consumers are either lured to the Premium plan's more extensive offerings or prefer the value of the Basic plan. This suggests that the Standard plan might be less appealing due to a lack of obvious distinctiveness or attraction. The Standard plan's uptake could be increased by reassessing its features or cost or by clearly separating it from the Basic and Premium plans.
4. Possibilities for Tiered Upgrades: Given the popularity of Basic and Premium, the business might think about developing customized upgrade routes. Giving Basic members who upgrade to Standard access to exclusive deals or perks, for example, may increase conversions and increase income from both the Standard and Premium sectors.
5. Potential Price Changes: The Basic plan's popularity indicates that its prices may be quite competitive, but it also raises the possibility that some consumers are losing out on higher tiers' value. Retaining existing customers and encouraging some to move up to higher tiers if they want better value could be achieved by gradually raising the Basic plan's price while improving its services.
6. Retention Focus on Premium Subscribers: Since Premium customers generate a high amount of revenue individually, retention strategies such as exclusive content, loyalty rewards, or personalized customer service for this group could be beneficial. Ensuring satisfaction and loyalty among Premium users may be critical to maintaining stable revenue from this segment.
7. Market Segmentation Insights: The segmentation shows a client base that includes value-seeking (Standard), premium-seeking (Premium), and budget-conscious members (Basic). This might point to chances for focused advertising, in which Basic users are given reasonably priced value upgrades while Premium subscribers are given customized messages emphasizing special advantages.

### Conclusion
---
The analysis conducted showed that there was a significant decline in the overall number of customers in 2023. Therefore, these inferences should be used as a guide to develop strategies for customer retention, targeted marketing, and possibly restructuring the subscription plans for optimal growth and customer satisfaction.





   









