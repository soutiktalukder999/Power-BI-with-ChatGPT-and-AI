# Power-BI with ChatGPT & AI



✅ Project Highlights

🎯 Designed & Developed: Built 2 interactive Power BI reports tailored for actionable business intelligence.

🤖 AI-Assisted Development: Leveraged ChatGPT and AI tools for enhanced data modeling, DAX formula optimization, and visual refinement.

📊 Dynamic Dashboards: Integrated filters, KPIs, and drill-down features to support real-time, strategic decision-making.

⚡ Accelerated Workflow: Improved development speed and accuracy through AI-assisted solutions for technical challenges.

🧩 User-Centric Design: Ensured reports are intuitive, visually engaging, and aligned with business goals.

🔁 Scalability & Reusability: Delivered modular and reusable report structures to support ongoing and future analytics requirements.



🏅 Certification
📜 AI Dashboards using Microsoft Power BI
Certified by Skill Nation
Proof of proficiency in building AI-enhanced Power BI dashboards using real-time data and advanced visualizations.







###   <!-- empty heading or any text creates a gap -->
<!-- SPACE -->
<br><br><br>  <!-- This creates vertical space -->





<img width="596" alt="d" src="https://github.com/user-attachments/assets/0f792b76-c379-4d05-8d66-d7532c73f511" />



# 🛍️ SOUTIK Ecommerce Sales Dashboard

An interactive **Power BI dashboard** that provides deep insights into an ecommerce platform’s sales performance across customers, regions, categories, and payment modes. Designed to empower decision-makers with **data-driven strategies**, this dashboard analyzes performance through various KPIs and visualizations.

![Soutik Ecommerce Dashboard](d.png)

---

## 📌 Table of Contents

