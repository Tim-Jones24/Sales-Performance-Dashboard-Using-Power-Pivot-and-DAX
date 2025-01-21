# Sales Performance Dashboard Using Power-Pivot and DAX
This project involves an interactive and insightful sales performance dashboard by integrating data from Excel files and an MSSQL database.

### Overview
This project demonstrates the creation of a sales performance dashboard leveraging Power Pivot in Excel,DAX calculations, and a star schema data model. The dashboard provides actionable insigts into sales trends, regional performance, sales team efficiency, and product demand.
Key features incude:
* Integration of sales,product,geography,and personnel dat into a unified data model.
* DAX-based calculations for total sales, total transactions, and key performance indicators.
* Visualization of insights such as monthly sales trends, regional sales performance, sales team rankings, and product demand.
* Slicers for interactive filtering by year, region and sales team to tailor views for stakeholders.

#### Data Sources
1. **Excel Files:**
   * Sales data
   * Products data
2.  **MSSQL Database:**
   * Geo data
   * People data
3. **Derived Table:**
     * Calendar Table (using Power Pivot in Excel)
    
#### Data Model
The data is organized into star schema, consisting of:
* **Fact Table:**
  * Sales
* **Dimension Tables:**
  * Products
  * Calendar
  * Geo
  * People

#### Schema Modifications:
* Renamed "Geo" to **Geo ID** in the Sales table.
* Renamed "Sales Person" to **SP_ID** in the Sales table.

#### DAX Measures
1. **Total Amount:** SUM(sales[Amount])
2. **Total Customers:** SUM(sales[Customers])
3. **Total Boxes:** SUM(sales[Boxes])
4. **Total Transactions:** COUNTROWS(sales)
5. **Total Boxes Per Transaction:** ROUND( [Total Boxes] / [Total Transactions],0)
6. **Amount Per Transaction:** ROUND(DIVIDE[Total Amount],[Total Transaction],2)

#### Summary of Key Records:
* Total Amount: $43,561,546
* Total Customers: 1,232,947
* Total Boxes: 2,901,311
* Total Boxes Per Transaction: 381
* Amount Per Transaction: $5,718.99
* Total Transactions: 7,617
* Total Products: 17

#### Insights Derived
1. **Monthly Sales(2021 & 2022)**: Tracked and visualized trends across two years.
2. **Regional Sales Performance**: Calculated average sales across regions.
3. **Top 3 Countries by Demand**: identified the countries with the highest quantities of boxes sold.
4. **Sales Leaderboard**: Highlighted the top 5 sales representatives based on sales amounts.
5. **Top Product Demand**: Ranked the top 3 products by quantity sold.
6. **Sales Team Performance**:
   * Analyzed average sales for the 4 sales teams: **Yummies, Delish, Judies, and N/A**

#### Interactive Dashboard Features
* **Slicers**:
  * **Year:** 2021, 2022
  * **Region:** America,APAC,Europe
  * **Sales Team:** Delish, Jucies,N/A, Yummies
  * **Excel Cube Value Functions:** Connected KPI's to slicers for dynamic and interactive filtering.

#### Technologies Used
* **Excel:** (Power Pivot, DAX, Cube Functions, Pivot Table)
* **MSSQL Database**

  #### Recommendations
  1. **Regional Optimization:**
     * More investment should be tailored to regions with higher average sales (APAC or America) while exploring startegies to bosst Europe performance.
  2. **Product Demand Forecasting:**
     * Focus production and marketing efforts on the top three products to align with customer demand. 
  3. **Sales Team Development:**
     * Provide targeted training to underperforming sales teams.
  4. **Customer Retention Campaigns:**
     * Leverage insights from top regions and products to design targeted loyalty programs for high-value customers.
  5. **Digital Marketing Alignment:**
     * Use the insights on top-performing products and regions to tailor digital campaigns,ensuring ads are geo-targeted and product-specific.

#### Conclusion
This project showcases the power of Excel tools in driving sales and marketing strategies by leveraging **Power Pivot** for data extraction and modelling, **DAX** for deriving actionable insights, and **Pivot Tables** for quick, real-time analysis. The integration of datasets into start schema enabled efficient modelling, while interactive dashboards and slicers provides stakeholders with dynamic insights into sales performance, regional trends, product demand, and team efficiency.
These tools combined to deliver a robust, user-friendly solution for data-driven decision-making.
