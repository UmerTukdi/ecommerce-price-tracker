# Book Catalog Scraper and Price Analysis

A Python project that collects book titles, listed prices, and star ratings from the Books to Scrape practice website, then explores the captured catalogue with Pandas and Matplotlib.

## Overview

The scraper visits the first three catalogue pages and extracts:

- Book title
- Listed price
- Star rating

The collected records are saved to `data/products.csv`. A separate Jupyter Notebook loads that CSV and analyses the price and rating distributions.

## Repository Contents

| Path | Description |
| --- | --- |
| `scrapar.ipynb` | Scrapes catalogue pages and writes the CSV |
| `data/products.csv` | Saved product records |
| `analysis.ipynb/analysis.ipynb` | Exploratory analysis and visualizations |

## Analysis

The analysis notebook calculates:

- Number of collected products.
- Average, minimum, and maximum listed price.
- Distribution of prices.
- Distribution of ratings.
- Average listed price by rating.

Prices are retained in the currency supplied by the source website (GBP). Ratings are stored as categorical values such as `One` through `Five`.

## Run Locally

Requires Python 3.9 or later and an internet connection for the scraping step.

```bash
git clone https://github.com/UmerTukdi/ecommerce-price-tracker.git
cd ecommerce-price-tracker

python -m venv .venv
```

Activate the environment:

```bash
# Windows
.venv\Scripts\activate

# macOS / Linux
source .venv/bin/activate
```

Install dependencies and launch Jupyter:

```bash
pip install requests beautifulsoup4 pandas matplotlib notebook
jupyter notebook
```

Run `scrapar.ipynb` to refresh `data/products.csv`. Then open `analysis.ipynb/analysis.ipynb` to review the analysis.

## Scope and Limitations

This is a one-time catalogue scraping and analysis exercise against a practice website. It does not yet maintain historical price snapshots, schedule recurring checks, monitor live retail products, or send price alerts. The saved CSV is a snapshot of the records collected when the scraper was last run.
