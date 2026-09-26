# Walmart Sales Analysis & Dashboard 🛒📊

End-to-end analysis of 10,000+ Walmart transaction records — from raw data cleaning
in Python to an interactive Power BI dashboard — covering sales trends, category
performance, payment behavior, and profit over time.

## 📌 Objective
- Clean and enrich raw transaction data (pricing, dates, ratings)
- Identify sales, profit, and rating trends across categories, branches, and time
- Build an interactive dashboard for business stakeholders to explore the data live

## 🛠️ Tools & Libraries
- **Python** Pandas, NumPy, Matplotlib, Seaborn (cleaning & EDA)
- **Power BI**  interactive dashboard & visual reporting

## 🧹 Data Cleaning & Feature Engineering (Python)
- Removed 31 rows with missing `unit_price`/`quantity`
- Dropped 51 duplicate transactions
- Parsed `date` and `time` into proper datetime types
- Stripped `$` from `unit_price` and cast to numeric
- Engineered new features: `Year`, `Day` (weekday), `Day_shifts` (Morning/Afternoon/Evening)
- Derived `Sales` (`unit_price × quantity`) and `profit` (`Sales × profit_margin`)
- Exported the cleaned, enriched dataset to Excel for use in Power BI

## 📊 Key Findings (Python EDA)

| Question | Finding |
|---|---|
| Best-rated category | **Food & Beverages**, followed by Sports & Travel |
| Lowest-rated categories | Fashion Accessories and Home & Lifestyle — flagged for improvement |
| Most used payment method | **Credit card**, followed by Ewallet |
| Busiest transaction day | **Tuesday**, followed by Sunday |
| Busiest time of day | **Evening**, followed by Afternoon |
| Sales trend 2019–2023 | Sharp drop after 2019, never recovered to prior levels; profit tracked the same pattern |
| Top revenue categories | **Fashion Accessories** and **Home & Lifestyle** drive most sales and profit |

## 📈 Power BI Dashboard

![Walmart Dashboard](images/walmart_dashboard.png)

The dashboard includes:
- **KPI cards** total profit, total sales
- **City/Branch filters** for interactive drill-down
- **Sales over year** trend
- **Category ratings** (min/avg/max) table
- **Busiest day** and **shift-based transaction volume**
- **Payment method breakdown** by transaction count and quantity
- **Total profit by category**

> 💡 To explore the dashboard interactively, download `walmart_sales_dashboard.pbix`
> and open it in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free).

## 🚀 How to Run the Analysis
```bash
git clone https://github.com/jobinjosej253/walmart-sales-dashboard.git
cd walmart-sales-analysis
pip install pandas numpy matplotlib seaborn openpyxl
jupyter notebook notebooks/walmart_data_analysis.ipynb
```

## 📂 Repo Structure
```
├── Walmart.csv
├── Walmart_formatted_data.xlsx
├── walmart_data_analysis.ipynb
├── walmart_sales_dashboard.pbix
├── images/
│ └── walmart_dashboard.png
└── README.md
```

## 📄 License
MIT
