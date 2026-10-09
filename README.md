# Level 2 – Task 3: Payment Mode Analysis
**RaushByte Technologies – Data Analytics Internship**

---

## 📌 Objective
Analyze how customers pay (UPI, Card, Cash, Net Banking), compare the four methods, calculate revenue by payment method, and study payment trends by region, in an interactive report.

---

## ✅ Requirements Completed

| # | Requirement | Status |
|---|-------------|--------|
| 1 | Analyze customer payment preferences | ✅ Done |
| 2 | Compare UPI, Card, Cash and Net Banking usage | ✅ Done |
| 3 | Calculate revenue by payment method | ✅ Done |
| 4 | Analyze region-wise payment trends | ✅ Done |
| 5 | Create reports and visualizations | ✅ Done (interactive HTML dashboard) |

---

## 📊 Dataset
- **File:** `data_analytics_sales_dataset`
- **Rows:** 8,000 orders | **Missing values:** 0 | **Duplicates:** 0
- **Period:** 1 Jan 2024 to 15 May 2025 (May 2025 is a partial month)
- **Columns used:** Region, Product, Payment_Mode, Date, Sales, Profit, Customer_Rating
- **Consistency checks:** Sales = Quantity × Unit_Price and Profit = Sales − Expense hold for every row

---

## 📈 Key Findings

### 1. Payment method comparison
| Method | Orders | % of Orders | Revenue | % of Revenue | Avg Order Value | Profit Margin |
|--------|--------|-------------|---------|--------------|-----------------|---------------|
| Cash | 2,053 | 25.7% | ₹52.3 Cr | 25.9% | ₹2,54,841 | 30.2% |
| UPI | 2,003 | 25.0% | ₹49.2 Cr | 24.4% | ₹2,45,385 | 29.8% |
| Card | 1,992 | 24.9% | ₹50.7 Cr | 25.1% | ₹2,54,363 | 29.8% |
| Net Banking | 1,952 | 24.4% | ₹49.6 Cr | 24.6% | ₹2,54,296 | 29.4% |
| **Total** | **8,000** | 100% | **₹201.8 Cr** | 100% | ₹2,52,221 | 29.8% |

- **Cash is the most used and highest-revenue method**, but only by a small margin over the others.
- **UPI has the lowest revenue and lowest average order value** (about 3.7% below the others).
- Usage is almost evenly split: each method is used for roughly a quarter of orders.

### 2. Region-wise payment trends (share of each region's orders)
| Region | UPI | Card | Cash | Net Banking |
|--------|-----|------|------|-------------|
| North | 24.9% | 25.3% | 26.4% | 23.3% |
| South | 24.0% | 24.3% | 25.3% | 26.4% |
| East | 26.4% | 24.9% | 25.0% | 23.8% |
| West | 24.9% | 25.1% | 26.0% | 24.1% |

- Largest regional leans: **South prefers Net Banking (26.4%)**, **East prefers UPI (26.4%)**, **North and West lean to Cash**.
- **West has the highest Cash revenue (₹14.1 Cr)**; **South has the lowest UPI revenue (₹11.7 Cr)**.

### 3. Are these differences real?
No. A chi-square test found that payment mix does **not** depend on region (p = 0.50), and an ANOVA found no significant difference in order value between payment methods (p = 0.39). The regional "preferences" above are within normal random variation. The honest conclusion is that **customers in this dataset use all four methods about equally in every region**.

### 4. Business takeaway
Because no method clearly dominates, a business should support all four methods in every region rather than prioritise one. The one small signal worth monitoring is UPI's lower order value.

---

## 🖥️ Dashboard Features

- **6 KPI cards:** Orders, Total Revenue, Avg Order Value, Profit, Leading Method, Avg Rating
- **Filters:** Region, Payment method, Year, Product (every chart updates live)
- **8 visuals:** Revenue by method, usage share donut, full comparison table, region-wise payment mix (100% bars), region × method revenue heatmap, product × method mix, monthly trend (switch between Orders and Revenue)
- **"What this view says"** panel that rewrites itself for the current filters
- Works offline, no install, light and dark mode

---

## 📁 Project Structure

```
Level2-Task3-Payment-Mode-Analysis/
│
├── dashboard.html      ← Interactive dashboard (data embedded)
├── README.md           ← This file
└── requirements.txt    ← Python dependencies (optional)
```

---

## 🚀 How to Open

1. Download `dashboard.html`
2. Double-click it → opens in your browser (Chrome, Edge, Firefox)
3. Use the filters on the left

---

## 🛠️ Tools Used

- **Python 3** (pandas, SciPy): data checks and significance tests
- **HTML + CSS + JavaScript:** interactive dashboard with hand-built SVG charts (no external libraries)

---

*Level 2 – Task 3 | RaushByte Technologies Data Analytics Internship*
