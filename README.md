# IT Job Market Analysis (IBM Data Analyst Capstone)

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-blue?logo=pandas)
![SQL](https://img.shields.io/badge/SQLite-blue?logo=sqlite)
![Seaborn](https://img.shields.io/badge/Seaborn-purple?logo=seaborn)
![IBM Cognos](https://img.shields.io/badge/IBM%20Cognos-gray?logo=ibm)

## 📌 Project Overview

This is the final capstone project for the **IBM Data Analyst Professional Certificate**. The goal was to perform an end-to-end data analysis of the IT job market to identify trends and in-demand skills.

I acted as a data analyst, collecting data from multiple diverse sources (APIs, web scraping, and CSV files), cleaning and wrangling the data, and then analyzing it using SQL and Python. The final insights were compiled into a final report and an interactive business intelligence (BI) dashboard using IBM Cognos.

## 🛠️ Tools & Technologies

* **Data Collection:** `Requests` (for APIs), `BeautifulSoup` (for Web Scraping)
* **Data Wrangling & Analysis:** `Pandas`, `NumPy`
* **Database:** `SQLite` (run directly in the notebook)
* **Data Visualization:** `Matplotlib`, `Seaborn`
* **BI Dashboard:** `IBM Cognos Analytics`

---

## 📊 Project Workflow

The project was broken down into a clear, step-by-step pipeline.

### 1. Data Collection
I gathered data from three separate sources to create a comprehensive dataset:
* **Notebook `1-Explore Data Set.ipynb`:** Loaded and explored the primary developer survey CSV file (`survey.csv`).
* **Notebook `2.a-Collect Data (API).ipynb`:** Queried a live jobs API to collect current job posting numbers for various locations and technologies.
* **Notebook `2.b-Collect Data (WebScraping).ipynb`:** Scraped a webpage to get a list of popular programming languages and their average annual salaries.

### 2. Data Wrangling, EDA & SQL Analysis
This was the core of the project, combined into one main notebook:
* **Notebook `3-Data_Wrangling_and_Visualization.ipynb`:**
    1.  **Loaded** the raw `survey.csv` data.
    2.  **Cleaned Data:** Removed 154 duplicate rows and imputed missing categorical values (`WorkLoc`) using the mode.
    3.  **Normalized Compensation:** Converted weekly and monthly salaries into a single `NormalizedAnnualCompensation` column for accurate comparison.
    4.  **Performed EDA:** Plotted distributions for `Age` and `Compensation` and removed extreme outliers using the IQR method.
    5.  **Loaded to SQL:** Loaded the final, clean DataFrame into an in-memory **SQLite database**.
    6.  **Analyzed with SQL:** Ran SQL queries to aggregate data and answer key business questions (e.g., "Top 5 Education Levels", "Median Salary by Age").
    7.  **Visualized Results:** Plotted the results of the SQL queries directly using Matplotlib and Seaborn.


## 📈 Key Findings (from Dashboard)

The analysis provided several key insights into the IT job market:

* **Top 5 In-Demand Languages:** JavaScript, HTML/CSS, SQL, Bash/Shell/PowerShell, and Python.
* **Top 5 In-Demand Databases:** MySQL, PostgreSQL, Microsoft SQL Server, SQLite, and MongoDB.
* **Future Language Trends:** JavaScript and Python remain top desired languages, with high interest in TypeScript.
* **Future Database Trends:** PostgreSQL and MongoDB show the most growth in developer interest.
* **Demographics:** The field is predominantly male (93.7%), with a large concentration of developers in the 25-35 age range
