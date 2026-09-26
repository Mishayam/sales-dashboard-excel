# Sales Dashboard (Excel)

A two-tab Excel workbook (`Sales_Dashboard.xlsx`) that generates synthetic sales data and summarizes it in an interactive dashboard with KPI cards, charts, and slicers.

> **Note:** Source data was generated using `RANDBETWEEN` and related formulas to simulate realistic sales records (not real business data). See "Data Generation" below.

## Structure

- **Data** — raw sales records (Order ID, Date, Region, Product Category, Units Sold, Unit Price)
- **Dashboard** — KPI cards, charts, and interactive slicers (Region / Product Category)

## Functions Used

**Math & Stats**
- `SUM` — total revenue per region
- `AVERAGE` — average order value
- `COUNT` / `COUNTA` — total orders / active sales reps
- `MAX` / `MIN` — highest and lowest single transaction

**Logical & Conditional**
- `IF` — bonus flag for units sold over 50
- `COUNTIF` / `COUNTIFS` — order counts by region
- `SUMIF` / `SUMIFS` — revenue by region + product category

**Lookup & Reference**
- `INDEX` / `MATCH` — highest revenue region lookup
- `VLOOKUP` — pull Unit Price / Region from a typed Order ID

## Data Generation

Synthetic data was created using:
- `INDEX` + `RANDBETWEEN` — random Region and Product Category values
- `RANDBETWEEN(DATE(...), DATE(...))` — random order dates
- `"ORD-" & TEXT(RANDBETWEEN(...), "0000")` — random alphanumeric Order IDs

## Dashboard Features

- KPI cards: Highest Revenue Region, Maximum Orders by Region, Maximum Single Order, Average per Order
- Charts: Revenue by Region (bar), Number of Orders (bar), Units Sold & Revenue by Category/Region (clustered bar), Revenue Share by Region (pie)
- Slicers for Region and Product Category
- Data validation and restricted input ranges to prevent accidental edits to source formulas

## Skills Demonstrated

- Core Excel formulas (SUM, IF, COUNTIF, SUMIF, INDEX/MATCH, VLOOKUP)
- Dashboard design: KPI cards, chart selection, slicers
- Data validation and workbook protection
- Synthetic data generation for testing/demo purposes

## Next Steps

- Apply the same workflow to a real-world, messy dataset (in progress — Kaggle dataset, 1.2M rows, using Python/pandas for cleaning before Excel/Power BI)
