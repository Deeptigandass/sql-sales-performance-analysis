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

![image.png](attachment:74b3ed24-67d2-41ee-9d20-992cda179d09:image.png)

2. 📦 Top-Selling Products (Revenue + Quantity)

![image.png](attachment:a5780470-26d2-4a1f-a5a6-7d5370f0e884:image.png)

3. 👨‍💼 Employee-wise Sales Performance

![image.png](attachment:b6c302c5-9882-4b2f-a696-4f37a79038c7:image.png)

4. 📅 Monthly Sales Trend

![image.png](attachment:12865f69-9698-42c7-8f81-956099044449:image.png)

5. ⚠️ Orders with Missing Billing Info

![image.png](attachment:9e3deba7-ca43-46ab-9891-a32c593b638d:image.png)

6. 👔 Manager-Subordinate Mapping

![image.png](attachment:3b638101-8494-4575-b11c-24fec54da4f3:image.png)

7. 🚚 Shipped Later than Expected (Delayed)

![image.png](attachment:0e540307-23d9-40cb-8ab6-9705d96d60fb:image.png)

### 📊 **Key Insights**

- **Kevin Brown** is both a top customer and a high-performing employee — potential **dual-role anomaly** or test case.
- **Gloves** and **Caps** (Clothing) were most expensive and had high revenue — focus more ads here.
- Multiple orders have **null billing addresses**, which may affect delivery or invoicing — flag these as **data quality issues**.
- Employees like **Michael Ray** generated over **90,000 in sales** — strong candidates for internal incentives.
- Clear peak in sales in **Feb & March 2025** — indicates **seasonal demand spike**.

![image.png](attachment:bd60b652-d686-49f6-b4e5-4aed6f412217:image.png)

### 🎯 **Business Impact**

This case study simulates a **real-world SQL-based business reporting role**, showcasing skills like:

- Writing optimized joins and aggregations
- Identifying anomalies and nulls
- Building executive-friendly KPIs
- Structuring ad hoc data into actionable insights
