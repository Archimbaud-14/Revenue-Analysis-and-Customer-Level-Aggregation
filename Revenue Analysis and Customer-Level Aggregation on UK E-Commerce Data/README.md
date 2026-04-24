# 💷 Revenue Analysis and Customer-Level Aggregation on UK E-Commerce Data

> Clean a large real-world transaction dataset, engineer revenue metrics and perform customer/product-level aggregations.

![Python](https://img.shields.io/badge/Python-3.13-3776AB?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.3-150458?logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Level](https://img.shields.io/badge/Level-Advanced-red)

---

## 📖 About
Analysis of **541,909 e-commerce transactions** from a UK-based online retailer. Covers data cleaning (missing CustomerID, cancellations, negative quantities), revenue engineering, customer/country aggregation, return rate analysis, and 5 business insights.

## 📊 Dataset
| Property | Detail |
|----------|--------|
| **File** | `data.csv` (ISO-8859-1) |
| **Records** | 541,909 → ~397K after cleaning |
| **Columns** | 8 features |
| **Date Range** | Dec 2010 – Dec 2011 |

## 📁 Structure
```
├── 📓 UK_Revenue_Analysis.ipynb
├── 📝 note.md · 📄 README.md · 📊 data.csv
├── 🖼️ chart1_monthly_revenue.png
├── 🖼️ chart2_top10_countries.png
├── 🖼️ chart3_top20_products.png
├── 🖼️ chart4_return_rate.png
├── 🖼️ chart5_top_customers_trend.png  ⭐
└── 🖼️ chart6_basket_size.png          ⭐
```

## 🔍 Key Findings
| Metric | Value |
|--------|-------|
| 💰 Total Revenue | ~£9.7M |
| 🇬🇧 UK Share | ~82% |
| 📅 Peak Month | November |
| 👤 Unique Customers | ~4,300 |
| 🔄 High-Return Markets | Flagged (>20%) |

## ✅ Deliverables
- [x] Jupyter notebook with full pipeline
- [x] note.md with methodology and 5 insights
- [x] Monthly revenue line chart
- [x] Top 10 countries bar chart
- [x] Top 20 products horizontal bar
- [x] Return rate by country
- [x] ⭐ Top customers monthly spending trend
- [x] ⭐ Basket size per country

---
<p align="center"><i>Built with 🐍 Python | 📊 pandas | 🎨 matplotlib + seaborn</i></p>
