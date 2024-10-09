# Restaurant-Sales-report-EDA-and-Analysis
This notebook thoroughly analyzes and visualizes the Restaurant Sales Report and find the hidden insights and patten in it


## Summary of the Restaurant Sales Data Analysis
### Dataset Overview:
1. File Format: CSV
2. Columns: Order_Id, Date, Item_Name, Item_Type, Item_Price, Quantity, Transaction_Amount, Transaction_Type, Received_By, and Time_Of_Sale
3. Data Size: 1000 rows and 10 columns
4. Special Notes: 'transaction_amount' is calculated as item_price * quantity
### Data Description:
1. Captures sales transactions from a local restaurant
2. Includes food and beverage details, prices, quantities, payment types, and transaction times
3. Transactions categorized by payment type, gender of staff, and time of the sale
### Data Quality:
1. No duplicates in the dataset
2. 107 missing values in the transaction_type column
3. Columns:
1. Numerical Columns: order_id, item_price, quantity, transaction_amount
2. Categorical Columns: item_name, item_type, transaction_type, received_by, time_of_sale
3. Date Column: date
### Measures of Central Tendency:
1. Means: item_price (33.32), quantity (8.16), transaction_amount (275.23)
2. Medians: item_price (25.0), quantity (8.0), transaction_amount (240.0)
3. Modes: item_price (20), quantity (13), transaction_amount (300), item_name ('Cold coffee'), item_type ('Fastfood'), transaction_type ('Cash'), received_by ('Mr.'), time_of_sale ('Afternoon' and 'Night')
### Measures of Dispersion:
1. Ranges: item_price (40), quantity (14), transaction_amount (880)
2. Variances: item_price (222.66), quantity (19.48), transaction_amount (41780.58)
3. Standard Deviations: item_price (14.92), quantity (4.41), transaction_amount (204.40)
4. Skewness & Kurtosis:
1. Skewness: item_price (0.63), quantity (-0.05), transaction_amount (1.05)
2. Kurtosis: item_price (-1.17), quantity (-1.24), transaction_amount (0.66)
### Unique Value Percentages:
1. item_name: Cold coffee (16.1%)
2. item_type: Fastfood (68.6%)
3. transaction_type: Cash (53.3%)
4. received_by: Mr. (51.2%)
5. time_of_sale: Night and Afternoon (20.5% each)
### Correlations:
1. Strong Positive Correlation: quantity and transaction_amount (0.73), item_price and transaction_amount (0.64)
2. Slight Positive Correlation: order_id with item_price, quantity, and transaction_amount, item_price with quantity
### Insights:
1. Cold coffee is the most popular item
2. Fast food is more frequently ordered than beverages
3. Customers prefer paying in cash slightly more than online payments
4. Male staff handle more transactions
5. Peak transaction times are in the afternoon and night

### Based on the statistical analysis:
1. Normality Check:  
The Shapiro-Wilk test indicated that transaction amounts were not normally distributed across all variables tested (item names, time of sales, receiver, transaction type).
2. ANOVA Testing:  
ANOVA was used to compare transaction amounts across different item names, times of sales, receivers, and transaction types. Significant differences were found in transaction amounts between different item names, times of sales, and transaction types.
Levene's test confirmed equal variances for most comparisons, ensuring the validity of ANOVA results.
3. Post hoc Testing:  
Pairwise Tukey HSD tests were employed to determine specific differences between groups where ANOVA indicated significance.
4. Chi-Square Tests:  
Chi-square tests were used to assess the independence between categorical variables (item names vs. time of sales, transaction type, and receiver). Results indicated that item names were not equally distributed across transaction types, while they were independent of both time of sales and receiver.
### Insights:
1. Item Name vs. Transaction Amount: Cold coffee, sandwich, and sugarcane juice had significantly different transaction amounts compared to other items.
2. Time of Sales vs. Transaction Amount: Transaction amounts did not significantly differ across different times of sales.
3. Transaction Type vs. Transaction Amount: There was no significant difference in transaction amounts between cash and online transactions.
4. Receiver vs. Transaction Amount: Transaction amounts did not significantly differ between transactions received by Mr. and Mrs.

