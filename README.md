# ⚡ Power BI with ChatGPT & AI

<div align="center">

<img src="https://img.shields.io/badge/Power%20BI-Analytics-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
<img src="https://img.shields.io/badge/ChatGPT-AI%20Assisted-412991?style=for-the-badge&logo=openai&logoColor=white" />
<img src="https://img.shields.io/badge/DAX-Data%20Modeling-00A4EF?style=for-the-badge" />
<img src="https://img.shields.io/badge/SQL-Data-336791?style=for-the-badge&logo=postgresql&logoColor=white" />

<br><br>

**AI-assisted Business Intelligence • Interactive Dashboards • Data Storytelling**

</div>

---

## 🚀 Project Overview

**Power BI with ChatGPT & AI** is a business intelligence project focused on building interactive, decision-oriented dashboards using **Microsoft Power BI**, supported by **ChatGPT and AI-assisted development workflows**.

The project demonstrates how AI can accelerate:

* 📊 Data analysis
* 🧩 Data modeling
* 🧮 DAX development
* 🎨 Dashboard design
* 🔍 Business insight generation
* ⚡ Troubleshooting and optimization

Two interactive Power BI dashboards were developed as part of this project:

1. 🛍️ **SOUTIK Ecommerce Sales Dashboard**
2. 💳 **Credit Card Financial Dashboard**

---

# 🎯 Project Highlights

| Area                     | Implementation                     |
| ------------------------ | ---------------------------------- |
| 📊 Business Intelligence | Interactive Power BI dashboards    |
| 🤖 AI Assistance         | ChatGPT-assisted development       |
| 🧮 DAX                   | Measures, calculations & KPI logic |
| 🎨 Visualization         | Interactive charts, KPIs & slicers |
| 🔍 Analytics             | Business and financial insights    |
| ⚡ Productivity           | AI-assisted troubleshooting        |
| ♻️ Reusability           | Modular dashboard structures       |
| 📈 Decision Support      | Data-driven business analysis      |

### 🤖 AI-Assisted Development

ChatGPT and AI tools were used throughout the development workflow to assist with:

* DAX formula creation and optimization
* Data modeling approaches
* Power BI troubleshooting
* Visualization selection
* Dashboard layout refinement
* Analytical reasoning
* Technical problem solving

> **AI was used as a development accelerator — while business logic, dashboard design and analytical interpretation remained part of the implementation process.**

---

# 🛍️ Dashboard 01 — SOUTIK Ecommerce Sales Dashboard

An interactive **Power BI ecommerce analytics dashboard** designed to analyze sales performance across customers, regions, categories, payment methods and product sub-categories.

### 📸 Dashboard Preview

