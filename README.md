# End-to-End-ELT-Project-Netflix-Data-Cleaning-Analysis-with-Python-and-SQL

# 🎬 Netflix ELT Data Pipeline — Python & SQL

This project demonstrates a complete **ELT (Extract, Load, Transform)** pipeline using the popular **Netflix dataset**. It showcases how raw data can be processed, structured, and analyzed using **Python** and **SQL**, mimicking real-world data engineering and analytics workflows.

---

## 📌 Project Overview

- **Extract** the raw Netflix dataset
- **Load** it into a relational database (e.g., MySQL or PostgreSQL)
- **Transform** and query the data using SQL to generate actionable insights

---

## 🔧 Tech Stack

- **Python**: Pandas, SQLAlchemy/pyodbc
- **SQL**: MySQL / PostgreSQL / SQLite (choose your flavor)
- **Jupyter Notebook** (for interactive analysis)
- **VS Code / Any IDE**

---

## 📈 Workflow Summary

### 1️⃣ Extract  
- Download the Netflix dataset in CSV format.
- Use Pandas to load and inspect the dataset.

### 2️⃣ Load  
- Set up the database schema for Netflix content data.
- Use `SQLAlchemy` or `pyodbc` to connect and insert data into the database.

### 3️⃣ Transform & Analyze  
- Use SQL queries to:
  - Count movies vs TV shows
  - Identify most frequent genres or directors
  - Analyze content trends over years
  - Filter content by country, rating, or release year

---

## 💡 Learning Objectives

- Understand the principles of ELT pipelines
- Perform data cleaning and formatting in Python
- Learn how to move data into SQL databases programmatically
- Use SQL to answer real-world business questions

---

## 🧪 Example SQL Queries

```sql
-- Number of movies and TV shows
SELECT type, COUNT(*) FROM netflix_titles GROUP BY type;

-- Top 5 countries by number of Netflix titles
SELECT country, COUNT(*) AS total FROM netflix_titles GROUP BY country ORDER BY total DESC LIMIT 5;

-- Most common genres
SELECT listed_in, COUNT(*) FROM netflix_titles GROUP BY listed_in ORDER BY COUNT(*) DESC;
