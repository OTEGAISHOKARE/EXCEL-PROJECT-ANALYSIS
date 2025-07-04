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
