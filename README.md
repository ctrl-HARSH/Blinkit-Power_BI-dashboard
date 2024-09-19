Blinkit Power_Bi Dashboard

Problem Statement:
The Blinkit Power_Bi dashboard is designed to provide a detailed analysis of sales performance, outlet efficiency, and customer satisfaction across various regions and product categories. 
By analyzing the data, stakeholders can gain valuable insights into the following:

What contributes the most to total sales in terms of fat content, outlet type, and location tier?
Which outlets perform better based on size and establishment year?
How do product sales and customer ratings vary across different outlet types and product categories?
Which locations (T1, T2, T3 cities) offer the most revenue potential for expansion?
The dashboard's insights enable stakeholders to make data-driven decisions to optimize product placement, promotions, and resource allocation.

Steps to Import Data from Excel to Power BI

Step 1: Open Power BI Desktop
Launch Power BI Desktop to load the data and create the visualizations.

Step 2: Import Data from Excel
Click on the Home tab.
Select Get Data > Excel.
Browse and select the Excel file containing the sales data.
Choose the relevant sheet and click Load.

Step 3: Data Cleansing
Once the data is imported, follow these data cleansing steps to ensure accuracy:
Remove duplicates: Ensure there are no duplicate entries in the dataset.
Fix data types: Confirm that columns like sales figures, ratings, and item counts are formatted correctly (currency, decimal, whole numbers).
Handle missing values: Use techniques like replacing missing values with averages or leaving them blank if non-critical.
Create calculated columns: Add calculated fields, such as total sales, item visibility, and average ratings.
Rename columns: Use descriptive names for columns to improve readability and understanding of the data.

Step 4: Create Metrics for the Matrix Visualization
To create the matrix visualization, define the metrics you want to display. Use the following code snippet to define key performance metrics:
DAX
Metrics = {
    ("Total Sales", NAMEOF('BlinkIT Grocery Data'[Total Sales]), 0),
    ("Avg Sales", NAMEOF('BlinkIT Grocery Data'[Avg Sales]), 1),
    ("No of items", NAMEOF('BlinkIT Grocery Data'[No of items]), 2),
    ("Avg Rating", NAMEOF('BlinkIT Grocery Data'[Avg Rating]), 3)
}

Instructions to Create the Matrix:
Navigate to the Visualizations pane.
Select the Matrix chart option.
In the Rows section, add the categories you want to analyze (e.g., Outlet Type, Item Type, Tier Location).
In the Values section, insert the metrics you created using the above DAX code: Total Sales, Avg Sales, No of Items, Avg Rating.
Format the matrix with colors, fonts, and layouts to make it more readable and informative.
The matrix will now display how each category (such as outlet type, item type, or location) performs in relation to the metrics like total sales, average sales, number of items sold, and average ratings.

Charts and Visualizations

1. Donut Chart: Sales by Fat Content
Purpose: Displays the distribution of total sales between products with low-fat and regular-fat content.
Data:
Low Fat: $425.36K
Regular: $776.32K
Total Sales: $1.20M
Insight: Regular fat products contribute the most to overall sales, accounting for 64.6%.

2. Clustered Bar Chart: Item Fat Content vs. Outlet Location Type
Purpose: This chart shows the relationship between product fat content (Low Fat vs. Regular) and outlet location, categorized by city tiers (T1, T2, T3).
Data:
Low Fat and Regular sales across T1, T2, and T3 locations.
Insight: Identifies which tier locations perform better in selling products with different fat contents.

3. Stacked Bar Chart: Item Type vs. Metrics
Purpose: This chart compares various item types against key metrics:
Total Sales
Average Sales
Number of Items Sold
Average Rating
Insight: Helps identify high-performing product categories in terms of revenue and customer satisfaction.

4. Line Chart: Outlet Establishment Year vs. Total Sales
Purpose: This line chart tracks total sales over time, categorized by the establishment year of each outlet.
Data:
X-axis: Year of establishment (2011–2022)
Y-axis: Total sales
Insight: Provides trends showing how sales have evolved over time and which years have been the most successful.

5. Donut Chart: Outlet Size vs. Total Sales
Purpose: This chart breaks down sales by outlet size (small, medium, large).
Data:
Small Outlet Sales: $444.79K
Medium Outlet Sales: $507.90K
Large Outlet Sales: $248.99K
Insight: Medium-sized outlets account for the highest sales, followed by small outlets.

6. Funnel Chart: Sum of Sales by Outlet Location (Tier-based)
Purpose: The funnel visualizes total sales across different city tiers (T1, T2, T3).
Data:
Tier 1 Cities: $336.40K
Tier 2 Cities: $393.15K
Tier 3 Cities: $472.13K
Insight: Tier 3 cities outperform Tier 1 and Tier 2 cities in terms of total sales.

7. Slicer: Outlet Type vs. Key Metrics
Purpose: The slicer filters the data by outlet type to display key metrics like total sales, average sales, number of items, average rating, and item visibility for:
Supermarket Type 1
Supermarket Type 2
Supermarket Type 3
Grocery Store
Data:
Supermarket Type 1: ($788K, 5577 items, 4 avg rating, $141 avg sales, 0.06 visibility)
Supermarket Type 2: ($131K, 928 items, 4 avg rating, $142 avg sales, 0.06 visibility)
Supermarket Type 3: ($131K, 935 items, 4 avg rating, $140 avg sales, 0.06 visibility)
Grocery Store: ($152K, 1083 items, 4 avg rating, $140 avg sales, 0.10 visibility)
Insight: This slicer allows stakeholders to compare different outlet types and assess their performance based on sales and customer satisfaction metrics.
By using these visualizations, metrics, and data points, the Blinkit Power_Bi dashboard offers a complete overview of sales performance, customer preferences, and outlet success, enabling stakeholders to make well-informed business decisions.
