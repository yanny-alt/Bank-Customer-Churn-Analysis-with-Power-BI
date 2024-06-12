# Customer Churn Analysis for a Bank

## Overview

**What is Customer Churn?**  
Customer churn, also known as customer attrition, is the rate at which customers leave a business relative to the total number of active customers. Reducing churn is crucial for maintaining a healthy customer base and ensuring business growth.

## Project Objective

This analysis aims to discover various factors contributing to the increased customer churn rate at the bank. These insights will help business users make informed decisions and strategize on how to improve customer retention and reduce churn rates.

## Tools Used

- **Power BI**: For data visualization and reporting.
- **Power Query**: For data transformation and preparation.

## About the Data

- **Source**: Commercial bank
- **Format**: CSV file with 10,000 rows
- **Anonymity**: All personally identifiable information has been removed to protect customer privacy.

### Data Dictionary

- **customer_id**: Unique identifier for each customer.
- **credit_score**: Rating of the customer's creditworthiness.
- **country**: Customer's country of residence.
- **gender**: Gender of the customer (male or female).
- **age**: Customer's age.
- **tenure**: Number of years the customer has been with the bank.
- **balance**: Deductible balance on the customer's bank account.
- **products_number**: Type of bank account the customer has.
- **credit_card**: Indicates if the customer has a credit card (1 for yes, 0 for no).
- **active_member**: Indicates if the account is active (1 for active, 0 for dormant).
- **estimated_salary**: Average annual salary received into the account.
- **churn**: Indicates if the customer has churned (1 for churned, 0 for not churned).

## Analytical Steps

1. **Data Preparation**
   - **Rename**: Changed data table name from `customer_churn_data` to `Customer Data`.
   - **Header Promotion**: Promoted the first row to the header.
   - **Column Removal**: Removed the `estimated_salary` column as it was redundant.
   - **Applied Steps Documentation**: Renamed steps in Power Query for better tracking.

2. **Data Categorization and Grouping**
   - **Labeling**: Replaced values in `products_number` for clarity.
   - **Grouping**: Used conditional column function to group `age`, `credit_score`, and `balance` columns.

3. **Formatting**
   - **Boolean Columns**: Changed values for clarity:
     - `active_member`: 0 = dormant, 1 = active
     - `churn`: 0 = not churned, 1 = churned
     - `credit_card`: 0 = no, 1 = yes

4. **Data Transformation**
   - **Custom Sorting**: Created reference tables for custom sorting.
   - **Renaming Columns**: Ensured all columns had meaningful names.
   - **Data Type Check**: Verified and corrected data types.

5. **Data Modeling**
   - **Relationships**: Established relationships between tables with correct cardinality.

6. **Visualization — Report**
   - Created DAX measures for key metrics:
     - **Customers**: Total number of unique customers.
     - **Customers Churned**: Total number of churned customers.
     - **Churn Rate**: Percentage of customers who have churned.

7. **Insights**
   - **Gender**: Churn rate for male customers is 65% but overall male churn rate is 25%.
   - **Credit Score**: Highest churn rate among those with the lowest credit scores (>400).
   - **Account Balance**: Most churned customers have account balances <=200k.
   - **Age**: High churn rate (56.2%) for customers aged 51-60.
   - **Products**: High churn rate (27.7%) among customers in the Prod 1 group; 100% churn rate for Prod 2 customers with account balances of 1k-10k.

8. **Recommendations**
   - **Target Seniors**: Create products for seniors approaching retirement age.
   - **Incentive Programs**: Offer incentives to long-term customers.
   - **Exclusive Packages**: Provide special packages for customers with high account balances.
   - **Investigate High Churn**: Understand and address 100% churn rate for Prod 2 customers with low account balances.

## Conclusion

This Power BI analysis went through major data analysis processes, from raw data to a comprehensive report. The insights gained provide valuable guidance for the bank to manage customer churn more effectively. Stakeholders can focus on key factors and implement strategies to enhance customer retention.

## Screenshots

### Dashboard Screenshot

![Dashboard Screenshot](link_to_dashboard_screenshot)

## Executive Summary

### Key Insights
- **Churn Rate**: Overall churn rate is 20.4%.
- **High Risk Groups**:
  - Customers aged 51-60.
  - Customers with low credit scores.
  - Customers with high account balances (>200k).

### Business Recommendations
- Implement targeted products and incentives for at-risk groups.
- Explore exclusive packages for high-balance customers.
- Investigate and address high churn rates in specific product groups.

Thank you for reading! Your feedback is appreciated.
