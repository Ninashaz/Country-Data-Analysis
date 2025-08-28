
# 🌍 Excel Data Analysis: Country Metrics Dashboard

**Author:** Nina  
**Project:**  Dynamic Country Data Analysis

A sophisticated Microsoft Excel dashboard that performs dynamic data analysis on a global country dataset. This project demonstrates advanced Excel functionalities, including dynamic arrays, powerful lookup functions, and automated ranking, to solve complex data queries.

## 🚀 Demonstrated Skills

This project showcases proficiency in:

*   **Dynamic Arrays:** Mastery of modern Excel functions like `FILTER`, `SORT`, and `XLOOKUP` that spill results automatically.
*   **Data Validation:** Creating user-friendly dropdown lists for interactive data selection.
*   **Advanced Lookups:** Using `XLOOKUP` for robust and flexible data retrieval, superior to traditional VLOOKUP.
*   **Complex Criteria Filtering:** Isolating datasets based on multiple conditions (e.g., unemployment rate, GDP comparison to average).
*   **Statistical Analysis:** Calculating global averages and performing comparative analysis (e.g., ±5% GDP range).
*   **Data Ranking:** Automatically assigning and updating ranks within a dataset.
*   **Structured References:** Using Excel Table syntax for formulas that are easy to read and maintain.

## 📊 Project Overview & Solutions

The workbook is built to solve specific analytical tasks :

### 1. Main Data Table (`Table2`)
Created a comprehensive table serving as the project's database with the following fields for numerous countries:
*   `Country Name`
*   `Capital/Major City`
*   `Population`
*   `Area (km²)`
*   `Abbreviation`
*   `Calling Code`
*   `GDP`
*   `Unemployment Rate`

### 2. Interactive Country Lookup (XLOOKUP)
*   **Feature:** A dynamic dropdown list allows users to select any country.
*   **Solution:** Used `Data Validation` to create the dropdown and an `XLOOKUP` formula to instantly retrieve and display all corresponding information (Capital, Population, GDP, etc.) for the selected country.
*   **Formula Preview:** `=XLOOKUP(Selected_Country, Table2[Country], Table2[[Capital]:[Unemployment Rate]], "Not Found")`

### 3. Dynamic List: Low Unemployment Countries
*   **Task:** Generate a list of countries with an unemployment rate of 10% or less.
*   **Solution:** Used the `FILTER` function to extract countries that meet the criteria `(Unemployment Rate <= 0.1)`. The `SORT` function orders the results neatly.
*   **Output:** A dynamic array displaying Country Name, Capital, and Unemployment Rate.

### 4. Dynamic List: Countries Above Average GDP
*   **Task:** Identify all countries with a GDP higher than the global average.
*   **Solution:** A `FILTER` function is used with a criteria that compares each country's GDP to the calculated global average `(GDP > AVERAGE(Table2[GDP]))`.
*   **Output:** A self-updating array showing Country Name, Capital, and GDP.

### 5. GDP Ranking
*   **Task:** Automatically assign a rank to each country based on its GDP within the main table.
*   **Solution:** Used the `RANK` function with structured references to compare each row's GDP against the entire GDP column.
*   **Formula Implemented:** `=RANK(Table2[@[GDP]], Table2[GDP])` is placed in a dedicated `Rank` column within `Table2`, providing an always-up-to-date leaderboard.

### 6. Find Countries with Similar GDP
*   **Task:** For a user-selected country (e.g., Iran), find all countries with a GDP within a ±5% range.
*   **Solution:** This is a two-step process:
    1.  An `XLOOKUP` retrieves the GDP of the selected country from the dropdown.
    2.  A powerful `FILTER` function is used to find all countries where the GDP is between 95% and 105% of the selected country's GDP `(GDP >= Selected_GDP*0.95, GDP <= Selected_GDP*1.05)`.
*   **Output:** A dynamic list of countries meeting the criteria, effectively showing economic peers.

## 🛠️ Technical Implementation

| Task | Key Function(s) Used | Description |
| :--- | :--- | :--- |
| **Data Lookup** | `XLOOKUP`, `Data Validation` | Robust search and retrieval of country data. |
| **Dynamic Filtering** | `FILTER` | Extracting specific subsets of data based on logical conditions. |
| **Sorting Data** | `SORT` | Organizing output in an ascending or descending order. |
| **Statistical Analysis** | `AVERAGE`, `RANK` | Calculating global metrics and ranking data points. |
| **Formula Logic** | Comparison Operators (`<`, `>`, `<=`, `>=`), Arithmetic (`*`, `%`) | Building complex criteria for filtering and calculations. |



<img width="1012" height="694" alt="Screenshot 2025-08-27 at 18 50 52" src="https://github.com/user-attachments/assets/ce2fb5cb-c50e-4d9f-9d84-b7f88e471e4b" />


## 🌟 Purpose

This project was designed to transform static data into an interactive analytical tool. It goes beyond basic Excel knowledge, demonstrating the ability to solve real-world data problems using efficient, powerful, and modern techniques essential for data analysis, business intelligence, and financial modeling roles.
