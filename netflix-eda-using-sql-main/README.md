#  Netflix EDA Using SQL

![Project Logo](https://github.com/Priyanshupriyadarshi29/netflix-eda-using-sql/blob/main/logo.png)

A deep dive into Netflix’s content catalog through **15+ SQL-powered business queries**—analyzing content types, genres, trends, and global distribution to uncover data-driven insights.

---

##  Project Highlights

- SQL-based Exploratory Data Analysis (EDA) on Netflix titles.
- Focused on deriving business insights from real-world querying.
- No external libraries—just powerful, efficient SQL logic.

---

##  Dataset Info

- **Source**: [Kaggle – Netflix Titles](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- **File**: `netflix_titles.csv`
- Contains: `title`, `type`, `country`, `release_year`, `rating`, `genres`, `cast/director`, `description`, and more.

---

##  Schema Definition (Schemas.sql)

```sql
CREATE TABLE netflix (
    show_id      VARCHAR(10),
    type         VARCHAR(20),
    title        VARCHAR(255),
    director     VARCHAR(255),
    casts        TEXT,
    country      VARCHAR(255),
    date_added   VARCHAR(50),
    release_year INT,
    rating       VARCHAR(10),
    duration     VARCHAR(20),
    listed_in    TEXT,
    description  TEXT
);
```

---

##  Business Questions & SQL Solutions

| Question | Query Highlights |
|---------|-------------------|
| 1 | Movies vs TV Shows count |
| 2 | Most frequent rating per content type |
| 3 | Top 5 countries by content volume |
| 4 | Most featured actors/directors |
| 5 | Genre-wise distribution |
| 6 | Longest duration titles |
| 7 | Recently added content (last 5 years) |
| 8 | Classify 'Good' vs 'Bad' using keywords like 'kill' or 'violence' |
| 9 | Year with highest average releases in India |
|10 | Salman Khan’s appearances in the past decade |

> All queries are available in `Solutions of 15 business problems.sql`.

---

##  A Sample SQL Query

**Top 5 countries with most Netflix content**

```sql
SELECT TRIM(country) AS country,
       COUNT(*) AS total_content
FROM netflix
WHERE country IS NOT NULL
GROUP BY country
ORDER BY total_content DESC
LIMIT 5;
```

---

##  File Overview

| File | Purpose |
|------|---------|
| `netflix_titles.csv` | Raw Netflix metadata |
| `Schemas.sql` | Table schema creation |
| `Business Problems Netflix.sql` | The list of business questions |
| `Solutions of 15 business problems.sql` | SQL query solutions |
| `logo.png` | Repository branding |
| `README.md` | This project overview |

---

##  Key Insights

- Movies dominate the catalog over TV shows.
- The United States and India lead Netflix content volume.
- Popular genres include Documentaries, Dramas, and Comedies.
- Content breadth has grown steadily in recent years.
- Descriptive keywords can flag content sentiment (e.g., via 'kill' or 'violence').

---

##  How to Get Started

1. Clone the project:
   ```bash
   git clone https://github.com/Priyanshupriyadarshi29/netflix-eda-using-sql.git
   cd netflix-eda-using-sql
   ```

2. Set up your SQL environment (SQLite, PostgreSQL, MySQL, etc.).

3. Use `Schemas.sql` to create the necessary table structure.

4. Import the dataset into your database.

5. Execute the solution queries in `Solutions of 15 business problems.sql`.

---

##  About Me

Hi, I'm **Priyanshu Priyadarshi**—a data analysis enthusiast passionate about SQL-powered insights and storytelling through data.

- GitHub: [@Priyanshupriyadarshi29](https://github.com/Priyanshupriyadarshi29)  

---


