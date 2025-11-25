📊 Sales Performance Dashboard – Power BI

An interactive and dynamic Sales Performance Dashboard built using Power BI, designed to analyze business performance across sales, profit, returns, forecast, customer ranking, and product profitability.

This dashboard includes advanced bookmarks and DAX measures making it a great example of professional Power BI development.

🚀 Key Features

🔹 KPI Summary Cards

Provides a high-level snapshot of overall business performance:

* Total Sales
* Total Profit
* Total Orders
* Return % (calculated using a custom DAX measure)*
* Average Delivery Time



🔄 Bookmark-Based Interactions (Advanced UX)

The dashboard contains multiple bookmark toggles for seamless navigation inside visuals:

📌 Sales & Profit Toggle (Bookmark)

* A line chart allows switching between:

  * Sales by Month
  * Profit by Month

📌 Orders Distribution Toggle

A donut chart with 2 bookmark views:

* Payment Mode Distribution
* Ship Mode Distribution

📌 Sales Distribution by Hierarchy

A bar chart allows switching between:

* Sales by Segment
* Sales by Category
* Sales by Sub-Category

These bookmarks make the dashboard more interactive and reduce page clutter.

---

📈 Visuals Included

1. Profit by Month (with Bookmark Toggle)

* Monthly trend analysis
* Toggle between Sales and Profit views

2. Orders Distribution (%)

* Shows customer order distribution across different classes
* Switch to payment/ship mode using bookmarks

3. Sales Distribution Across States & Regions

* Donut chart for state-wise contribution
* Map visual showing region-wise density

4. Sales by Category / Segment / Subcategory

* Dynamic bar chart
* Switch hierarchy levels using bookmark buttons

5. Top 50 Customer Ranking

* Table showing:

  * Customer Name
  * Country, Region, City
  * Total Sales

6. Upcoming 15-Day Sales Forecast

* Line chart using Power BI’s built-in forecasting
* Confidence intervals
* Slicer for date-based drill-down

7. Product Performance: Sales vs Profit Comparison

* Scatter plot
* Visualizes profitability vs sales
* Category-level legend for easy comparison

8. Global Filters: Region & Year
- Slicers placed at the top of the report
- Allow users to filter the entire dashboard by Region and Year
- Helps in dynamic analysis across visuals


🛠️ DAX Measures Used

Return %
A custom DAX measure created to calculate the percentage of returned orders:
DAX:
Return (%) = 
VAR TotalOrders =
    COUNTROWS(SuperStore_Sales_Dataset)

VAR ReturnedOrders =
    CALCULATE(
        COUNTROWS(SuperStore_Sales_Dataset),
        SuperStore_Sales_Dataset[Returns] = 1
    )
RETURN
if(ISBLANK(ReturnedOrders),0,DIVIDE(ReturnedOrders, TotalOrders, 0))


## 🎯 Business Questions Answered

This dashboard answers:

* Which months perform the best in profit and sales?
* Which product categories or subcategories generate maximum revenue?
* What is the organization’s return percentage?
* How do customers across regions contribute to sales?
* Who are the top-performing customers?
* How will sales look for the next 15 days?
* What is the relationship between sales and profit for each product?



📌 How to Use

1. Download the `.pbix` file.
2. Open in Power BI Desktop.
3. Use bookmarks to switch between:

   * Sales ↔ Profit
   * Payment Mode ↔ Ship Mode
   * Segment ↔ Category ↔ Sub-Category
4. Explore forecast and map visuals for deeper insights.

---

🧑‍💼 About This Project

This dashboard demonstrates professional-level capabilities in:

* DAX
* Forecasting
* UX through bookmarks
* Visual storytelling
* Hierarchy-based insights


