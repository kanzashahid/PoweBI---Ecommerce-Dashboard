# PoweBI---Ecommerce-Dashboard

# Power BI Dashboard: Orders and Details

## Overview
This Power BI dashboard is designed to provide a comprehensive analysis of order data using two key files: **Orders** and **Details**. The dashboard offers insights into key performance indicators (KPIs) such as sales amount, quantity, profit, and customer performance, along with time-based and geographic segmentation. The dashboard features drill-down capabilities and filters for enhanced data exploration and reporting flexibility.

## Data Sources
1. **Orders**: Contains information related to customer orders.
2. **Details**: Contains detailed breakdowns of each order, including individual items, quantities, and profits.

## KPIs
The following key performance indicators (KPIs) are available in the dashboard:

1. **Sum of Amount**: Total sales amount from all orders.
2. **Sum of Quantity**: Total quantity of items sold across all orders.
3. **Sum of Profit**: Total profit generated from all orders.
4. **Sum of AOV**: Average Order Value (AOV) is calculated by dividing the total sales amount by the number of orders.
5. **Sum of Amount by State**: Total sales amount segmented by the state where the order was placed.
6. **Sum of Amount by CustomerName**: Total sales amount attributed to each individual customer.

## Time Segmentation
The dashboard includes quarter-wise breakdowns of the KPIs to analyze the data over time:

- **Q1 (Jan-Mar)**
- **Q2 (Apr-Jun)**
- **Q3 (Jul-Sep)**
- **Q4 (Oct-Dec)**

Each quarter's performance is visualized for quick comparison and tracking of sales trends over the year.

## Filters
The following filters are available in the dashboard for a more focused analysis:
- **State**: Filter data by the state where orders were placed.
- **Customer Name**: Filter data to analyze performance by individual customers.
- **Date Range**: Filter orders based on specific time periods.
- **Product Category**: Filter by categories of items sold.
- **Order Status**: Filter by completed, pending, or canceled orders.

## Drill-Down Functionality
The dashboard provides drill-down functionality to allow users to explore data at multiple levels of granularity:
- From **Year** to **Quarter** to **Month** to **Day**.
- From **State** to **City** to **Customer**.

## DAX Calculations
The KPIs and advanced calculations are powered by DAX (Data Analysis Expressions). Key DAX measures include:

1. **Total Amount**:
    ```DAX
    Total Amount = SUM(Orders[Amount])
    ```

2. **Total Quantity**:
    ```DAX
    Total Quantity = SUM(Details[Quantity])
    ```

3. **Total Profit**:
    ```DAX
    Total Profit = SUM(Details[Profit])
    ```

4. **Average Order Value (AOV)**:
    ```DAX
    AOV = DIVIDE(SUM(Orders[Amount]), COUNT(Orders[OrderID]))
    ```

5. **Amount by State**:
    ```DAX
    Amount by State = SUMX(Orders, Orders[Amount])
    ```

6. **Amount by Customer Name**:
    ```DAX
    Amount by Customer = SUMX(Orders, Orders[Amount])
    ```

## How to Use the Dashboard
1. **View KPIs**: Start by viewing the KPIs to get an overview of sales performance, quantity, and profit.
2. **Use Filters**: Apply filters (e.g., by State or Customer Name) to focus on specific segments of data.
3. **Drill Down**: Use the drill-down feature to explore data at more granular levels (e.g., from Year to Quarter to Month).
4. **Analyze Trends**: View quarter-wise trends to understand how performance changes over time.
5. **Export**: Export visualizations and reports as needed for presentations or further analysis.

---

This Power BI dashboard provides a flexible, interactive way to monitor and analyze order data, empowering users to make data-driven decisions.
