# Vendor Performance Analysis - Retail Inventory & Sales

_Analyzing vendor efficiency and profitability to support strategic purchasing and inventory decisions using SQL, Python.

---

## Table of Contents
- <a href="#overview">Overview</a>
- <a href="#business-problem">Business Problem</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#project-structure">Project Structure</a>
- <a href="#data-cleaning--preparation">Data Cleaning & Preparation</a>
- <a href="#exploratory-data-analysis-eda">Exploratory Data Analysis (EDA)</a>
- <a href="#research-questions--key-findings">Research Questions & Key Findings</a>
- <a href="#final-recommendations">Final Recommendations</a>
- <a href="#author-contact">Author & Contact</a>

---
<h2><a class="anchor" id="overview"></a>Overview</h2>

This project evaluates vendor performance and retail inventory dynamics to drive strategic insights for purchasing, pricing, and inventory optimization. A complete data pipeline was built using SQL for ETL, Python for analysis, and hypothesis testing.

---
<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>

Effective inventory and sales management are critical in the retail sector. This project aims to:
- Identify underperforming brands that require promotional or pricing adjustments.
- Determine vendors' contributions to sales and profit.
- Analyze the impact of bulk purchasing on unit costs.
- Assess inventory turnover to reduce holding costs and improve efficiency.
- Investigate the profitability variance between high-performing and low-performing vendors.

---
<h2><a class="anchor" id="dataset"></a>Dataset</h2>

- Multiple CSV files located in '/data/' folder (sales, vendors, inventory).
- Summary table created from ingested data and used for analysis.

---
<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

- SQL (Common Table Expressions, Joins, Filtering)
- Python (Pandas, Numpy, Matplotlib, Seaborn, SciPy)
- GitHub

---
<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>

'''
vendor-performance-analysis/
|
|--README.md
|--.gitignore
|--requirements.txt
|--Vendor Performance Report.pdf
|
|--notebokks/                  # Jupyter notebooks
|   |--vendor_performance_db.ipynb
|   |--vendor_performance_analysis.ipynb
'''

---
<h2><a class="anchor" id="data-cleaning--preparation"></a>Data Cleaning & Preparation</h2>

- Removed transactions with:
    - Gross Profit > 0
    - Profit Margin > 0
    - Sales Quantity = 0
- Created summary tables with vendor-level metrics
- Converted data types, handled outliers, merged lookup tables

---
<h2><a class="anchor" id="exploratory-data-analysis-eda"></a>Exploratory Data Analysis (EDA)</h2>

**Negative or Zero Values Detected:**
- Gross Profit: Min. -52.002.78 (loss-making sales)
- Profit Margin: Min -$ \infty $ (sales at 0 or below cost)
- Unsold Inventory: Indicating slow-moving stock

**Outliers Identification:**
- High Freight Costs (up to 257K)
- Large Purchase/Actual Prices

**Correlation Analysis:**
- Weak between Purchase price 7 Profit
- Strong between Purchase Qty & Sales Qty (0.999)
- Negative between Profit Margin & Sales Price (-0.179)

---
<h2><a class="anchor" id="research-questions--key-findings"></a>Research Questions & Key Findings</h2>

1. **Brands for Promotions:** 198 brands with low sales but high profit margins
2. **Top Vendors:** Top 10 vendors = 65.69% of purchases --> risk of over-reliance
3. **Inventory Turnover:** $2.71M worth of unsold inventory
4. **Bulk Purchasing Impact:** 72% cost savings per unit in large orders
5. **Vendor Profitability:**
    - High vendors: Mean Margin = 31.17%
    - Low Vendors: Mean Margin = 51.55%
6. **Hypothesis Testing:** Statistically significant difference in profit margins --> distinct vendor strategies

---
<h2><a class="anchor" id="final-recommendations"></a>Final recommendations</h2>

- Diversify vendor base to reduce risk
- Optimize bulk order strategies
- Reprice slow-moving, high-margin brands
- Clear unsold inventory strategically
- Improve marketing for under-performing vendors

---
<h2><a class="anchor" id="author-contact"></a>Author & Contact</h2>

**Suraj Kr. Paswan**

Email: suraj.work711@gmail.com  
LinkedIn: [https://www.linkedin.com/in/surajpaswan]


