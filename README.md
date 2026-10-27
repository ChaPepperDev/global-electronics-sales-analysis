# Global Electronics Retailer Sales Analysis

![Global Electronics Retailer Dashboard](images/dashboard.png)

## Project Overview

This project analyzes sales data from a global electronics retailer to identify revenue trends, product performance, sales-channel distribution, seasonality, and geographic patterns.

The data was cleaned, transformed, and analyzed using **Python**, **Pandas**, and **Matplotlib**. An interactive dashboard was then developed in **Power BI**, with **DAX** measures used to present the main business indicators and insights.

The project covers sales data from 2016 to February 2021.

> **Note:** 2021 contains only partial data through February 20, 2021 and should not be directly compared with complete years.

## Business Questions

The analysis was designed to answer the following questions:

- How did revenue evolve over time?
- Which product categories generate the most revenue?
- Which products perform best in terms of revenue and units sold?
- Are there seasonal patterns in sales?
- How does online revenue compare with physical-store revenue?
- Which countries and physical stores generate the most revenue?

## Tools and Technologies

- Python
- Pandas
- Matplotlib
- Jupyter Notebook
- Power BI
- DAX
- Git
- GitHub

## Data Source

The project uses the **Global Electronics Retailer** dataset from the Maven Analytics Data Playground.

- **Dataset:** [Global Electronics Retailer](https://mavenanalytics.io/data-playground/global-electronics-retailer)
- **Source:** Microsoft
- **License:** Public Domain
- **Dataset size:** 62,884 transaction records across multiple related tables

The original dataset contains information about:

- Sales
- Products
- Stores
- Customers
- Exchange rates

A data dictionary is included in the `docs` directory.

The main source tables used directly in the Python analysis were:

- `Sales.csv`
- `Products.csv`
- `Stores.csv`

The processed dataset used in Power BI is available at:

`data/processed/sales_cleaned.csv`

## Data Preparation

The main data preparation steps included:

- Inspection of dataset structure and data types
- Missing-value analysis
- Duplicate validation
- Date conversion
- Product data cleaning
- Store data integration
- Sales and product table joins
- Revenue calculation
- Creation of year and month variables
- Identification of online and physical-store sales
- Export of the cleaned dataset for Power BI

The final analytical dataset contains **62,884 sales line items**.

## Key Metrics

| Metric | Value |
|---|---:|
| Total Revenue | $55.76M |
| Total Orders | 26.33K |
| Units Sold | 197.76K |
| Unique Customers | 11.89K |
| Average Order Value | $2.12K |
| Online Revenue Share | 20.45% |

## Key Insights

### Revenue Trend

Revenue increased between 2016 and 2019, reaching its highest level in **2019**.

A significant decline was observed in 2020.

The 2021 result represents only a partial year and should therefore not be directly compared with previous full-year results.

### Product Categories

**Computers** generated the highest revenue among all product categories, followed by **Home Appliances**.

**Games and Toys** generated the lowest revenue during the analyzed period.

### Product Performance

Desktop computers dominated the ranking of highest-revenue products.

The analysis also showed that products with lower sales volume can still generate significant revenue when their unit price is substantially higher.

### Seasonality

Using only complete years from 2016 to 2020, **December** generated the highest accumulated revenue.

February and January also performed strongly, while March and especially April showed weaker results.

### Sales Channels

Physical stores accounted for approximately **79.55%** of total revenue.

Online sales represented approximately **20.45%** of total revenue.

This indicates that physical retail remained the company's primary sales channel during the analyzed period.

### Geographic Performance

The **United States** was the strongest market among physical-store locations.

Nine of the ten highest-revenue physical stores were located in the United States.

The highest-performing individual store was located in **Nevada**.

## Power BI Dashboard

The Power BI dashboard provides an interactive view of the main business indicators and allows users to filter the analysis by:

- Year
- Country
- Sales Channel

The dashboard includes:

- Total Revenue
- Total Orders
- Units Sold
- Unique Customers
- Average Order Value
- Online Revenue Share
- Revenue by Year
- Revenue by Category
- Top 10 Products by Revenue
- Revenue by Sales Channel

The dashboard shown at the top of this README was built from the processed dataset exported by the Python notebook.

## Project Structure

```text
global-electronics-sales-analysis/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   └── global_electronics_sales_analysis.ipynb
│
├── data/
│   ├── raw/
│   │   ├── Sales.csv
│   │   ├── Products.csv
│   │   ├── Stores.csv
│   │   ├── Customers.csv
│   │   └── Exchange_Rates.csv
│   │
│   └── processed/
│       └── sales_cleaned.csv
│
├── docs/
│   └── Data_Dictionary.csv
│
└── images/
    └── dashboard.png
```

## How to Run the Project

Clone the repository:

```bash
git clone https://github.com/ChaPepperDev/global-electronics-sales-analysis.git
```

Navigate to the project directory:

```bash
cd global-electronics-sales-analysis
```

Install the Python dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
notebooks/global_electronics_sales_analysis.ipynb
```

Run all cells from top to bottom.

The notebook automatically reads the source datasets from `data/raw/` and exports the processed analytical dataset to `data/processed/sales_cleaned.csv`.

## Conclusion

This project demonstrates an end-to-end data analytics workflow, from raw-data inspection and cleaning to exploratory analysis, business KPI development, and interactive visualization.

The analysis identified **Computers** as the strongest product category, showed that revenue peaked in **2019**, highlighted clear seasonal patterns, and confirmed the continued dominance of physical-store sales.

The project also demonstrates practical use of **Python, Pandas, Matplotlib, Power BI, DAX, Git, and GitHub** in a reproducible portfolio project.
