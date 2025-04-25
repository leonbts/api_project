# 🚀 Exoplanet Exploration Project

## 📜 Overview
This project showcases data retrieval from NASA's Exoplanet Archive API and web scraping of Wikipedia's "List of Potentially Habitable Exoplanets." The goal is to explore and compare exoplanet data from two different sources, analyze the differences, and practice working with APIs and web scraping techniques in Python.

### 🛠️ Tools and Libraries
- **Python 3.x**
- **Pandas**: Data manipulation
- **Requests**: HTTP requests to retrieve data from the API
- **BeautifulSoup** (optional, for more complex scraping): For HTML parsing
- **Jupyter Notebook**: Interactive environment for coding

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

## 💻 How to Run

1. Clone this repository to your local machine.
    ```bash
    git clone https://github.com/your-username/exoplanet-exploration.git
    ```

2. Install the necessary Python libraries:
    ```bash
    pip install requests pandas
    ```

3. Run the Jupyter Notebook:
    ```bash
    jupyter notebook your_project_notebook.ipynb
    ```

4. View the output CSV files in the `output/` folder:
    - `output/exoplanets.csv`: Data from the NASA Exoplanet Archive API
    - `output/wikipedia_habitable_exoplanets.csv`: Data scraped from Wikipedia

## 🔎 Results & Analysis

- The API data from NASA’s Exoplanet Archive provides structured data, which includes precise scientific measurements such as orbital period, mass, and radius.
- The Wikipedia scraping provides a list of potentially habitable exoplanets, along with details like discovery year and distance, but may lack some of the precision found in the API data.

### 📉 Challenges & Lessons Learned
- **API Query**: Structuring SQL queries to return the desired data was straightforward, but filtering by discovery year allowed me to narrow down relevant results.
- **Web Scraping**: Extracting tables from Wikipedia was easy with `pandas.read_html()`, but sometimes the page structure can change, requiring us to adjust the index of the correct table.
- **Data Cleaning**: Both sources required minimal cleaning, but ensuring the formats (e.g., numerical data) were consistent across datasets was important for comparison.

## 🌱 Next Steps & Future Work
- Integrating other data sources, like other space agencies' exoplanet data, for a more comprehensive analysis.
- Visualizing the data with charts using libraries like `matplotlib` or `seaborn`.
- Exploring more advanced web scraping techniques (e.g., handling dynamic content with `Selenium`).

## 📚 References
- [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/)
- [Wikipedia - List of Potentially Habitable Exoplanets](https://en.wikipedia.org/wiki/List_of_potentially_habitable_exoplanets)