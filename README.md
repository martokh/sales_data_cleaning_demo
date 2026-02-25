## Sales Data Cleaning Demo

This project is a portfolio-ready demo that cleans a messy retail sales dataset, validates data quality, computes KPIs, and prepares an Excel-first dashboard.

### Project structure

- `data/raw/` – original Kaggle file (`kaggle_original.csv`) and intentionally messy input (`messy_raw.csv`).
- `data/processed/` – cleaned outputs, KPI tables, validation summary, and data dictionary.
- `notebooks/01_sales_cleaning.ipynb` – main, end-to-end notebook (inspection → cleaning → validation → KPIs → exports).
- `outputs/` – Excel dashboard file and optional chart PNGs.
- `screenshots/` – placeholders for portfolio screenshots (raw issues, validation summary, dashboard, KPI table).

### How to run

1. Create and activate a Python environment with at least:
   - `pandas`, `numpy`, `matplotlib`, `openpyxl`, `jupyter`.
2. From the project root:
   ```bash
   jupyter notebook notebooks/01_sales_cleaning.ipynb
   ```
3. Run all cells from top to bottom.  
   This will generate:
   - `data/processed/cleaned_sales.csv`
   - `data/processed/validation_summary.csv`
   - `data/processed/kpi_table.csv`
   - `data/processed/rev_by_month.csv`
   - `data/processed/top_products.csv`
   - `data/processed/rev_by_region.csv`
   - `data/processed/data_dictionary.txt`
   - `outputs/sales_dashboard.xlsx`

### Excel dashboard

Open `outputs/sales_dashboard.xlsx` and:

- Use sheet `Cleaned_Data` as the source table.
- Build KPI cards for:
  - Total Revenue
  - Total Orders
  - Average Order Value (AOV)
  - Invalid Rows Removed
- Build three charts on sheet `Dashboard`:
  - Revenue by Month (line) – from `rev_by_month.csv`.
  - Top 10 Products by Revenue (bar) – from `top_products.csv`.
  - Top 10 Regions by Revenue (bar) – from `rev_by_region.csv`.
