# Subscription_Service_Analysis

### Project Title: Customer Segmentation for A Subscription Service 

[Project Overview](#project-overview)

[Data Sources](#data-sources)

[Tools Used](#tools-used)

[Data Cleaning and Preparations](#data-cleaning-and-preparations)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Analysis](#data-analysis)

[Inferences](#inferences)

[Conclusions](#conclusion)

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
- - MIcrosoft Excel; [Download here](https://www.microsoft.com)
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




