# 📊 Investment Portfolio Performance Analysis

---

## 📈 Overview

This repository presents an interactive **Investment Portfolio Performance Analysis Dashboard** developed using **Microsoft Power BI**.

The project analyzes a diversified stock portfolio to evaluate investment performance, profitability, returns, current portfolio value, and company-wise performance.

The dashboard combines financial analysis with interactive data visualization to help users understand portfolio performance, compare investments, and identify the strongest-performing companies.

---

## 🎯 Project Objective

The primary objective of this project is to evaluate the performance of an investment portfolio using an interactive Power BI dashboard.

The analysis focuses on:

- 💰 Total Amount Invested
- 💵 Current Portfolio Value
- 📈 Overall Portfolio Return
- 📊 Company-wise Returns
- 🏆 Top Performing Company
- 💹 Net Profit / Gain or Loss
- 🏢 Company-level Performance
- 📊 Profit Contribution by Company
- 🔍 Investment vs. Current Value
- 📈 Investment vs. Return

The dashboard transforms portfolio data into actionable financial insights through KPIs, charts, comparisons, and interactive filters.

---

## 📝 Description

This project demonstrates the application of **Business Intelligence, Financial Analytics, and Data Visualization** to investment portfolio data.

The Power BI dashboard provides an interactive environment for analyzing the relationship between investment amount, current value, gain/loss, and percentage returns.

By combining KPI cards, charts, filters, and DAX measures, the dashboard enables users to identify high-performing investments and understand portfolio-level profitability.

The project demonstrates how financial data can be transformed into an interactive analytical solution for investment performance evaluation.

---

## 📊 Dashboard

The project contains a **single-page interactive Power BI dashboard** designed to provide a comprehensive overview of portfolio performance.

### 📈 Portfolio Performance Dashboard

![Portfolio Performance Dashboard](DASHBOARD%20IMAGES/DASH.png)

The dashboard provides insights into:

- 💰 Total Amount Invested
- 💵 Current Portfolio Value
- 📈 Portfolio Return
- 🏆 Top Performing Company
- 💹 Net Profit
- 📊 Company-wise Return
- 🍩 Profit Contribution by Company
- 📈 Investment vs. Current Value
- 📊 Investment vs. Return
- 🔍 Company and Sector filtering

---

## ✨ Features

- 📊 Interactive Power BI portfolio dashboard
- 💰 Total investment analysis
- 💵 Current portfolio value analysis
- 📈 Portfolio return calculation
- 🏆 Top performer identification
- 💹 Net profit analysis
- 🏢 Company-wise return analysis
- 📊 Profit contribution analysis
- 🔍 Interactive company filtering
- 🏭 Sector-level filtering
- 📈 Investment vs. return comparison
- 💰 Investment vs. current value comparison
- 🧮 DAX-based financial calculations
- 📑 Excel-based portfolio dataset
- 📋 Project presentation included
- 🖼️ Dashboard screenshot included

---

## 📌 Key Metrics

| 📌 Metric | 📊 Description |
|---|---|
| 💰 Amount Invested | Total amount invested across the portfolio |
| 💵 Current Portfolio Value | Current value of the investments |
| 📈 Portfolio Return | Overall gain/loss relative to total investment |
| 🏢 Number of Holdings | Number of companies included in the portfolio |
| 🏆 Top Performer | Company with the highest percentage return |
| 💹 Net Profit | Gain/loss associated with the top-performing investment |

---

## 🧮 DAX Measures

The dashboard uses **DAX (Data Analysis Expressions)** to calculate key portfolio performance indicators.

### 1️⃣ Portfolio Return

```DAX
Portfolio Return =
DIVIDE(
    SUM(Sheet1[Gain / Loss (₹)]),
    SUM(Sheet1[AmountInvested (₹)]),
    0
)
```

Calculates the overall portfolio return by dividing total gain/loss by total amount invested.

---

### 2️⃣ Top Performer Sector

```DAX
Top Performer Sector =
MAXX(
    TOPN(
        1,
        Sheet1,
        Sheet1[Gain / Loss (%)],
        DESC
    ),
    Sheet1[Sector]
)
```

