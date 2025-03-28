# data-analyst-abdul
# Project 1: Descriptive analysis of Customer Purchase Behaviours
Project Objective: In this project, descriptive analysis of customer purchase data at fictional company called 'Saibi-Retail'. 

The objective is to compile important aspects of consumer purchases, spot patterns, and provide insights that can guide inventory control and marketing plans.

Dataset: The dataset consists 'Saibi-Retail' of transactional data from Saibi World over the past year, containing the following key features:
Transaction ID: Unique identifier for each purchase
Customer ID: Identification number for each customer
Purchase Date: Date and time of the transaction
Age: Age of the customer
Product Category: Category of the purchased product (e.g., electronics, clothing, groceries)
Quantity: Number of items purchased
Price per Unit: Price per individual item
Total Amount: Total price of the transaction

# Methodology
Step 1: Data Ingestion and Preparation
In this step, data ingestion will be done using AWS S3 buckets. For this purpose, 'saibi-retail-raw-abdul' bucket is created to upload the 'Saibi-retail.csv' dataset.
<img width="1418" alt="Screenshot 2025-03-27 at 2 41 16 PM" src="https://github.com/user-attachments/assets/36b2f8af-aef3-4bde-a631-bc46e6d7303d" />

Step 2: Once the dataset is upload in the raw S3 Bucket, the next step is to clean the dataset. There are total of 17 errors that can be encountered in the dataset which can range from missing values to invalued values or it can be related to formatting issues etc.

The AWS service used in this case will be AWS Glue Databrew to clean the dataset, and perform data profiling and cleaning. The content has no data issues but the column names are changed to Camel case with no space in between, which are easier to read.

The job is successful and the outputs are created in 'sab-rtl-trf-abd' S3 Bucket.
<img width="1434" alt="Screenshot 2025-03-27 at 4 38 43 PM" src="https://github.com/user-attachments/assets/ad7f9400-fbb0-481b-a960-32a947d70704" />

User Output:
<img width="1426" alt="Screenshot 2025-03-27 at 4 40 10 PM" src="https://github.com/user-attachments/assets/84040466-c4eb-4c2a-9f9d-0772642774b3" />

System Output: Two outputs were created based on Gender, Male & Female.
<img width="1427" alt="Screenshot 2025-03-27 at 4 41 09 PM" src="https://github.com/user-attachments/assets/7648cecb-fe49-42a9-8f93-866bf9ca2bcb" />

# Trend Analysis
Once the data has been cleaned, we will be using Tableau to conduct our data analysis, starting off with sales trend over the 30 days. As it can be seen that sales start off strong in beginning of the month, then reach thier lowest at the middle of the month, after picking up the pace and going up during the last days of the month.


<img width="749" alt="Screenshot 2025-03-27 at 5 07 22 PM" src="https://github.com/user-attachments/assets/d7b5c827-20b7-4b05-b8d6-e0b10cc4c4b4" />


















