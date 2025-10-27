IBM Data Analyst Capstone Project
This repository contains my final capstone project for the IBM Data Analyst Professional Certificate. This project simulates a real-world task by performing an end-to-end data analysis pipeline to identify trends in the IT job market.

The primary goal was to collect, clean, and analyze data from diverse sources to answer key questions about in-demand technology skills.


📌 Project Objectives
To identify the most in-demand programming languages, databases, and IDEs.

To determine which skills are correlated with the highest salaries.

To present these findings in an interactive dashboard for stakeholders.

🛠️ Tools & Technologies
Python 3: The core language for all data collection and cleaning.

Data Manipulation: pandas, numpy

Data Collection:

Requests: For querying a jobs API.

BeautifulSoup: For web scraping salary data from a webpage.

Data Visualization: matplotlib, seaborn, plotly

Database: sqlite3 (for running SQL queries on the cleaned data).

BI Tool: IBM Cognos Analytics (for building the final interactive dashboard).

IDE: Jupyter Notebooks / Google Colab

📊 Project Workflow
1. Data Collection
I gathered data from three different sources:

Survey Data: A core .csv file with developer survey responses (m1_survey_data.csv).

API Data: I built and ran a local Flask API (2.a-Jobs_API.ipynb) and then queried it (2.a-Collect Data (API).ipynb) to get the number of job postings for 12 different technologies.

Web Scraping: I used BeautifulSoup to scrape a webpage for data on popular programming languages and their average salaries (2.b-Collect Data (WebScraping).ipynb).

2. Data Wrangling & Cleaning (3-DataWrangling-.ipynb)
This was the most critical step. I loaded the raw 11,552-row survey dataset and:

Identified and removed 154 duplicate rows.

Imputed missing values for WorkWeekHrs and CodeRevHrs using their mean.

Normalized Compensation: Created a new column, NormalizedAnnualCompensation, by converting "Monthly" and "Weekly" salaries to "Yearly" to allow for accurate comparison.

3. Exploratory Data Analysis (EDA) (4-ExploratoryDataAnalysis.ipynb)
I dug into the cleaned data to find initial insights:

Plotted distributions for Age and NormalizedAnnualCompensation (using histograms and box plots).

Identified and analyzed outliers in the compensation data.

Created a correlation matrix to find relationships between variables.

4. Data Visualization & SQL (5-DataVisualization.ipynb)
To answer the key business questions, I loaded the cleaned DataFrame into an in-memory sqlite database and ran SQL queries to aggregate the data. I then used matplotlib to plot the results.

📈 Key Findings & Results
(Replace these with your actual findings from Notebook 5)

Top 5 In-Demand Languages: JavaScript, HTML/CSS, SQL, Python, Java.

Top 5 In-Demand Databases: PostgreSQL, MySQL, SQLite, MongoDB, Microsoft SQL Server.

Salary vs. Language: [Language] and [Language] had the highest median annual salaries.

Dashboard Insights: The final dashboard visualizes all these findings and can be filtered by [Your Filter, e.g., 'Country'] to get specific insights.