Identifies the sector associated with the top-performing company.

---

### 3️⃣ Top Performer

```DAX
Top Performer =
MAXX(
    TOPN(
        1,
        Sheet1,
        Sheet1[Gain / Loss (%)],
        DESC
    ),
    Sheet1[Company Name]
)
```

Identifies the company with the highest percentage return in the portfolio.

---

### 4️⃣ Net Profit

```DAX
Net Profit =
MAXX(
    TOPN(
        1,
        Sheet1,
        Sheet1[Gain / Loss (%)],
        DESC
    ),
    Sheet1[Gain / Loss (₹)]
)
```

Returns the gain/loss in ₹ associated with the company having the highest percentage return.

---

### 5️⃣ Max Return (%)

```DAX
Max Return (%) =
MAX(Sheet1[Gain / Loss (%)]) / 100
```

Identifies the maximum percentage return recorded among the companies in the portfolio.

---

### 6️⃣ Company Return (%)

```DAX
Company Return (%) =
DIVIDE(
    MAX(Sheet1[Gain / Loss (%)]),
    100
)
```

Converts company-level gain/loss percentage values into decimal percentage format for visualization.

---

## 📊 Visualizations

The dashboard uses interactive Power BI visuals to communicate portfolio performance.

### Portfolio Analysis

- 📌 KPI Cards
- 📊 Company-wise Return Chart
- 💰 Investment vs. Current Value
- 📈 Investment vs. Return
- 🍩 Profit Contribution by Company
- 🏆 Top Performer Indicator
- 📈 Portfolio Return Analysis

### Interactive Analysis

The dashboard supports interactive exploration through portfolio-related filters and visual interactions.

Users can analyze:

- Companies
- Sectors
- Investments
- Returns
- Current Value
- Gain / Loss
- Portfolio Performance

---

## ⚡ Main Insights

The dashboard is designed to provide insights into portfolio performance through:

- 🏆 Identification of the highest-returning company
- 📈 Comparison of returns across companies
- 💰 Comparison between invested amount and current value
- 💵 Analysis of portfolio-level profit/loss
- 📊 Understanding company-wise contribution to portfolio performance
- 🔎 Interactive exploration of individual investments
- 📈 Identification of stronger and weaker portfolio performers

---

## 💡 Business Use Case

Investment portfolios contain multiple securities with different levels of investment and performance.

A portfolio performance dashboard can help investors and analysts:

- Monitor investment performance
- Compare individual companies
- Identify high-performing investments
- Evaluate portfolio profitability
- Understand investment returns
- Compare current value against invested capital
- Analyze gain/loss across investments
- Make data-driven portfolio decisions

This project demonstrates how Power BI can be used to present financial metrics in an intuitive and interactive format.

---

## 🔄 Analytical Workflow

```text
Excel Portfolio Dataset
          ↓
   Data Preparation
          ↓
      Power BI
          ↓
     DAX Measures
          ↓
 Interactive Dashboard
          ↓
Financial Performance
      Analysis
          ↓
   Actionable Insights
```

---

## 🛠️ Technologies Used

- **Microsoft Power BI** — Dashboard development, visualization, analytics, and reporting
- **DAX** — Financial calculations and analytical measures
- **Microsoft Excel** — Portfolio dataset and source data
- **Power Query** — Data preparation and transformation

---

## 📂 Repository Structure

```text
Investment-Portfolio-Performance-Analysis/
│
├── 📁 DASHBOARD IMAGES
│   └── DASH.png
│
├── 📁 DATASET
│   └── DATASET OF PORTFOLIO.xlsx
│
├── 📁 POWER BI REPORT
│   └── PORTFOLIO DASHBOARD.pbix
│
├── 📁 PROJECT PRESENTATION
│   └── PORTFOLIO PROJECT.pptx
│
└── README.md
```

---

## 📦 What's Included

### 📊 Power BI Report

```text
POWER BI REPORT/
└── PORTFOLIO DASHBOARD.pbix
```

The complete interactive Power BI dashboard.

### 📑 Dataset

```text
DATASET/
└── DATASET OF PORTFOLIO.xlsx
```

