# Dashboard Overview

This project features a Fraud Risk Assessment and Transaction Insight Dashboard designed to help organizations monitor, analyze, and manage potential fraud risks within their transaction data.

## Features & Insights
- Fraud Risk Analysis: Visualizes the number of possible frauds per product, highlighting high-risk items such as headphones, laptops, smartphones, tablets, and coffee machines.
- Fraud Rules & Compliance: Displays the proportion of fraud instances based on different fraud rules, such as suspicious dates, bulk quantities, unknown statuses, and zero-price transactions.
- Transaction Trends: Tracks the count of potential frauds over multiple years, helping identify periods with increased risk.
- Product & Fraud Performance: Compares product sales against fraud scores, helping identify products with higher fraud risks.
- Customer Fraud Scoring: Ranks customers based on their fraud scores and incident counts, enabling targeted investigations.
- Transaction Filtering: Allows filtering by date, product type, and method to facilitate detailed analysis.

## Purpose
The dashboard aims to assist financial and compliance teams in identifying, assessing, and mitigating potential fraudulent activities within company transactions, thereby enhancing fraud detection and prevention efforts.

# Fraud Detection Pipeline/Script

## Description:
This project is a Fraud Detection Pipeline for financial transactions. It helps identify potentially fraudulent transactions based on simple business rules. The pipeline:

1. Reads transaction files (CSV or Excel).
2. Cleans and standardizes the data.
3. Applies rules to flag suspicious transactions.
4. Calculates a fraud score for each transaction.
5. Saves the cleaned and scored data for further review.

## Fraud rules used in this project:
1. Transactions before the year 2000 are likely fraudulent.
2. Bulk transactions with more than 500 items are suspicious.
3. Transactions with a price of 0 but marked as "Completed" are suspicious.
4. Transactions with unknown payment methods are suspicious.
5. Transactions with unknown status are suspicious.

## Tech Stack
Python (pandas, numpy, csv, datetime, logging)
SQL Server (using SQLAlchemy for database connections)
dotenv (to store database credentials safely)

## Installation:
1. Clone the repository:
git clone <repository-url>
cd <repository-folder>
2. Install Python packages:
pip install pandas numpy python-dotenv sqlalchemy pyodbc openpyxl
3. Create a .env file with your database settings (Optional):
4. Place your transaction file (CSV or Excel) in the DataSet folder.
5. Run the pipeline:
6. Check the folders created by the pipeline:
- Final_Files/ → Contains cleaned transactions with fraud scores.
- Review_Files/ → Contains columns that may need manual review.