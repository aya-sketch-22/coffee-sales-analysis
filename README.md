# ☕ Coffee Shop Sales Analysis

Data analysis project exploring one year of coffee shop transaction data (March 2024 – March 2025, 3,600+ transactions) to uncover sales patterns and support data-driven business decisions.

## Tools Used
- Python (Pandas, Matplotlib, Seaborn)
- Google Colab / Jupyter Notebook

## Key Questions Answered
- Which month, weekday, and hour generate the most sales?
- Which menu items are top revenue drivers?
- Do customers pay differently by cash vs. card?
- Is revenue driven by more customers, or by customers spending more per order?

## Key Insights
- **Peak month:** October 2024 (13,891.16 THB) — full-month comparison, excluding incomplete final month of data
- **Best day of week:** Tuesday (18,637.38 THB), notably higher than Sunday (13,858.06 THB)
- **Peak hour:** 10:00 AM (10,994.52 THB)
- **Top-grossing product:** Latte (27,866.30 THB)
- **Revenue driver:** Sales fluctuations (up to 2x month-to-month) were driven primarily by order volume, not average order value — the average price per order stayed stable (~28–34 THB) all year, meaning customer traffic — not upselling — is the key lever for revenue growth
- **Cross-dataset comparison:** A secondary dataset (index_2) with a more premium menu (30 items) had a 17% *lower* average order value than the primary dataset — showing that menu variety alone doesn't guarantee higher spending per customer

## Files
- `coffee_sales_analysis.ipynb` — full analysis notebook, runnable in Google Colab
- `index_1.csv` — primary transaction dataset

## Note on Data Quality
This project includes a deliberate data-quality check: an initial month-over-month grouping incorrectly combined the same calendar month across different years (e.g., March 2024 + March 2025), inflating that month's apparent total. This was caught and corrected by re-grouping on year+month instead of month name alone — a good reminder to always validate groupings against the underlying time dimension.
