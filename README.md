# Predicting the Trend of Imported Cars in Thailand

This Jupyter Notebook (`sec2-group8.ipynb`) analyzes car sales data from a CSV file (`2024-2025car.csv`) to study trends in sedan registrations in Thailand for 2565–2567 (2022–2024). It focuses on sedans (not more than 7 passengers) and examines brands like TESLA, BYD, NETA, DEEPAL, and ORA.

## CSV Data

The CSV contains:

- **Columns**: Year, Month, Types of Cars, Brands, Car Model, Amount  
- **Data**: Sales of sedans from various brands, with `Amount` indicating units sold.

## How the Code Works

### Data Preparation:

- Loads the CSV using `pandas` and filters for sedans.
- Cleans data: ensures `Amount` is numeric, standardizes `Brands` (uppercase, no whitespace).
- Splits data by year (2565, 2566, 2567).

### Visualization:

- Defines a function to create pie charts showing the top 10 brands by sales for each year using `matplotlib`.
- Displays sales distribution for sedans.

### EV Brand Analysis:

- Filters for electric vehicle (EV) brands: **TESLA, BYD, NETA, DEEPAL, ORA**.
- Aggregates sales by year and brand, calculating year-over-year (YoY) growth rates.
- Plots sales trends as a line graph.
- Computes total EV sales and market share for these brands within the sedan category.

## Outputs:

- Pie charts for top 10 brands per year.
- Table of total sales by year and brand.
- YoY growth rates for EV brands.
- Total EV sales and market share table.
- Line plot of EV brand sales trends (`sales_trends.png`).

## Requirements

- Python 3.x  
- Libraries: `pandas`, `matplotlib`, `statsmodels`

## Usage

1. Place `2024-2025car.csv` in the same directory as the notebook.
2. Run the notebook cells to process data, generate visualizations, and display results.

## Notes

- The CSV must have the expected columns: `Year`, `Month`, `Types of Cars`, `Brands`, `Car Model`, `Amount`.
- The code handles errors like missing files or incorrect formats using `try-except` blocks.
- Thai font support (`TH Sarabun New`) is configured for visualizations.