- [Overview](#overview)
- [Key Metrics](#key-metrics)
- [Business Insights](#business-insights)
- [Dataset Description](#dataset-description)
- [Visual Breakdown](#visual-breakdown)
- [DAX Measures](#dax-measures)
- [How to Use](#how-to-use)
- [Conclusion](#conclusion)

---

## 🔍 Overview

The **SOUTIK Ecommerce Dashboard** helps visualize sales and operational data across multiple dimensions:

- Track revenue, profit, and quantity sold.
- Identify top-performing customers, product categories, and states.
- Evaluate profit trends over months and sub-categories.
- Understand customer payment preferences.
- Perform time-based filtering via quarter and state slicers.

---

## 📈 Key Metrics

| Metric                          | Value    |
|----------------------------------|----------|
| **Total Revenue (Amount)**       | ₹438,000 |
| **Total Profit**                 | ₹37,000  |
| **Total Quantity Sold**          | 5,615    |
| **Average Order Value (AOV)**    | ₹121,000 |

---

## 📊 Business Insights

### 🔹 Sales & Customers
- **Top Customer:** Hariprash generated the highest sales volume, followed by Madhav and Madan Mohan.
- **High Revenue States:** Maharashtra and Madhya Pradesh lead, indicating a strong customer base in these regions.

### 🔹 Product Category Performance
- **Clothing** dominates with **63%** of total sales quantity.
- **Electronics (21%)** and **Furniture (17%)** are strong secondary categories.
  
### 🔹 Profit Analysis
- **Monthly Trends:** Profits peaked in **January** and **December**, likely due to promotional events or festive seasons.
- **June shows a negative profit**, suggesting higher returns or discount campaigns.

### 🔹 Payment Insights
- **COD (Cash on Delivery)** is the most used mode at **44%**, followed by **UPI (21%)**.
- Indicates the need to promote digital payments like Credit/Debit cards (combined only 25%).

### 🔹 Sub-Category Profitability
- **Printers** and **Bookcases** deliver the highest profitability.
- Low-performing sub-categories can be evaluated for discontinuation or rebranding.

---

## 📂 Dataset Description

### 📁 1. `Orders.csv`
Contains transactional data:
- `OrderID`, `Amount`, `Profit`, `Quantity`
- `PaymentMode`, `CustomerName`, `State`

### 📁 2. `Details.csv`
Contains product metadata:
- `ProductName`, `Category`, `Sub-Category`

---

## 📊 Visual Breakdown

| Visualization                        | Description |
|--------------------------------------|-------------|
| **KPI Cards**                        | Shows total Amount, Profit, Quantity, and AOV |
| **Bar Chart - Amount by Customer**   | Identifies top-spending customers |
| **Donut Chart - Category Breakdown** | Displays share of each product category |
| **Bar Chart - State Revenue**        | Sales distribution by geography |
| **Donut Chart - Payment Mode**       | Customer payment preferences |
| **Bar Chart - Monthly Profit**       | Tracks profit trends across months |
| **Bar Chart - Sub-Category Profit**  | Compares profitability across sub-categories |
| **Slicers: Quarter, State**          | Enables dynamic filtering for time and location |

---

## 💡 DAX Measures (Sample)

```DAX
-- Total Sales Amount
Total Amount = SUM(Orders[Amount])

-- Total Profit
Total Profit = SUM(Orders[Profit])

-- Average Order Value (AOV)
AOV = DIVIDE(SUM(Orders[Amount]), COUNT(Orders[OrderID]))

-- Profit by Month
Monthly Profit = 
CALCULATE(
    SUM(Orders[Profit]),
    ALLEXCEPT(Orders, Orders[Month])
)

-- Quantity Share by Category
Clothing Share % =
DIVIDE(
    CALCULATE(SUM(Orders[Quantity]), Details[Category] = "Clothing"),
    CALCULATE(SUM(Orders[Quantity]))
)
```

---

## 🚀 How to Use

1. Open the `.pbix` file in **Power BI Desktop**.
2. Load the datasets (`Orders.csv` and `Details.csv`) or use Power Query to connect dynamically.
3. Use slicers (State, Quarter) to explore data by region and time.
4. Hover or click on visuals for drill-through insights.

---

## ✅ Conclusion

This dashboard empowers ecommerce stakeholders to:
- Understand performance across multiple dimensions.
- Optimize operations by identifying top regions, products, and customers.
- Make strategic decisions using actual profit trends and customer behavior.

> 🔧 **Customization Tip:** You can enhance this dashboard by integrating return rates, customer lifetime value (CLV), or real-time API data from your ecommerce platform.

---






###   <!-- empty heading or any text creates a gap -->
<!-- SPACE -->
<br><br><br>  <!-- This creates vertical space -->




<img width="602" alt="c" src="https://github.com/user-attachments/assets/4c5d4d3b-165f-4372-9edd-e5d625ede7c4" />




# 💳 Credit Card Financial Dashboard – Power BI Project

## 📊 Summary
This **Credit Card Financial Dashboard** provides an end-to-end analysis of credit card usage, transaction patterns, and revenue generation across customer demographics and behavior. Key metrics like **Revenue (55M)**, **Total Transaction Amount (45M)**, **Interest Earned (7.84M)**, and **Transaction Count (656K)** are displayed via interactive cards and visual elements. Slicers allow filtering by **Quarter**, **Gender**, and **Card Type**, enabling dynamic insights into financial performance and user segmentation.

---

## ✅ Dashboard Highlights

### 📈 Key Visuals
- **KPI Cards**: Display core financial indicators.
- **Revenue vs. Total Transaction Volume (by Quarter)**  
  - Highest Revenue: **Q1 (14M)**
  - Highest Transactions: **Q3 (166.6K)**
- **Revenue by Card Category**
  - Blue: **46M**
  - Silver: **6M**
  - Gold: **2M**
  - Platinum: **1M**
- **Revenue by Job Type**
  - Businessman: **17M**
  - White-collar: **10M**
  - Self-employed / Govt: **8M**
- **Revenue by Expenditure Type**
  - Bills: **14M**, Entertainment: **10M**, Fuel: **9M**
- **Revenue by Chip Use**
  - Swipe: **35M**
  - Chip: **17M**
  - Online: **3M**
- **Revenue by Education**
  - Graduates lead with **22M**

### 📅 Week-over-Week Revenue (WOW)
| Week | Previous Week Revenue | Current Week Revenue | % Change |
|------|------------------------|-----------------------|----------|
| 52   | 1,070,439              | 933,134               | **-12.8%** |
| 51   | 1,026,549              | 1,070,439             | +4.3%     |
| 50   | 980,152                | 1,026,549             | +4.7%     |

---

## 📌 Key Metrics

| Metric                  | Value  |
|-------------------------|--------|
| **Revenue**             | 55M    |
| **Total Trans Amount**  | 45M    |
| **Interest Earned**     | 7.84M  |
| **Total Trans Count**   | 656K   |

---

























