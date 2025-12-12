# 📊 Financial Reports Projects

This project analyzes and compares key **financial performance factors** across multiple companies and industries using data from their **Balance Sheets** and **Income Statements** between **2018 and 2022**.  
The goal is to derive insights into **profitability, liquidity, leverage, and efficiency trends** across sectors such as **Technology, FMCG, and Real Estate** through exploratory data analysis and visualizations.

---

## 🧭 Project Overview

Understanding how financial metrics evolve over time is essential for assessing corporate health and strategy.  
This notebook aggregates, cleans, and visualizes multi-year financial data to answer key questions such as:

- How do **profitability margins** vary across sectors and years?  
- What patterns exist between **leverage** and **profitability**?  
- Which industries maintain stronger **liquidity positions**?  
- How correlated are key balance sheet and income statement variables?

---

## 🗂️ Dataset Description

Two core datasets were used:

1. **Balance_Sheet.xlsx** — includes assets, liabilities, equity, cash, and inventory details.  
2. **Income_Statement.xlsx** — includes revenue, operating income, COGS, and expenses.  

Both files share common columns:
- `Year`
- `comp_type` (sector: `tech`, `fmcg`, `real_est`)
- `company` (ticker or name)

---

## ⚙️ Libraries Used

This project leverages Python’s data-science stack for data wrangling, statistical analysis, and visualization:

| Category | Libraries |
|:--|:--|
| Data Manipulation | `pandas`, `numpy` |
| Visualization | `matplotlib`, `seaborn` |
| File Handling | `openpyxl` |
| Jupyter Notebook Environment | `nbformat`, `IPython.display` |

---

## 🔍 Methodology

1. **Data Integration** – Combined balance sheet and income statement data by `company`, `year`, and `sector`.  
2. **Data Cleaning** – Standardized column names, handled missing values, and ensured numeric consistency.  
3. **Financial Ratio Computation** – Derived key indicators including:  
   - **Profitability:** Gross Margin, Operating Margin, ROA, ROE  
   - **Liquidity:** Current Ratio, Quick Ratio, Cash Ratio  
   - **Leverage:** Debt-to-Equity, Liabilities-to-Assets  
   - **Efficiency:** Asset Turnover, Days Inventory Outstanding (DIO)
4. **Visualization & Correlation Analysis** – Generated bar charts, heatmaps, and regression plots to understand inter-relationships among metrics.  
5. **Sector-wise Insights** – Summarized cross-industry patterns for each ratio and year.

---

## 📈 Key Visual Insights

### 1. Sector-wise Ratio Comparisons (2018–2022)
- **Tech** companies show high profitability and liquidity with low leverage.  
- **FMCG** firms maintain steady margins and moderate leverage.  
- **Real Estate** is capital-intensive with higher leverage and more variable profitability.

### 2. Correlation Heatmap
- Strong positive correlation between **Total Revenue** and **Operating Expenses (0.98)**.  
- Negative correlation between **Leverage** and **Equity (–0.54)** — higher leverage implies weaker equity positions.  
- **Current Ratio** correlates positively with **Profitability (0.22)** and **Equity (0.61)** — financially sound companies tend to manage liquidity effectively.

### 3. Leverage vs. Profitability Relationship
- A weak but positive regression trend indicates **moderate leverage may improve profitability**, but excessive debt introduces volatility.

---

## 🧮 Outputs & Deliverables

- **Jupyter Notebook:** Full workflow (`notebook.ipynb`)  
- **Visual Reports:**  
  - Sector bar plots  
  - Correlation heatmap  
  - Regression analysis between key ratios  
- **Derived Data Files:**  
  - `analysis_ready_with_ratios.csv`  
  - `sector_summary.csv`  
  - `sector_snapshot_2022.csv`

---

## 🧠 Insights Summary

| Metric | Tech | FMCG | Real Estate |
|:--|:--|:--|:--|
| **Leverage** | Low | Moderate | High |
| **Profitability** | High | Moderate | Variable |
| **Liquidity** | Strong | Stable | Weak |
| **Volatility** | Low | Low | High |

> **Conclusion:**  
> The financial ecosystem from 2018–2022 shows that **sectoral business models drive ratio behavior**.  
> Tech firms are efficient and resilient, FMCG stable and predictable, and Real Estate cyclical but leverage-driven.

---

## 🚀 How to Run the Project

```bash
# Clone the repository
git clone https://github.com/<your-username>/financial-reports-projects.git
cd financial-reports-projects

# Install dependencies
pip install pandas numpy matplotlib seaborn openpyxl

# Open the notebook
jupyter notebook notebook.ipynb
