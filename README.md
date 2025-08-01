# movie-box-office-analysis

#  Movie Box Office Analysis — BOM + IMDb

##  Project Overview

This data science project combines **Box Office Mojo (BOM)** and **IMDb** data to explore what kinds of films perform best at the box office. We aim to identify key features (such as genres, runtime, ratings) that influence domestic and international gross revenue. Our findings will support business decisions around film production and marketing.

---

## 🗂 Data Sources

- **Box Office Mojo (BOM)** — Domestic and foreign gross, release year, movie titles.
- **IMDb Database (SQL)** — Title info, genres, runtime, ratings, votes.

The two datasets were merged on matching **title** and **year/start_year** fields after cleaning.

---

##  Data Cleaning

- Removed rows with missing critical data (title, year, gross, genre).
- Cleaned numeric columns by removing non-numeric characters and converting to floats.
- Extracted primary genres from multi-genre strings.
- Converted gross figures to millions for easier interpretation.
- Joined datasets using inner merge on `title` and `year`.

---

##  Exploratory Data Analysis (EDA)

- Most frequent genres by count and total revenue.
- Distribution of gross income by genre and runtime.
- Runtime vs. revenue trends.
- Correlation between IMDb ratings and revenue.
- Top-performing titles by worldwide gross.

>  See full visualizations and insights in the [`notebooks/movie_analysis.ipynb`](notebooks/movie_analysis.ipynb).

---

##  Business Recommendations

1.  **Invest in Action and Adventure films** — These genres consistently generate the highest worldwide revenue.
2.  **Target runtime between 100–130 minutes** — Films in this range show stronger box office performance on average.
3.  **Balance domestic and foreign strategies** — Some films make most of their revenue internationally; targeting global markets is key.

---

##  Tableau & Exports

The cleaned, merged dataset is available in `data/merged_movies_data.csv` and can be imported directly into Tableau for dashboarding.

---

##  Tools Used

- **Python**: pandas, matplotlib, seaborn, sqlite3
- **SQL**: Queries to extract relevant data from IMDb database
- **Jupyter Notebook**: Exploratory analysis and data cleaning
- **PowerPoint**: Business presentation
- **Tableau**: Optional for advanced visualization

---
