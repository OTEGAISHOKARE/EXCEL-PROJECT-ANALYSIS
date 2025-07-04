# EXCEL-PROJECT-ANALYSIS
Here is the documentation of my first ever project work which I analysed using the microsoft excel.

This project was given to me by the DIGITAL SKILLUP AFRICA where I was taught how to use my Excel, SQL, and Power BI  to analyze and visually represent my findings.

## PROJECT TOPIC: AMAZON PRODUCTS REVIEW

### Project Overview
This Data Analysis project aims to generate insight into the sales performance of Products bought on Amazon. By analysing the various parameters in the data received, I seek to gain enough insight to make reasonable decisions which then enable me to give compelling summarization around the data analyzed and to know which of the products is at the top of our chart.

### Data Source
The primary Data source of the Data used here is Amazon Case study.xls and this is an open source data that was shared by the DSA Facilitators to all Data Analyst under the DSA.

### Tools used
- Ms Exccel for Data cleaning [Download Here](https://www.microsoft.com)
- Pivot table for data visualization

### Data Cleaning and Preparation
In the initial phase of the Data cleaning and preparations, I performed the following actions;
1. Data loading and Inspection
2. Handling missing variables
3. Data cleaning and formatting

### Exploratory Data Analysis
EDA involves the exploring of the Data to answer some questions about the Data such as ;
- What is the Average discount percentage
- Which product have the highest average ratings
- Total number of reviews per category
- Total potential revenue
- Top 5 products in terms of rating

### DATA ANALYSIS
[Amazon case study tega project.xlsx](https://github.com/user-attachments/files/21057672/Amazon.case.study.tega.project.xlsx)

To get the total Average discount of all products, I used the
- Pivot Table:
- Rows: Category
- Values: Discount % → summarize by Average
- https://raw.githubusercontent.com/OTEGAISHOKARE/EXCEL-PROJECT-ANALYSIS/refs/heads/main/IMG_20250703_144006.jpg

 To get the Product with Highest average ratings, I used the
 - Pivot table
 - Column: Average rating (in descending order)

To get Products listed under each category
- Pivot Table:
- Rows: Category
- Values: Product Name → set to Count (Distinct)

Total number of reviews per category
- Pivot Table:
- Rows: Category
- Values: Rating Count (Sum)

Average actual price vs discounted price by category
- Pivot Table:
- Rows: Category
- Values: Actual Price  (Average), Discounted Price (Average)

Which products have the highest number of reviews
- Pivot: Rating Count column  (descending)

How many products have a discount of 50% or more:
calculated column on table
- =IF(Discount % >= 50, "Yes", "No")

Distribution of product ratings
- Pivot Table:
- Rows: Rating 
- Values: Product Name(count).  

Total potential revenue by category (Actual Price × Rating Count)
Calculated column in table
- =Actual Price * Rating Count
- Pivot Table:
- Rows: Category
- Values: Potential Revenue(Sum)

Number of unique products per price range bucket
- Excel formular=IF(Discounted Price < 200, "<₹200",
   IF(Discounted Price <= 500, "₹200–₹500", ">₹500"))

- Pivot Table:
- Rows: Price Bucket
- Values: Product Name(Count)

How does the rating relate to the level of discount
- Excel formular=IF([@Discount%]<=10, "0-10%",
  IF([@Discount%]<=20, "11-20%",
  IF([@Discount%]<=30, "21-30%", ...))

- Pivot Table:
- Rows: Discount Bucket
- Values: Average Rating (Average)

How many products have fewer than 1,000 reviews
Filter Rating Count < 1000

Which categories have products with the highest discounts
- Pivot Table:
- Rows: Category
- Values: Discount % → Max

Top 5 products by rating + number of reviews combined

### Conclusion 
- The total Average discount of all products is 48%

- The sum of Rating count in total is 26,766,379.

- The Highest Average rating is 4.6 ⭐

- The product with the Highest Average rating is the TABLET with 4.6 ratings

- Product Category with the highest review is the ACCESSORIES and PERIPHERALS with a total of 5,079,479 ratings in total

### VISUAL PREVIEW 
![IMG_20250703_142831](https://github.com/user-attachments/assets/131a601e-6a86-4c4f-807e-d776b32a4711)

![IMG_20250703_142919](https://github.com/user-attachments/assets/dc5c4311-7c37-43e1-97b3-e5e73f9cec02)

![IMG_20250703_143030](https://github.com/user-attachments/assets/9c698e7d-cc9a-40a3-a48d-d1c32fcaeac9)

![IMG_20250703_144006](https://github.com/user-attachments/assets/4dbb1415-8dca-4192-8713-681d539978a1)

### REFERENCE
- Excel workbook
- Amazon case study
- DSA Facilitators
