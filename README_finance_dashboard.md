# FinceSight: Finance Analytics Dashboard

An interactive Power BI dashboard that gives management one place to track transactions, fees, taxes, customer segments and regional performance, with year-over-year comparison and drill-down to individual records.

**Skills shown:** Power BI, DAX, data modelling, data cleaning, dashboard design, KPI reporting

---

## Preview

| Overview | Transactions |
|---|---|
| ![Overview](images/overview.png) | ![Transactions](images/transactions.png) |

---

## The problem

A financial organization could not easily see how its business was performing. Transaction growth, monthly trends, failed payments, top customer segments, state-wise results, fees and taxes were all spread across raw data. The goal was a single dashboard that answers these questions in seconds and lets users filter and drill down on their own.

## What the dashboard answers

| Question | Where to look |
|---|---|
| How much money moved, and how does it compare with last year? | 5 KPI cards with year-over-year change |
| Which months are strong or weak? | Total Amount by Month |
| How many payments succeed, fail or stay pending? | Amount by Transaction Status |
| Which customer segments bring the most value? | Amount by Customer Segment |
| Which states perform best? | Amount by State |
| Which transaction types earn the most fees and tax? | Transaction Type heatmap table |
| How do male and female customers compare? | Amount by Gender |
| What are the exact transactions behind a number? | Transactions page with drillthrough |

**KPIs:** Total Amount, Total Transactions, Average Transaction Value, Total Fees, Total Tax

## Pages

**1. Overview:** 5 KPI cards and 6 charts (monthly trend, status donut, segment bar, state bar, transaction type heatmap table, gender donut).

**2. Transactions:** a detailed grid of every transaction, with a coloured status column and colour-scaled amount, fees and tax. A back button returns to the Overview.

## Features

- **Dynamic Measure slicer:** one dropdown switches the main charts between Amount, Transactions, Average Value, Fees and Tax, and the chart titles update with it
- **Year-over-year comparison** on every KPI card
- **Drillthrough:** right click a bar, slice or point on the Overview and open the matching transactions
- **Synced slicers:** Year, Occupation and Category apply to both pages
- **Clean, consistent design:** dark sidebar, light canvas, one accent colour, card layout

## Key insights (2025)

- **Retail** is the biggest segment, contributing over half of the total amount (about 76M of 137.5M).
- **Maharashtra** leads all states (about 22M), followed by Karnataka and Gujarat.
- **Loan EMI** and **Transfer** are the two largest transaction types and together make up more than half of the total amount. Loan EMI also earns the highest fees.
- About **85%** of the amount comes from successful transactions, around **10%** from failed ones and about **4%** is pending.
- Monthly amount **peaked in July** and dropped to its **lowest point in September**.
- Compared with 2024, total amount grew **1.4%** while the number of transactions fell slightly (**0.6%**), so the average transaction value rose by about **2%**.
- Male and female customers contribute almost equally.

## Data model

A star schema: one transactions table connected to a customers table and a calendar table, so every chart can be filtered by customer details and by time.

```
customers (1) ---- (many) finance_transactions (many) ---- (1) Calendar
```

## About the data

The dataset is **dummy (sample) data created for practice**. It does not belong to any real company or bank. It has about 50,000 transactions in INR.

## Repository structure

```
finance-analytics-powerbi-dashboard/
  powerbi/    dashboard file (.pbix)
  images/     dashboard screenshots
  docs/       Business_Requirements.docx
  README.md
```

## How to open

1. Download the `.pbix` file from the `powerbi/` folder.
2. Open it in **Power BI Desktop** (free from Microsoft, Windows only).

## Author

**Roshan Shaw**, final-year B.Tech (IT), Kolkata
[GitHub](https://github.com/Ronan-112) | [LinkedIn](#) | roshanshaw94770@gmail.com
