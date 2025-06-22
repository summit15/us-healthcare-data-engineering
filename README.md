# us-healthcare-data-engineering
# 📌 Project Description
This project involves the development of an end-to-end ETL pipeline to process and prepare US FDA-approved drug product data for analysis and downstream applications. The dataset contains key drug-related information such as product IDs, drug names, dosage forms, administration routes, marketing dates, DEA scheduling, and pharmacological classes.

The main objective is to:

Clean inconsistent or missing entries

Engineer useful features (like drug name, marketing duration)

Normalize fields for storage and future use

Store the output in a structured format like CSV and SQLite

This mimics a real-world data engineering task where the source data is semi-clean but needs refinement for reliability and usability.

# 🔁 ETL Process Details
🟦 1. Extract
Source: Drugs_product.csv uploaded manually.

Tool used: Python (pandas).

The dataset was read using pandas.read_csv().
🟨 2. Transform
Transformation steps involved:

🧹 Data Cleaning
Standardized column names (removed spaces, uppercase).

Removed duplicates.

Converted STARTMARKETINGDATE and ENDMARKETINGDATE to datetime format.

Replaced null or missing values in important fields like DEASCHEDULE, ENDMARKETINGDATE, and PROPRIETARYNAMESUFFIX.

🛠️ Feature Engineering
Full Drug Name: Combined PROPRIETARYNAME + PROPRIETARYNAMESUFFIX.
Marketing Duration: Calculated the duration (in years) since the drug was marketed.
📊 Normalization
Cleaned and normalized manufacturer and labeler names.

Ensured consistent casing and format for PHARM_CLASSES and ROUTENAME.

🟩 3. Load
Cleaned data was stored in two formats:
# Data Source: https://www.kaggle.com/datasets/maheshdadhich/us-healthcare-data?resource=download&select=Drugs_package.csv


