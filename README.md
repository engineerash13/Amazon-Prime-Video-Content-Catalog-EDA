# Amazon Prime Video — Content Catalog EDA

An in-depth Exploratory Data Analysis of Amazon Prime Video's content catalog using two datasets — titles metadata (9,871 records) and cast/crew credits (124,235 records). The project uncovers content diversity patterns, genre dominance, regional production trends, IMDb rating distributions, and key contributor analysis to support content strategy and recommendation optimization.

**Author:** Ashwin Suryawanshi | **Type:** Individual Project

---

## Files in This Repository

| File | Description |
|------|-------------|
| `EDA_On_Amazon_Prime_By_Ashwin_Suryawanshi.ipynb` | Full EDA notebook — 2-dataset merge, 5-step data wrangling, 20+ Plotly/Seaborn charts across UBM framework |

---

## Tools & Technologies

- **Python** — Pandas, NumPy
- **Visualization** — Plotly Express, Plotly Graph Objects, Plotly Subplots, Matplotlib, Seaborn
- **Jupyter Notebook** — Google Colab

---

## Datasets

Two datasets merged on `id` for analysis:

**titles.csv — Content Metadata (9,871 records × 15 columns)**

| Column | Description |
|--------|-------------|
| `id` | Unique title identifier |
| `title` | Name of movie or TV show |
| `type` | MOVIE or SHOW |
| `description` | Synopsis |
| `release_year` | Year of release |
| `age_certification` | Age rating (PG-13, R, TV-MA, etc.) — 6,487 missing |
| `runtime` | Duration in minutes |
| `genres` | List of genres |
| `production_countries` | Country/countries of production |
| `seasons` | Number of seasons (TV shows only) — 8,514 missing |
| `imdb_id` | IMDb unique identifier |
| `imdb_score` | IMDb average user rating — 1,021 missing |
| `imdb_votes` | Number of IMDb votes — 1,031 missing |
| `tmdb_popularity` | TMDb popularity score — 547 missing |
| `tmdb_score` | TMDb average rating — 2,082 missing |

**credits.csv — Cast & Crew (124,235 records × 5 columns)**

| Column | Description |
|--------|-------------|
| `person_id` | Unique person identifier |
| `id` | Foreign key linking to titles.csv |
| `name` | Actor or crew member name |
| `character` | Role played by actor — 16,287 missing |
| `role` | ACTOR, DIRECTOR, or WRITER |

---

## Data Wrangling

| Step | Action |
|------|--------|
| 1 | Merged titles.csv and credits.csv on `id` (left join) — created enriched master dataset |
| 2 | Selected 18 key columns for analysis |
| 3 | Removed 56 duplicate rows from credits.csv and 3 from titles.csv |
| 4 | Imputed numerical missing values (imdb_score, tmdb_score, runtime) with median |
| 5 | Dropped rows with missing `description` or `character` (critical columns) |

---

## Charts (20+ — UBM Framework)

### Univariate Analysis
| Chart | Type | Key Insight |
|-------|------|-------------|
| Distribution of IMDb Scores | Histogram + KDE | Roughly normal / slightly right-skewed; most titles cluster in a mid-high range |
| Content Type Distribution | Donut Chart | Shows proportion of Movies vs TV Shows on the platform |
| Top 10 Most Popular Genres | Bar Chart | Reveals dominant genre categories driving the catalog |
| Runtime Distribution | Histogram | Most movies fall within a standard runtime range; TV shows show wider spread |
| Release Year Distribution | Histogram | Content heavily skewed toward recent years (post-2000) |

### Bivariate Analysis
| Chart | Type | Key Insight |
|-------|------|-------------|
| IMDb Score vs TMDb Popularity | Scatter Plot (color by genre) | Weak positive correlation — high scores don't always mean high popularity |
| Content Releases Over Years | Line Chart (by type) | Consistent growth in both Movies and TV Shows; streaming era acceleration post-2015 |
| IMDb Score by Genre | Box Plot | Drama and documentary genres have higher median ratings; comedy has wider spread |
| Top Production Countries | Bar Chart | USA dominates; India, UK, and Japan are secondary producers |
| Genre Trend Over Time | Stacked Area Chart | Drama remains consistently dominant; thriller/crime grew significantly post-2010 |

### Multivariate Analysis
| Chart | Type | Key Insight |
|-------|------|-------------|
| IMDb Score vs Runtime by Content Type | Scatter (colored by type) | Movies with longer runtime tend to score higher; TV shows show less correlation |
| Genre vs Production Country Heatmap | Heatmap | Reveals country-specific genre specializations |
| Rating vs Release Year by Type | Multi-line Chart | Older content tends to have higher IMDb scores (survivor bias) |
| Top Directors by Content Count | Horizontal Bar | Identifies key contributors driving catalog volume |
| Top Actors by Appearance | Horizontal Bar | Maps most prolific actors across the Prime catalog |

---

## Key Insights

- **Movies dominate** the catalog significantly over TV Shows in raw count
- **Drama is the #1 genre** — most frequent and consistently high-rated across years
- **USA is the top producer** by far, followed by India and the UK
- **IMDb and TMDb scores show weak correlation** — platform popularity ≠ critic quality
- **Content releases accelerated sharply post-2015** — streaming era boom clearly visible
- **Older titles score higher on IMDb** — survivor bias means only high-quality older content remains
- **6,487 missing age certifications** — gap in content moderation metadata

---

## Business Recommendations

1. **Expand regional content** — India and South Korea are underserved relative to their audience size
2. **Invest in Drama and Thriller** — highest ratings + consistent viewer demand
3. **Optimize recommendation algorithm** — TMDb popularity and IMDb score should be weighted separately
4. **Fill age certification gaps** — 6,487 missing ratings create content moderation risk
5. **Leverage top-performing directors** — repeat collaborations with high-rated directors drive quality perception

---

## Topics

`eda` `python` `plotly` `seaborn` `amazon-prime` `streaming` `data-analysis` `pandas` `content-analytics` `imdb`
