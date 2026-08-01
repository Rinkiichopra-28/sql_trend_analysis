# 📈 SQL Time-Series Trend Engine

A zero-data-movement time-series trend analysis engine built in PostgreSQL that automatically resamples daily data, computes dual-window moving averages (4-week & 12-week), and calculates momentum spread to classify upward, downward, and neutral trends.

##  Live Interactive Demo
You can execute and test this exact SQL query live in your browser:
 **[Run Query on OneCompiler](https://onecompiler.com/postgresql/44wy7dsev)**

---

##  Architecture & Features
* **Time-Bucket Resampling:** Aggregates daily transactional/event logs into clean weekly intervals using `DATE_TRUNC`.
* **Dual Moving Averages:** Computes 4-week (short-term) and 12-week (long-term) rolling averages using SQL window frames (`ROWS BETWEEN N PRECEDING AND CURRENT ROW`).
* **Momentum Spread Indicator:** Measures the percentage deviation between fast and slow moving averages to quantify trend velocity.
* **Automated Trend Classification:** Classifies weekly data points into **Upward**, **Downward**, or **Neutral** trend states.

---

##  Tech Stack
* **Database Engine:** PostgreSQL 15+ (ANSI SQL)
* **SQL Concepts:** Common Table Expressions (CTEs), Window Functions (`OVER`, `ROWS BETWEEN`), Aggregations (`AVG`), Date Arithmetic (`DATE_TRUNC`), and Conditional Logic (`CASE WHEN`).
