# 📝 Note: Revenue Analysis and Customer-Level Aggregation on UK E-Commerce Data

## Methodology

### 1. Data Loading & Quality Check
- Loaded `data.csv` (encoding=ISO-8859-1): **541,909 rows**, 8 columns
- **CustomerID**: 135,080 missing rows (25%) — dropped for customer-level analysis
- **Description**: 1,454 missing — retained where possible

### 2. Data Cleaning Pipeline
1. Convert `InvoiceNo` to string for cancelled order detection
2. Separate cancelled orders (`InvoiceNo` starting with "C"): ~9,288 invoices
3. Drop rows with missing `CustomerID`
4. Filter out negative `Quantity` (returns): ~25,900 rows kept for return analysis
5. Remove zero/negative `UnitPrice` entries
6. Convert `InvoiceDate` to datetime; extract year, month features

### 3. Revenue Engineering
- Created `Revenue = Quantity × UnitPrice`
- Aggregated at **customer level**: total revenue, order count, avg order value, unique products
- Aggregated at **country level**: total revenue, order count, customer count, revenue share %

### 4. Return Rate Analysis
- Calculated cancellation rate: cancelled invoices / total invoices per country
- Flagged markets: 🔴 HIGH (>20%), ⚠️ MEDIUM (10-20%), ✅ LOW (<10%)

### 5. Visualizations

| # | Chart | File |
|---|-------|------|
| 1 | Monthly Revenue Line | `chart1_monthly_revenue.png` |
| 2 | Top 10 Countries Bar | `chart2_top10_countries.png` |
| 3 | Top 20 Products Bar | `chart3_top20_products.png` |
| 4 | Return Rate by Country | `chart4_return_rate.png` |
| 5 | ⭐ Top Customers Trend | `chart5_top_customers_trend.png` |
| 6 | ⭐ Basket Size by Country | `chart6_basket_size.png` |

---

## Key Findings

| Metric | Value |
|--------|-------|
| Total Revenue | ~£9.7M |
| Unique Customers | ~4,300 |
| UK Revenue Share | ~82% |
| Peak Month | November (~£1.16M) |
| Top Product | WHITE HANGING HEART T-LIGHT HOLDER |
| Avg Order Value | ~£392 |
| Top 5 Customers Share | ~5.2% |

---

## 💡 5 Business Insights

1. **UK = 82% Revenue** — Extreme geographic concentration; diversify into EU markets
2. **November = Peak** — Christmas effect; start promotions in October
3. **Top 5 Customers = 5.2%** — VIP churn risk; implement loyalty program
4. **High Return Markets** — Some countries >20% cancellation; investigate quality/fit issues
5. **Gift Items Dominate** — Create curated bundles and subscription boxes for Q4

## Technical Stack
- **Python 3.13**: pandas, matplotlib, seaborn
- **Dataset**: `data.csv` (541,909 rows × 8 columns, ISO-8859-1 encoding)
- **Source**: [UCI ML Repository — Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)

*Analysis completed April 2026*
