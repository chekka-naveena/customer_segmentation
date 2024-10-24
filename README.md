# Customer Segmentation Analysis

---

# Overview

This document outlines the comprehensive data cleaning process applied to the customer, products, regions, and transactions datasets. The cleaning procedures were executed in Power BI using the Power Query Editor to ensure that the data is uniform, consistent, and accurate.

---

## Datasets
- *Customer Dataset*
- *Products Dataset*
- *Regions Dataset*
- *Transactions Dataset*

---

## 1. Customer Dataset 

*Columns:* CustomerID, Email, updated_phone_number, City, State, Country, Gender, Age, Updated_Joined_date, updated_last_purchase_date, TotalSpent, LoyaltyPoints, PurchaseFrequency, CustomerSegment, PreferredPaymentMethod, MaritalStatus, Updated_Account_creation_date, AccountStatus, LastUpdated, Updated_Referrer_Id, FeedbackRating, Domain of mail, country_code.

### Cleaning Steps
1. *Import Data:* Loaded the dataset into Power BI through Get Data > Text/CSV.
2. *Extract Email Domains:* Filtered the Email column to exclude invalid domains.
3. *Standardize Phone Numbers:* Formatted the phone numbers  (e.g., +1-123-456-7890).
4. *Handle Missing Values:* Addressed missing values logically, either by filling or imputing.
5. *Correct Data Types:* Ensured that each column had the appropriate data type (e.g., Date, Number, Text).
6. *Format Zipcode:*Ensured the zipcode is in text hence the zipcode can also start from zero and replaced null and black spaces with "00000".
7. *Standardize Date Formats:* Applied uniform date formatting across all relevant columns.
8. *Filling missing values :* Filled the missing values in gender,customersegment,matirak ststus paymentmethod and in some other colums like loyaltypoints with appropriate methods like replacing with 0 or unknown or with the column median or average.

---

## 2. Product Dataset
*Columns:* ProductID, ProductName, Category, Price, StockStatus, Supplier, Updated_Price, Updated_StockStatus, LastUpdated, etc.

### Cleaning Steps
1. *Remove Duplicates:* Checked  and removed duplicate entries based on ProductID.
2. *Handle Missing Values:* Imputed missing values for Price and StockStatus as needed and also in productname and category when it is null to unknown.
3. *Correct Data Types:* Verified that Price is a number and ProductName is text.
4. *Format the data:* Captilize the starting letter and trimmed the spaces if needed in colums like productname and category.

---

## 3. Regions Dataset 

*Columns:* RegionID, RegionName,Managername, Country, State,Sales,Totalcustomers, LastUpdated, CountryCode.

### Cleaning Steps
1. *Handle Missing Values:* Addressed missing region or country data using median or average.
2. *Correct Data Types:* Ensured text formatting for RegionName and number formatting for CountryCode and other columns.
  
---

## 4. Transactions Dataset

*Columns:* TransactionID, CustomerID, ProductID, TransactionDate, Quantity, TotalAmount, PaymentMethod, DiscountApplied, LastUpdated.

### Cleaning Steps
1. *Remove Duplicates:* Ensured that TransactionID is unique and removed any duplicates.
2. *Handle Missing Data:* Imputed or removed missing entries for Quantity and TotalAmount.
3. *Correct Data Types:* Applied appropriate data types, ensuring TransactionDate is in a date format and TotalAmount is a number.
4. *Standardize Payment Methods:* Ensured uniformity in the PaymentMethod column (e.g., Credit Card, PayPal)and fillling null values with not specified .
5. *Update Discounts:* Checked for consistent values in the DiscountApplied column.

---

## Conclusion

"The datasets have undergone a comprehensive cleaning and standardization process. They now feature consistent, error-free, and well-structured data, ensuring readiness for advanced analysis and reporting in Power BI. The transformation ensures data integrity and enhances reliability, allowing for efficient and accurate insights generation."

