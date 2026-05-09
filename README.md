# E-commerce-Data-Cleaning-and-Data-Modelling
This project involves cleaning and transforming e-commerce data in Power BI using Power Query, addressing issues such as missing values, incorrect data types, duplicates, and inconsistent formatting. The data was then structured into a star schema by defining fact and dimension tables and establishing proper relationships.
## Objectives
- **Data Cleaning** – Ensure data accuracy, consistency, and completeness by handling null values, correcting data types, removing duplicates, and standardizing formats.
- **Data Modelling** – Build an optimized star schema with well-defined relationships to support efficient analysis and reporting.
## Power BI File
Data Cleaning and Data Modelling: https://drive.google.com/drive/folders/1zfPPAqUSu3Qm0mRefUBoPMmtse37PcWj?usp=drive_link

## Data Cleaning Process
Data cleaning was performed using Power Query in Power BI to ensure consistency, accuracy, and usability of the dataset.
<img width="1888" height="958" alt="Screenshot 2026-05-09 153340" src="https://github.com/user-attachments/assets/72ea15b7-1caa-43fb-b19e-51e8e8c159be" />
### 1. Removing Unnecessary Columns
The process began by eliminating irrelevant and unused columns. This step reduces data volume, minimizes noise, and improves overall model performance.
### 2. Fixing Data Types
Each column’s data type was reviewed and corrected to ensure compatibility with calculations and relationships.
- Date formats were corrected using the **Advanced Editor**.
- **Change Type with Locale** was applied to properly interpret regional date formats and avoid misclassification.
### 3. Standardizing Text Data
Text fields were cleaned and standardized to ensure consistency across the dataset.
- Leading and trailing spaces were removed using the Trim function.
- Text formatting was standardized (uppercase, lowercase, proper case).
- Inconsistent values were corrected (e.g., “Book’s” was replaced with “Books”) to prevent duplication in analysis.
### 4. Handling Null Values
Missing values were handled based on the context of the data.
- Care was taken to avoid introducing inaccurate assumptions when addressing null values.
### 5. Merging Columns
Columns such as first name and last name were merged into a single Full Name field to improve readability and usability in reports.
### 6. Removing Duplicates
Duplicate records were identified and removed to maintain data integrity, particularly for key fields.

## Data Modelling Process
Following data cleaning, the dataset was structured into an optimized model to support efficient analysis.
<img width="1060" height="645" alt="Screenshot 2026-05-09 154314" src="https://github.com/user-attachments/assets/32f22699-d6c3-4fe7-8ebf-9d86a7f86488" />
### 1. Star Schema Design
A star schema approach was implemented to enhance performance and simplify reporting.
- The **Fact Orders table** serves as the central transactional table.
- Dimension tables include Customers, Products, Sellers, Payment Mode, Delivery Status, Reviews, and Calendar.
### 2. Defining Relationships and Cardinality
Relationships between tables were established based on data structure and business logic.
- One-to-Many (1:M) relationships were primarily used (e.g., one customer to multiple orders).
### 3. Creating Relationships in Power BI
Relationships were created and validated using multiple methods:
- Auto-detect for initial suggestions
- Drag-and-drop for manual linking
- Edit Relationship settings to configure cardinality and filter direction
### 4. Active vs Inactive Relationships
Both active and inactive relationships were managed within the model:
- Active relationships are used by default in analysis
- Inactive relationships can be activated using DAX for specific scenarios.
### 5. Calendar Table Creation
A dedicated calendar table was created to enable time-based analysis.
- The date range was derived from the minimum and maximum order dates in the fact table
- This supports time intelligence calculations such as monthly trends, yearly comparisons, and period analysis

## Summary
This project provided a comprehensive, hands-on experience in data cleaning and data modeling using Power BI, reinforcing both technical skills and best practices in building reliable analytical datasets.
#### Data Cleaning Learnings:
- Learned how to prepare raw data for analysis by removing unnecessary and irrelevant columns to improve performance and clarity.
- Gained experience in identifying and correcting incorrect data types, especially for date fields using Advanced Editor and Locale settings.
- Understood the importance of standardizing text data using Trim, case formatting (uppercase/lowercase/capitalize), and value replacement to ensure consistency.
- Developed the ability to handle missing values appropriately depending on data context and business logic.
- Learned how to merge related columns (e.g., full name creation) to improve usability and readability in reporting.
- Strengthened data integrity by removing duplicate records and ensuring uniqueness in key fields.
#### Data Modeling Learnings:
- Gained a clear understanding of the star schema and how it improves performance and simplifies reporting structures.
- Learned how to properly identify and separate fact tables (transactions) and dimension tables (descriptive entities).
- Developed the ability to define and manage relationships between tables using correct cardinality (one-to-one, one-to-many, many-to-many).
- earned different methods of creating relationships in Power BI, including auto-detect, manual drag-and-drop, and relationship editing.
- Understood the importance of active vs inactive relationships and how inactive relationships can be activated using DAX when needed.
- Learned how to design and implement a calendar table to support time intelligence functions such as monthly, quarterly, and yearly analysis.
