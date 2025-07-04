# **Sales Performance & Customer Insights Dashboard (SQL)**

: SQL Case Study

### 📌 **Project Overview**

As a Business & Data Analyst, I conducted an end-to-end analysis using the `SalesDB` SQL Server database to uncover **customer behavior**, **employee performance**, and **product trends**. The objective was to create actionable insights for improving **sales strategy**, **retention**, and **revenue growth**.

---

### ❓ **Problem Statement**

The leadership team raised concerns about stagnating revenue and unclear performance metrics across products and employees. My goal was to uncover:

- Who are our **most valuable customers**?
- Which **products and employees** drive sales the most?
- Are there **seasonal sales patterns** we can leverage?
- Can **archived orders** reveal additional sales opportunities?

---

### 🧾 **Database Tables Used**

| Table Name | Description |
| --- | --- |
| `Sales.Customers` | Customer information and demographics |
| `Sales.Orders` | Order-level transaction data |
| `Sales.Products` | Product catalog and pricing |
| `Sales.Employees` | Sales staff involved in transactions |
| `Sales.OrdersArchive` | Historical order data |

---

### ❓ **Key Business Questions**

1. Who are the **top 5 customers by revenue**?
2. What are the **top-performing products** by revenue and quantity?
3. Which **employees** generate the highest sales?
4. What is the **monthly sales trend** for the past year?
5. How can we **leverage archived orders** to boost sales?

---

### ⚙️ **Tech Stack**

- **Database**: SQL Server
- **Language**: T-SQL
- **Tools**: SSMS, Notion (for documentation), Excel (for visualization)

---

🔍 **Key SQL Queries**

1. 🧑‍🤝‍🧑 Top Customers by Total Sales

SELECT 
    C.CustomerID,
    C.FirstName + ' ' + ISNULL(C.LastName, '') AS CustomerName,
    SUM(O.Sales) AS TotalSpent
FROM Sales.Customers C
JOIN Sales.Orders O ON C.CustomerID = O.CustomerID
GROUP BY C.CustomerID, C.FirstName, C.LastName
ORDER BY TotalSpent DESC;


2. 📦 Top-Selling Products (Revenue + Quantity)

SELECT 
    P.Product,
    P.Category,
    SUM(O.Quantity) AS TotalUnitsSold,
    SUM(O.Sales) AS TotalRevenue
FROM Sales.Products P
JOIN Sales.Orders O ON P.ProductID = O.ProductID
GROUP BY P.Product, P.Category
ORDER BY TotalRevenue DESC;


3. 👨‍💼 Employee-wise Sales Performance

SELECT 
    E.EmployeeID,
    E.FirstName + ' ' + ISNULL(E.LastName, '') AS EmployeeName,
    SUM(O.Sales) AS TotalSales
FROM Sales.Employees E
JOIN Sales.Orders O ON E.EmployeeID = O.SalesPersonID
GROUP BY E.EmployeeID, E.FirstName, E.LastName
ORDER BY TotalSales DESC;


4. 📅 Monthly Sales Trend

SELECT 
    FORMAT(OrderDate, 'yyyy-MM') AS Month,
    SUM(Sales) AS MonthlyRevenue
FROM Sales.Orders
GROUP BY FORMAT(OrderDate, 'yyyy-MM')
ORDER BY Month;


5. ⚠️ Orders with Missing Billing Info

SELECT * 
FROM Sales.Orders
WHERE BillAddress IS NULL OR Sales IS NULL;


6. 👔 Manager-Subordinate Mapping

SELECT 
    M.FirstName + ' ' + M.LastName AS Manager,
    E.FirstName + ' ' + E.LastName AS Subordinate
FROM Sales.Employees E
JOIN Sales.Employees M ON E.ManagerID = M.EmployeeID;


7. 🚚 Shipped Later than Expected (Delayed)

SELECT 
    OrderID, OrderDate, ShipDate, DATEDIFF(DAY, OrderDate, ShipDate) AS ShippingDelayDays
FROM Sales.Orders
WHERE DATEDIFF(DAY, OrderDate, ShipDate) > 5;


### 📊 **Key Insights**

- **Kevin Brown** is both a top customer and a high-performing employee — potential **dual-role anomaly** or test case.
- **Gloves** and **Caps** (Clothing) were most expensive and had high revenue — focus more ads here.
- Multiple orders have **null billing addresses**, which may affect delivery or invoicing — flag these as **data quality issues**.
- Employees like **Michael Ray** generated over **90,000 in sales** — strong candidates for internal incentives.
- Clear peak in sales in **Feb & March 2025** — indicates **seasonal demand spike**.


### 🎯 **Business Impact**

This case study simulates a **real-world SQL-based business reporting role**, showcasing skills like:

- Writing optimized joins and aggregations
- Identifying anomalies and nulls
- Building executive-friendly KPIs
- Structuring ad hoc data into actionable insights