The Excel dataset used for the portfolio analysis.

### 🖼️ Dashboard Image

```text
DASHBOARD IMAGES/
└── DASH.png
```

Screenshot of the final single-page Power BI dashboard.

### 📋 Project Presentation

```text
PROJECT PRESENTATION/
└── PORTFOLIO PROJECT.pptx
```

The presentation created for the portfolio analysis project.

---

## 🚀 Quick Start

### 1. Download or Clone the Repository

Download or clone this repository to your local system.

### 2. Open the Power BI Report

Navigate to:

```text
POWER BI REPORT/PORTFOLIO DASHBOARD.pbix
```

Open the file using **Microsoft Power BI Desktop**.

### 3. Load the Dataset

The source dataset is available at:

```text
DATASET/DATASET OF PORTFOLIO.xlsx
```

If Power BI asks for the source file location, update the data source path to the downloaded Excel file.

### 4. Explore the Dashboard

Open the dashboard and interact with the available filters and visualizations.

Users can analyze:

- Investment amount
- Current portfolio value
- Portfolio return
- Company-wise returns
- Sector-wise performance
- Profitability
- Top-performing company
- Gain/loss

### 5. Review the Presentation

The project presentation is available at:

```text
PROJECT PRESENTATION/PORTFOLIO PROJECT.pptx
```

---

## 🎓 Project Context

This project was developed as part of a **Portfolio Management Workshop**.

It demonstrates the practical application of:

- Financial Analysis
- Investment Portfolio Analysis
- Business Analytics
- Business Intelligence
- Data Visualization
- Power BI
- DAX

The project combines financial concepts with data analytics to create an interactive investment-performance reporting solution.

---

## 🎯 Skills Demonstrated

- 📊 Microsoft Power BI
- 🧮 DAX
- 📈 Financial Data Analysis
- 💰 Portfolio Performance Analysis
- 📌 KPI Development
- 📊 Data Visualization
- 🔍 Interactive Dashboard Design
- 📑 Excel Data Analysis
- 💡 Business Intelligence
- 📈 Performance Analysis
- 🏢 Company-wise Analysis
- 🏭 Sector-wise Analysis

---

## 📚 Project Learning Outcomes

This project provided practical experience in:

- Building interactive Power BI dashboards
- Creating financial KPIs
- Writing DAX measures
- Comparing investment performance
- Analyzing gain/loss data
- Creating company-level performance analysis
- Designing business-oriented visualizations
- Presenting financial insights through dashboards
- Converting raw financial data into meaningful insights

---

## 👥 Audience

This project can be useful for:

- 📊 Business Analytics students
- 💰 Finance and investment students
- 📈 Data analysts
- 💼 Business analysts
- 📊 Power BI learners
- 💹 Investment enthusiasts
- 🎓 Students building financial analytics portfolios

---

## 🤝 Contributing

Suggestions, improvements, and feedback are welcome.

For questions, feedback, or improvements, feel free to open an issue or start a discussion.

---

## 📄 License

This project is distributed under the **MIT License**.

---

## 📬 Get in Touch

**Sahil Singhal**

Business Analytics | Data Analytics | Power BI

<p align="left">
  <a href="https://www.linkedin.com/in/sahil-singhal-2b507823b/">
    <img src="https://img.shields.io/badge/LinkedIn-Profile-blue?style=for-the-badge&logo=linkedin" alt="LinkedIn">
  </a>
  <a href="mailto:SINGHALSAHIL22@GMAIL.COM">
    <img src="https://img.shields.io/badge/Email-Contact-red?style=for-the-badge&logo=gmail" alt="Email">
  </a>
  <a href="https://github.com/0SAHILl">
    <img src="https://img.shields.io/badge/GitHub-Profile-black?style=for-the-badge&logo=github" alt="GitHub">
  </a>
</p>

---

## 🏆 Credits

This project was developed by **Sahil Singhal** as part of a **Portfolio Management Workshop**.

---

## ⭐ Final Note

Thank you for checking out this project!

📊 **Turning investment data into meaningful financial insights through Power BI and DAX.**
