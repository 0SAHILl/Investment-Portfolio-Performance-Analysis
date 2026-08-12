# 📊 Investment Portfolio Performance Analysis

---

## 📈 Overview

This repository presents an interactive **Investment Portfolio Performance Analysis Dashboard** developed using **Microsoft Power BI**.

The project analyzes a diversified stock portfolio to evaluate investment performance, profitability, returns, current portfolio value, and company-wise performance.

The dashboard combines financial analysis with interactive data visualization to help users understand portfolio performance, compare investments, and identify the strongest-performing companies.

---

## 🎯 Project Objective

The primary objective of this project is to evaluate the performance of an investment portfolio using interactive Power BI dashboards.

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

The Power BI report contains two dashboard pages designed to provide both a high-level portfolio overview and detailed performance analysis.

### 🏠 Page 1 — Portfolio Overview

The first dashboard provides a high-level summary of the investment portfolio.

![Portfolio Overview](DASHBOARD%20IMAGES/PAGE%201.png)

The dashboard provides insights into:

- 💰 Total Amount Invested
- 💵 Current Portfolio Value
- 📈 Overall Portfolio Return
- 🏢 Company-wise Performance
- 🏆 Top Performing Company
- 💹 Net Profit / Gain or Loss
- 📊 Portfolio Performance

---

### 📈 Page 2 — Portfolio Performance Analysis

The second dashboard provides deeper analysis of individual investments and company-level performance.

![Portfolio Performance Analysis](DASHBOARD%20IMAGES/PAGE%202.png)

The analysis focuses on:

- Investment vs. Current Value
- Investment vs. Return
- Company-wise Returns
- Profitability Analysis
- Company Performance
- Interactive Portfolio Analysis
- Comparative Investment Performance

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
- 🖼️ Dashboard screenshots included

---

## 📌 Key Metrics

| 📌 Metric | 📊 Description |
|---|---|
| 💰 Amount Invested | Total amount invested across the portfolio |
| 💵 Current Portfolio Value | Current value of the investments |
| 📈 Portfolio Return | Overall gain/loss relative to total investment |
| 🏢 Number of Companies | Number of companies included in the portfolio |
| 🏆 Top Performer | Company with the highest percentage return |
| 💹 Net Profit | Gain/loss associated with the top-performing investment |

---

## 🧮 DAX Measures

The dashboard uses **DAX (Data Analysis Expressions)** to calculate key portfolio performance indicators.

### 1️⃣ Max Return (%)

```DAX
Max Return (%) =
MAX(Sheet1[Gain / Loss (%)])/100
```

This measure identifies the maximum percentage gain/loss recorded among the companies in the portfolio.

---

### 2️⃣ Net Profit

```DAX
Net Profit =
MAXX(
    TOPN(1, Sheet1, Sheet1[Gain / Loss (%)], DESC),
    Sheet1[Gain / Loss (₹)]
)
```

This measure returns the gain/loss in ₹ associated with the company having the highest percentage return.

---

### 3️⃣ Portfolio Return

```DAX
Portfolio Return =
DIVIDE(
    SUM(Sheet1[Gain / Loss (₹)]),
    SUM(Sheet1[AmountInvested (₹)]),
    0
)
```

This measure calculates the overall portfolio return by dividing total gain/loss by the total amount invested.

---

### 4️⃣ Top Performer

```DAX
Top Performer =
MAXX(
    TOPN(1, Sheet1, Sheet1[Gain / Loss (%)], DESC),
    Sheet1[Company Name]
)
```

This measure identifies the company with the highest percentage return in the portfolio.

---

## 📊 Visualizations

The dashboard uses interactive Power BI visuals to communicate portfolio performance.

### Portfolio Analysis

- 📌 KPI Cards
- 📊 Company-wise Return Charts
- 💰 Investment Comparison
- 💵 Current Portfolio Value Comparison
- 📈 Return Analysis
- 💹 Profitability Analysis
- 🏆 Top Performer Indicator

### Interactive Analysis

The dashboard supports interactive exploration through portfolio-related filters and visual interactions.

Users can analyze:

- Companies
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
│   ├── PAGE 1.png
│   └── PAGE 2.png
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

### 🖼️ Dashboard Images

```text
DASHBOARD IMAGES/
├── PAGE 1.png
└── PAGE 2.png
```

Screenshots of the Power BI dashboard pages.

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

Navigate through the dashboard pages and interact with the available filters and visualizations.

Users can analyze:

- Investment amount
- Current portfolio value
- Portfolio return
- Company-wise returns
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

## 📄 License

This project is distributed under the **MIT License**.

---

## 🤝 Contributing

Suggestions, improvements, and feedback are welcome.

For questions, feedback, or improvements, feel free to open an issue or start a discussion.

---


## 📬 Get in touch

[![Email](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:singhalsahil22@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sahil-singhal-2b507823b/)
---

## 🏆 Credits

This project was developed by **Sahil Singhal** as part of a **Portfolio Management Workshop**.

---

## ⭐ Final Note

Thank you for checking out this project!

📊 **Turning investment data into meaningful financial insights through Power BI and DAX.**
