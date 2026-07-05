# Airbnb Listings Analysis (SQL + Python)

## Problem Statement
Analyze Airbnb listings data for a chosen city to uncover pricing patterns,
neighborhood trends, and host behavior — the kind of insight a business or
travel platform would use to guide pricing and marketing decisions.

## Dataset
Source: [[Inside Airbnb](http://insideairbnb.com/get-the-data/)](https://www.kaggle.com/datasets/rafaelaaltermann/listings-csv) — free, public data.
1. Download the `listings.csv` file for that city.
2. Place it in the `data/` folder as `listings.csv`.

## Findings

- **Entire homes cost significantly more than shared spaces.** Entire home/apt
  listings average $542/night, more than double a private room ($270) and
  nearly 3x a shared room ($195). Entire homes also dominate the market,
  making up 13,105 of the ~16,600 listings analyzed.

- **New listings are priced higher, not lower.** Counterintuitively, listings
  with zero reviews average $814/night — the highest of any group — while
  price steadily drops as review count increases, down to $342 for listings
  with 50+ reviews. This suggests either overconfident initial pricing from
  new hosts, or that higher-end/luxury properties haven't yet accumulated
  reviews, while established listings compete more aggressively on price.

- **A handful of hosts operate at commercial scale.** The top host manages
  159 listings, and names like "Yes Temporada," "RioHost," and "Anfitriao
  Gente Boa" indicate property management companies rather than individual
  hosts — a sign the market includes both casual hosts and organized rental
  businesses.

- **Data quality issues were identified and handled.** ~15,000 listings had
  missing neighbourhood data and were removed. Extreme price outliers (one
  listing was priced at $562,031/night) were capped at the 99th percentile.
  Some neighbourhood names remain slightly fragmented due to inconsistent
  formatting in the source data (e.g. "Rio De Janeiro, Rj" vs "Rio De
  Janeiro, Rio De Janeiro") — a known limitation rather than a full fix.

## Tools & Skills Demonstrated
SQL (SQLite): aggregation, GROUP BY, HAVING, CASE statements
Python: pandas for data cleaning and outlier handling
Data visualization: matplotlib/seaborn
Data quality: missing value handling, outlier detection, text normalization


