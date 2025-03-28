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

# Regression Analysis
In this step, the Regression analysis will be done on Price per Unit and Total Amount of Sales. The Linear trend line is used for which we will interpret if that the variables are significant or not. The intercept and the coefficient are both statistically significant. It can be stated with confidence that Price per Unit has a large impact on Total Amount because the p-value is far below 0.05. Statistical significance is confirmed because the t-value is greater than 2.

Although at a slower rate, sales rise as prices rise. According to the logarithmic model, price increases have a greater impact at lower price points but diminish as prices rise. Given its importance, the model can be applied to pricing strategies, assisting Saibi Retail in forecasting sales at various price points.

<img width="1240" alt="Screenshot 2025-03-27 at 5 27 30 PM" src="https://github.com/user-attachments/assets/d85628b2-95a3-4292-995b-01b7f921e684" />

# Root Cause Analysis
In this step, qualitative analysis is done by conducting interviews from Store managers, following insights were obtained:
The following findings were derived from staff and store managers' interviews:

Consumer Behavior: Consumers are being increasingly price conscious, particularly when it comes to expensive product categories like luxury goods and technology.
Inventory Issues: Reduced sales may have led to frequent shortages and delayed refilling in crucial areas.
Influence of Competitors: Due to superior offers, customers are moving online marketplaces and comparing pricing.
Seasonal Trends: In line with noted transaction patterns, sales sharply decline after the holidays.

'The 5 Why's' Analysis:
- What caused the drop in sales? => Consumers are buying fewer expensive goods.
- Why do consumers shun expensive products? →  Prices went up from the previous year.
- Why did prices go up? => Product pricing was impacted by inflation and supplier costs.
- Why did supplier costs rise? Due to supply chain interruptions and market shortages.
- Why are there shortages in the market? → Supply constraints and global economic instability.

# Segmentation Analysis
When customers' purchase habits are broken down by gender, the segmentation analysis shows clear patterns:
 
Female Clients:
- The clothing goods category accounted for the majority of sales from female consumers.
- The overall sales, which exceeded $80,000, were considerably greater due to the contribution of female clients.
- This implies that women are more likely to make fashion-related purchases and that they may do so more frequently or with greater transaction values.

Male Clients:
- The Electronics product category was primarily preferred by male consumers.
- Male client sales were little over $80,000, suggesting a close but marginally smaller contribution to total sales than that of female consumers.

<img width="1229" alt="Screenshot 2025-03-27 at 5 45 32 PM" src="https://github.com/user-attachments/assets/cb7f0824-c04b-4566-a84b-6b5694f9ba41" />

These results demonstrate that although both market sectors make a substantial contribution to total sales, female consumers appear to have a more extensive and sophisticated buying habit, especially when it comes to apparel.  On the other hand, although they spend less overall, male consumers exhibit a considerable interest in technology.  Based on these results, additional segment-specific marketing and inventory strategies can be created, emphasizing product preferences to increase engagement and sales.

# Final Dashboard

After the descriptive analysis has been done, following dashboard will be used to present findings and insights to our stakeholders.

<img width="997" alt="Screenshot 2025-03-27 at 6 12 16 PM" src="https://github.com/user-attachments/assets/ac8ed857-cea7-49a0-bf73-2cbd98b45e83" />

# Key Insights and Recommendations
Based on the data analysis and patterns uncovered, following recommendations are proposed to ensure that Saibi Retail is on the right track:

Modify Pricing Strategies: Consider reassessing prices for important product categories to better meet consumer demands, particularly for those that are in high demand. Providing more flexible pricing might address the drop in sales .
Optimize Inventory Management: Close inventory gaps by enhancing forecasting and stock monitoring systems, especially for high-turnover items like electronics and apparel.
Increase Customer Engagement with Promotions: Develop more alluring offers for infrequent purchasers and customize promotional campaigns to target particular customer segments (e.g., frequent promotions for female customers in clothes).





