![SOUTIK Ecommerce Dashboard](https://github.com/user-attachments/assets/0f792b76-c379-4d05-8d66-d7532c73f511)

---

## 📌 Dashboard Objectives

The dashboard helps stakeholders:

* Track revenue and profitability
* Monitor quantity sold
* Identify high-value customers
* Analyze regional performance
* Understand category demand
* Evaluate payment preferences
* Analyze monthly profit trends
* Compare sub-category profitability

---

## 📈 Key Metrics

| Metric                 | Dashboard Value |
| ---------------------- | --------------: |
| 💰 Total Revenue       |           ₹438K |
| 📈 Total Profit        |            ₹37K |
| 📦 Total Quantity Sold |           5,615 |
| 🧾 Average Order Value |           ₹121K |

> **Note:** Values shown above represent the metrics reported in the dashboard. AOV should be validated against the underlying order-count definition before using it as a formal business KPI.

---

# 🔎 Business Insights

### 👤 Sales & Customers

* **Hariprash** generated the highest sales volume.
* **Madhav** and **Madan Mohan** followed among the stronger customers.
* **Maharashtra** and **Madhya Pradesh** were among the leading revenue-generating states.

### 👕 Category Performance

**Clothing** dominated quantity sold:

| Category       | Share |
| -------------- | ----: |
| 👕 Clothing    |   63% |
| 💻 Electronics |   21% |
| 🛋️ Furniture  |   17% |

This indicates a strong demand concentration within the clothing category.

### 📈 Profitability

* Profit showed noticeable variation across months.
* **January** and **December** recorded strong profit performance.
* **June** showed negative profit, which could warrant investigation into discounts, returns, costs or promotional campaigns.

### 💳 Payment Behavior

| Payment Mode             |           Share |
| ------------------------ | --------------: |
| 💵 COD                   |             44% |
| 📱 UPI                   |             21% |
| 💳 Credit/Debit & Others | Remaining share |

The high COD share suggests an opportunity to encourage digital payment adoption.

### 🖨️ Sub-Category Profitability

**Printers** and **Bookcases** were among the strongest-performing sub-categories in terms of profitability.

Lower-performing categories can be investigated for:

* Pricing adjustments
* Inventory optimization
* Promotional changes
* Product repositioning

---

# 📂 Ecommerce Dataset

### `Orders.csv`

Contains transactional information such as:

```text
OrderID
Amount
Profit
Quantity
PaymentMode
CustomerName
State
```

### `Details.csv`

Contains product information such as:

```text
ProductName
Category
Sub-Category
```

---

# 📊 Dashboard Visuals

| Visualization           | Purpose                         |
| ----------------------- | ------------------------------- |
| 📌 KPI Cards            | Revenue, profit, quantity & AOV |
| 📊 Customer Bar Chart   | Top customers by sales          |
| 🍩 Category Donut Chart | Category quantity distribution  |
| 🌎 State Bar Chart      | Regional revenue                |
| 💳 Payment Donut Chart  | Payment preferences             |
| 📈 Monthly Profit Chart | Profit trends                   |
| 📊 Sub-Category Chart   | Profitability comparison        |
| 🎛️ Quarter Slicer      | Time-based filtering            |
| 🎛️ State Slicer        | Geographic filtering            |

---

# 🧮 DAX Measures

### Total Sales Amount

```DAX
Total Amount =
SUM(Orders[Amount])
```

### Total Profit

```DAX
Total Profit =
SUM(Orders[Profit])
```

### Average Order Value

```DAX
AOV =
DIVIDE(
    SUM(Orders[Amount]),
    COUNT(Orders[OrderID])
)
```

### Monthly Profit

```DAX
Monthly Profit =
CALCULATE(
    SUM(Orders[Profit]),
    ALLEXCEPT(
        Orders,
        Orders[Month]
    )
)
```

### Clothing Quantity Share

```DAX
Clothing Share % =
DIVIDE(
    CALCULATE(
        SUM(Orders[Quantity]),
        Details[Category] = "Clothing"
    ),
    CALCULATE(
        SUM(Orders[Quantity])
    )
)
```

---

# 💳 Dashboard 02 — Credit Card Financial Dashboard

The **Credit Card Financial Dashboard** provides an end-to-end view of credit card transactions, revenue, customer behavior and financial performance.

It combines financial KPIs with demographic and transaction-level analysis to help identify patterns across:

* Customer segments
* Card categories
* Transaction types
* Expenditure categories
* Education
* Occupation
* Chip usage
* Quarterly performance

---

## 📸 Dashboard Preview

![Credit Card Financial Dashboard](https://github.com/user-attachments/assets/4c5d4d3b-165f-4372-9edd-e5d625ede7c4)

---

# 📊 Key Financial Metrics

| KPI                         | Value |
| --------------------------- | ----: |
| 💰 Revenue                  |   55M |
| 💳 Total Transaction Amount |   45M |
| 💵 Interest Earned          | 7.84M |
| 🔢 Transaction Count        |  656K |

---

# 📈 Financial Dashboard Insights

### 📅 Quarterly Performance

**Highest Revenue**

> Q1 — approximately **14M**

**Highest Transaction Count**

> Q3 — approximately **166.6K transactions**

---

### 💳 Revenue by Card Category

| Card Category | Revenue |
| ------------- | ------: |
| 🔵 Blue       |     46M |
| ⚪ Silver      |      6M |
| 🟡 Gold       |      2M |
| 🟣 Platinum   |      1M |

The Blue card category contributes the majority of total revenue.

---

### 👔 Revenue by Job Type

| Job Type                   | Revenue |
| -------------------------- | ------: |
| Businessman                |     17M |
| White-collar               |     10M |
| Self-employed / Government |      8M |

This segmentation provides a view of revenue contribution across customer occupations.

---

### 🛒 Revenue by Expenditure Type

| Expenditure   | Revenue |
| ------------- | ------: |
| Bills         |     14M |
| Entertainment |     10M |
| Fuel          |      9M |

Bills represent the largest expenditure category among the highlighted segments.

---

### 💳 Revenue by Chip Usage

| Transaction Type | Revenue |
| ---------------- | ------: |
| Swipe            |     35M |
| Chip             |     17M |
| Online           |      3M |

Swipe transactions represent the largest contribution to revenue.

---

### 🎓 Revenue by Education

**Graduates** represent the highest-revenue education segment at approximately **22M**.

---

# 📆 Week-over-Week Revenue

| Week | Previous Week | Current Week |    Change |
| ---: | ------------: | -----------: | --------: |
|   52 |     1,070,439 |      933,134 | 🔻 -12.8% |
|   51 |     1,026,549 |    1,070,439 |  🟢 +4.3% |
|   50 |       980,152 |    1,026,549 |  🟢 +4.7% |

### 📌 Observation

The dashboard shows positive momentum across weeks 50 and 51, followed by a decline in week 52.

This type of WoW analysis can help identify short-term changes in customer spending behaviour.

---

# 🎛️ Interactive Features

Both dashboards use interactive Power BI functionality including:

```text
┌───────────────────────────────┐
│        INTERACTIVE BI         │
├───────────────────────────────┤
│                               │
│  🎛️ Slicers                  │
│  📊 Dynamic Visuals            │
│  🔎 Filtering                 │
│  📌 KPI Cards                 │
│  📈 Trend Analysis             │
│  🖱️ Cross Filtering            │
│  🔍 Drill-down Analysis       │
│                               │
└───────────────────────────────┘
```

Users can dynamically explore the data rather than relying on static reports.

---

# 🤖 How ChatGPT & AI Were Used

One of the main goals of this project was to explore **AI-assisted BI development**.

### AI-assisted workflow

```text
Raw Data
   │
   ▼
Data Understanding
   │
   ▼
Power Query / Modeling
   │
   ▼
ChatGPT-assisted DAX
   │
   ▼
KPI Development
   │
   ▼
Dashboard Design
   │
   ▼
Business Insights
   │
   ▼
Validation & Refinement
```

### ChatGPT assisted with:

* 🧮 DAX formulas
* 🧠 Analytical reasoning
* 🐛 Debugging
* 📊 Visualization ideas
* 🧩 Data modeling approaches
* ✨ Dashboard improvement
* 🔍 Insight generation

---

# 🛠️ Technology Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=python,django,git,github,vscode,docker" />

<br><br>

<img src="https://img.shields.io/badge/Microsoft%20Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
<img src="https://img.shields.io/badge/DAX-Data%20Analysis-00A4EF?style=for-the-badge" />
<img src="https://img.shields.io/badge/ChatGPT-AI%20Assistance-412991?style=for-the-badge&logo=openai&logoColor=white" />
<img src="https://img.shields.io/badge/SQL-Database-336791?style=for-the-badge&logo=postgresql&logoColor=white" />

</div>

---

# 🚀 How to Use

### 1️⃣ Install Power BI Desktop

Download and install **Microsoft Power BI Desktop**.

### 2️⃣ Load the Dataset

Import:

```text
Orders.csv
Details.csv
```

For the credit card dashboard, load the corresponding financial transaction dataset.

### 3️⃣ Open the PBIX File

Open the project in Power BI Desktop.

### 4️⃣ Explore the Dashboard

Use:

* State filters
* Quarter filters
* Gender filters
* Card type filters
* Interactive charts
* KPI cards

to explore the data.

---

# 🏅 Certification

## 📜 AI Dashboards using Microsoft Power BI

**Certified by Skill Nation**

This certification demonstrates proficiency in creating **AI-enhanced Power BI dashboards**, working with real-time data concepts, advanced visualizations and AI-assisted analytics workflows.

---

# 📚 Skills Demonstrated

```text
Power BI
│
├── Data Visualization
├── Dashboard Design
├── KPI Development
├── Interactive Reporting
├── Data Modeling
│
DAX
│
├── Measures
├── Aggregations
├── CALCULATE
├── DIVIDE
└── Context Management
│
AI
│
├── ChatGPT
├── AI-Assisted Development
├── Prompt Engineering
└── Analytical Reasoning
│
Business Analytics
│
├── Sales Analysis
├── Financial Analysis
├── Customer Analysis
├── Profitability Analysis
└── Trend Analysis
```

---

# 🔮 Future Improvements

Potential enhancements include:

* 🔄 Real-time API integration
* 📦 Inventory analytics
* 👥 Customer Lifetime Value (CLV)
* 🔁 Customer retention analysis
* 💰 ROI analysis
* 📉 Return-rate analysis
* 🤖 AI-powered forecasting
* 🧠 Natural-language querying
* 📊 Automated business summaries
* ☁️ Power BI Service deployment

---

# 💡 Key Takeaways

This project demonstrates how **Business Intelligence + AI assistance** can accelerate the analytics development lifecycle.

The dashboards transform raw transactional data into:

> **Data → Information → Insight → Decision**

The combination of **Power BI, DAX, ChatGPT and business analytics** creates a workflow that is faster, more iterative and highly adaptable.

---

# 👨‍💻 Author

<div align="center">

### **Soutik Talukder**

`Python Developer` · `GenAI Developer` · `Django Developer` · `Application Support` · `Power BI`

<a href="https://github.com/soutiktalukder999">
<img src="https://img.shields.io/badge/GitHub-soutiktalukder999-181717?style=for-the-badge&logo=github" />
</a>

<br><br>

**⚡ Building with Python • AI • Data • BI**

</div>

---

<div align="center">

### ⭐ If you found this project useful, consider giving it a star!

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00F7FF,50:7B61FF,100:000000&height=120&section=footer"/>

</div>
