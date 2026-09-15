# Superstore Sales — Exploratory Data Analysis

Exploratory data analysis of the Superstore sales dataset, done in Python on Google Colab.

## About the Dataset

The dataset (`train.csv`) contains 9,800 retail orders with the following information:

- **Order details**: Order ID, Order Date, Ship Date, Ship Mode
- **Customer info**: Customer ID, Customer Name, Segment
- **Location**: Country, City, State, Postal Code, Region
- **Product info**: Category, Sub-Category, Product Name
- **Sales**: Sales value per order

## What This Notebook Covers

- Data cleaning (date parsing, missing values, duplicates)
- Univariate analysis — distribution of sales, order counts by segment/category/region
- Bivariate analysis — sales by category, segment, sub-category, and state
- Time trends — monthly sales, yearly sales by category, sales by day of week
- Correlation analysis between numeric features
- Shipping performance by ship mode

## Tools Used

- Python (pandas, numpy)
- Matplotlib & Seaborn (static visualizations)
- Plotly (interactive visualizations)
- missingno (missing data visualization)
- Google Colab

##  Repository Contents

```
├── superstore-eda-colab.ipynb   # Main analysis notebook
├── train.csv                    # Dataset
└── README.md                    # This file
```

## How to Run

1. Clone this repo
2. Open `superstore-eda-colab.ipynb` in [Google Colab](https://colab.research.google.com)
3. Upload `train.csv` when prompted, or place it in the same folder if running locally
4. Run all cells (Runtime → Run all)

## Key Findings

- **Total sales**: ~$2.26M across 4,922 unique orders (Jan 2015 – Dec 2018)
- **Technology** is the top-selling category ($827K), narrowly ahead of Furniture ($729K) and Office Supplies ($705K)
- **Phones** and **Chairs** are the highest-revenue sub-categories, each bringing in over $320K
- **Consumer** is the dominant segment, generating more sales ($1.15M) than Corporate and Home Office combined
- **West** and **East** regions lead in sales; **California** and **New York** are the top two states by a wide margin
- **Standard Class** is by far the most-used shipping method (60% of orders) and also the slowest, averaging ~5 days — **Same Day** shipping (0 days) is rare, used in only ~5% of orders
- Sales are noticeably higher on **weekends** (Saturday/Sunday) and lower midweek, with **Thursday** the slowest day
- Sales trend upward year over year, peaking in **November 2018** ($118K) — consistent with a holiday shopping spike
- Individual order values are skewed: the average order is ~$231, but the median is only ~$54, meaning a small number of large orders pull the average up
