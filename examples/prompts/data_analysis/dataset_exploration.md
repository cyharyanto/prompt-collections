# Data Analysis Prompt Examples

This document provides example prompts for data exploration and analysis tasks.

## Initial Dataset Exploration

```
You are a skilled data analyst. I want you to help me explore and understand this dataset. 

Dataset description:
- Name: Customer Purchase History
- Rows: 15,000 customer transactions
- Time period: January 2022 - December 2022
- Fields:
  * transaction_id (unique identifier)
  * customer_id (customer identifier)
  * purchase_date (YYYY-MM-DD format)
  * product_id (product identifier)
  * product_category (categorical: Electronics, Clothing, Home, Food, Other)
  * purchase_amount (numerical: purchase value in USD)
  * payment_method (categorical: Credit, Debit, PayPal, Other)
  * customer_age (numerical: age in years)
  * customer_gender (categorical: M, F, Other)
  * customer_location (categorical: state/province code)

Here's a sample of the first 5 rows:

transaction_id,customer_id,purchase_date,product_id,product_category,purchase_amount,payment_method,customer_age,customer_gender,customer_location
T1001,C5432,2022-01-05,P765,Electronics,499.99,Credit,34,M,CA
T1002,C8765,2022-01-06,P234,Clothing,59.95,PayPal,27,F,NY
T1003,C5432,2022-01-12,P890,Home,129.50,Credit,34,M,CA
T1004,C2341,2022-01-15,P567,Electronics,899.00,Credit,45,M,TX
T1005,C7654,2022-01-17,P123,Food,75.25,Debit,29,F,FL

Please help me understand:
1. What are the key characteristics of this dataset?
2. What initial patterns or trends can you identify?
3. What potential analyses would be valuable to perform?
4. What data quality issues should I be aware of?
5. What visualizations would you recommend creating?
```

## Statistical Analysis Request

```
You are a statistician with expertise in retail data. I need you to analyze this sales dataset and provide statistical insights.

Dataset summary:
- Monthly sales data by product category (Electronics, Clothing, Home, Food)
- Time period: 24 months (Jan 2021 - Dec 2022)
- Includes promotional periods and seasonal events

Key questions:
1. Is there a statistically significant difference in sales performance between categories?
2. Which product category shows the strongest seasonal patterns?
3. What is the correlation between promotional spending and sales by category?
4. Can you identify any significant outliers in the data?
5. What statistical models would you recommend for forecasting future sales?

For each analysis, please:
- Describe the statistical approach you would use
- Explain what tests would be appropriate and why
- Interpret what the results would mean for business decisions
- Note any additional data that would strengthen the analysis

Here's the summary data for Electronics:
Month,Sales,Promo_Spend,Seasonal_Index
Jan-21,156200,15000,0.85
Feb-21,142500,12000,0.78
Mar-21,165300,18000,0.92
Apr-21,170200,20000,0.95
May-21,168700,15000,0.94
Jun-21,190300,25000,1.05
Jul-21,210500,30000,1.15
Aug-21,225600,35000,1.25
Sep-21,195400,22000,1.08
Oct-21,178900,20000,0.98
Nov-21,245600,40000,1.35
Dec-21,302300,45000,1.70
...

[Additional category data would be provided here]
```

## Data Visualization Recommendations

```
You are a data visualization expert. I have a customer segmentation dataset and need recommendations for the most effective ways to visualize key relationships and patterns.

Dataset contains:
- 5,000 customers
- 12 variables including demographics, purchase behavior, and engagement metrics
- 4 identified customer segments from a clustering algorithm

Key variables:
- Annual spend (numerical: 0-50,000)
- Purchase frequency (numerical: 0-200 transactions per year)
- Average order value (numerical: 0-1,000)
- Product category preference (categorical: 5 categories)
- Customer tenure (numerical: 0-15 years)
- Age group (categorical: 18-24, 25-34, 35-44, 45-54, 55+)
- Channel preference (categorical: online, in-store, mobile app)
- Loyalty program status (binary: member/non-member)
- Customer segments (categorical: 4 segments from clustering)

I need visualization recommendations that will:
1. Clearly show the differences between the 4 customer segments
2. Highlight the relationship between spend, frequency, and value
3. Show how segment composition varies by age group and channel preference
4. Visualize segment stability over customer tenure
5. Present the findings to non-technical stakeholders

For each recommendation, please:
- Specify the exact chart type
- Explain why it's appropriate for the specific relationship
- Note any customizations that would enhance clarity
- Suggest tools or libraries best suited for creating it
- Provide tips on interpretation
```

> Note: These are placeholder examples that will be expanded with additional context and variations. 