# Airbnb Listings Analysis (SQL + Python)

## Problem Statement
Analyze Airbnb listings data for a chosen city to uncover pricing patterns,
neighborhood trends, and host behavior — the kind of insight a business or
travel platform would use to guide pricing and marketing decisions.

## Dataset
Source: [Inside Airbnb](http://insideairbnb.com/get-the-data/) — free, public data.
1. Go to the site, pick a city (e.g. London, NYC, or Kuala Lumpur if available).
2. Download the `listings.csv` file for that city.
3. Place it in the `data/` folder as `listings.csv`.

## Tools
- **SQLite** — lightweight database to practice real SQL
- **Python (pandas)** — load data into SQL, pull results back out
- **matplotlib / seaborn** — visualizations

## How to Run
1. Install requirements:
   ```
   pip install -r requirements.txt
   ```
2. Load the CSV into a SQLite database:
   ```
   python setup_database.py
   ```
3. Run the analysis (executes SQL queries + generates charts):
   ```
   python analysis.py
   ```
4. Charts will be saved into the `charts/` folder.

## Project Structure
```
airbnb-analysis/
├── data/               # put listings.csv here
├── charts/             # generated output charts
├── setup_database.py   # loads CSV into SQLite
├── queries.sql         # all SQL queries used in analysis
├── analysis.py         # runs queries, cleans data, makes charts
├── requirements.txt
└── README.md
```

## Key Questions Explored
- Which neighborhoods have the highest average listing price?
- How does room type (entire home / private room / shared room) affect price?
- Which hosts have the most listings?
- How do prices vary by review score / number of reviews?

## Findings
*(Fill this in after running the analysis — e.g. "Neighborhood X has the
highest average price at $Y, but Neighborhood Z offers similar ratings for
30% less, suggesting it's undervalued.")*

Add 3-4 bullet points here with your actual numbers and 1-2 chart screenshots
once you've run it on real data. This section is what recruiters read first.
