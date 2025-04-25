# 🚀 Exoplanet Exploration Project

## 📜 Overview
This project showcases data retrieval from NASA's Exoplanet Archive API and web scraping of Wikipedia's "List of Potentially Habitable Exoplanets." The goal is to explore and compare exoplanet data from two different sources, analyze the differences, and practice working with APIs and web scraping techniques in Python.

## 🔧 Project Breakdown

### 1. **API Data: NASA Exoplanet Archive**
- **Goal**: Query the NASA Exoplanet Archive API to retrieve data about exoplanets discovered after 2015.
- **Endpoint**: `https://exoplanetarchive.ipac.caltech.edu/TAP/sync`
- **Key Information Retrieved**:
  - Planet name, host star, discovery method, discovery year, orbital period, radius, mass
- **Steps**:
  1. Send a request to the API with a SQL-style query.
  2. Convert the JSON response into a pandas DataFrame.
  3. Save the data as a CSV file for easy analysis.

### 2. **Web Scraping: Wikipedia - Potentially Habitable Exoplanets**
- **Goal**: Scrape the Wikipedia page "List of Potentially Habitable Exoplanets" to get data about exoplanets that might have conditions suitable for life.
- **Table of Interest**: The main table on the Wikipedia page contains information about the planets' name, discovery date, star, distance, and habitability.
- **Steps**:
  1. Use `pandas.read_html()` to scrape the table directly from the Wikipedia page.
  2. Save the scraped data as a CSV file for further analysis.

## 🔎 Results & Analysis

- The API data from NASA’s Exoplanet Archive provides structured data, which includes precise scientific measurements such as orbital period, mass, and radius.
- The Wikipedia scraping provides a list of potentially habitable exoplanets, along with details like discovery year and distance, but may lack some of the precision found in the API data.

### 📉 Challenges & Lessons Learned
- **API Query**: Structuring SQL queries to return the desired data was straightforward, but filtering by discovery year allowed me to narrow down relevant results.
- **Web Scraping**: Extracting tables from Wikipedia was easy with `pandas.read_html()`, but sometimes the page structure can change, requiring us to adjust the index of the correct table.

## 📚 References
- [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/)
- [Wikipedia - List of Potentially Habitable Exoplanets](https://en.wikipedia.org/wiki/List_of_potentially_habitable_exoplanets)