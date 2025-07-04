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

![Screenshot 2025-07-04 121430](https://github.com/user-attachments/assets/53a27043-3e1f-4481-be1e-4c8214b1adc2)




2. 📦 Top-Selling Products (Revenue + Quantity)

![Screenshot 2025-07-04 121516](https://github.com/user-attachments/assets/e589b6fa-994a-4d73-8937-1ea21e11e8ee)



3. 👨‍💼 Employee-wise Sales Performance

![Screenshot 2025-07-04 121814](https://github.com/user-attachments/assets/b5297ff7-d501-4fca-9b95-33c65758bb59)






4. 📅 Monthly Sales Trend

![Screenshot 2025-07-04 121620](https://github.com/user-attachments/assets/463c1373-1aff-48cf-a0ec-b8b0cb0b8885)



5. ⚠️ Orders with Missing Billing Info

![Screenshot 2025-07-04 121706](https://github.com/user-attachments/assets/44173fa1-4f08-432e-9843-539031043408)


6. 👔 Manager-Subordinate Mapping

![Screenshot 2025-07-04 121931](https://github.com/user-attachments/assets/bfcdab5d-8259-4f7d-a744-1477e77a8ea3)


7. 🚚 Shipped Later than Expected (Delayed)

![Screenshot 2025-07-04 122032](https://github.com/user-attachments/assets/6f880e22-f9d0-476a-a212-530123291839)




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
