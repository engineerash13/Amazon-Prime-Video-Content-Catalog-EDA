# 🎬 Amazon Prime Video — Exploratory Data Analysis

> **Uncovering content trends, viewer preferences, and regional insights from Amazon Prime's catalog of 9,000+ titles**

---

## 📌 Project Overview

With the rapid expansion of the streaming industry, Amazon Prime Video has established itself as one of the leading global platforms. This project performs an **in-depth Exploratory Data Analysis (EDA)** on Amazon Prime's content catalog to uncover key patterns, evaluate content diversity, and analyze viewer ratings — ultimately enabling smarter, data-driven content strategy decisions.

---

## 🗂️ Dataset Description

The analysis is based on **two interconnected datasets**:

| Dataset | Records | Description |
|---|---|---|
| `titles.csv` | 9,871 rows × 15 columns | Metadata for all movies & TV shows |
| `credits.csv` | 124,235 rows × 5 columns | Cast & crew mapped to each title |

### Key Features

**titles.csv** — Show type, genres, production countries, IMDb scores, release years, runtime, age certification, TMDb popularity

**credits.csv** — Actor/director names, roles, character names, linked to title IDs

---

## 🎯 Business Objective

| Stakeholder | Objective |
|---|---|
| Content Team | Identify high-performing genres for acquisition |
| Engineering | Improve recommendation algorithm accuracy |
| Marketing | Target campaigns by audience age & geography |
| Strategy | Recognize underserved regional markets |

---

## 🔍 Analysis Workflow

```
Data Loading → Data Cleaning → EDA → Visualization → Insights → Business Recommendations
```

### Phases Covered

1. **Know Your Data** — Shape, dtypes, first look
2. **Data Wrangling** — Handling missing values, removing duplicates, feature extraction
3. **Univariate Analysis** — Individual variable distributions
4. **Bivariate Analysis** — Cross-variable relationships (Num-Cat, Num-Num, Cat-Cat)
5. **Multivariate Analysis** — Heatmaps, pair plots, combined trend charts

---

## 📊 Key Visualizations & Insights

### 🎞️ Content Distribution
- **Movies dominate** the platform over TV Shows, indicating a film-first content strategy
- Content releases show a **strong upward trend post-2015**, peaking in recent years

### 🌍 Regional Insights
- **USA, India, and UK** are the top content-producing countries
- Significant underrepresentation of content from **South America and Africa** — an opportunity for platform expansion

### 🎭 Genre Analysis
- **Drama, Comedy, and Action** are the most common genres
- Niche genres tend to carry **higher average IMDb scores**, suggesting quality over quantity
- Genre trends over time show the **rise of thriller and documentary content**

### ⭐ Ratings & Quality
- IMDb score distribution is **right-skewed** — most content clusters between 5.5–7.5
- **Box plots by genre** reveal which genres consistently outperform others in critical reception
- Age certification analysis shows **TV-MA and R-rated content** dominate, informing adult-focused marketing

### 🎬 Contributor Analysis
- Top directors and actors are mapped to their content's performance metrics
- A small group of **prolific contributors** accounts for a disproportionately large portion of high-rated titles

### 🔗 Correlation Findings
- Moderate **positive correlation** between TMDb popularity and IMDb votes
- Runtime shows **minimal impact** on IMDb scores — quality trumps length

---

## 🛠️ Tech Stack

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px
import plotly.graph_objects as go
from plotly.subplots import make_subplots
```

| Library | Purpose |
|---|---|
| Pandas & NumPy | Data manipulation |
| Matplotlib & Seaborn | Static visualizations |
| Plotly | Interactive charts |

---

## 📁 Project Structure

```
Amazon-Prime-EDA/
├── EDA_On_Amazon_Prime_By_Ashwin_Suryawanshi.ipynb
├── titles.csv
├── credits.csv
└── README.md
```

---

## 💡 Business Recommendations

- **Content Acquisition:** Prioritize genres with consistently high IMDb scores and underrepresented regions
- **Recommendation Engine:** Leverage correlations between TMDb popularity and IMDb votes for better suggestions
- **Original Content:** Invest in high-scoring niche genres for differentiation from competitors
- **Regional Expansion:** Africa and South America remain significantly underserved — a growth opportunity

---

## 👨‍💻 Author

**Ashwin Suryawanshi**
*EDA Capstone Project | Individual Contribution*

> 📌 Amazon Prime Video — Exploratory Data Analysis on Content Trends, Viewer Ratings & Regional Insights

---

## 📜 License

This project is for educational and analytical purposes only.
