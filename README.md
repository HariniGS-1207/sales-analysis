# sales-analysis
Data analysis project using SQLite, Python, and matplotlib on sales_data.db


This project analyzes a small **sales dataset** stored in SQLite (`sales_data.db`) using **Python, pandas, and matplotlib**.  
It demonstrates how to run SQL queries inside Python, aggregate sales data, and visualize results.

## 📂 Files in this repo
- `task7_sales_analysis.ipynb` — Jupyter/Colab notebook with full code
- `sales_summary_by_product.csv` — aggregated sales & revenue per product
- `sales_revenue_bar.png` — bar chart of revenue by product

## ⚙️ Steps Covered
1. Create `sales` table and insert sample sales records.
2. Run SQL queries:
   - Total quantity sold per product
   - Total revenue per product (`SUM(quantity * price)`)
3. Load SQL results into pandas.
4. Save summary CSV + generate bar chart.

## 🛠 Tools
- Python (pandas, sqlite3, matplotlib)
- Google Colab / Jupyter Notebook
- SQLite database

## 🧾 Example SQL Query
```sql
SELECT product, SUM(quantity * price) AS revenue
FROM sales
GROUP BY product
ORDER BY revenue DESC;

