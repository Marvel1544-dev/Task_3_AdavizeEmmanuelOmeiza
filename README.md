# Books Web Scraping Project

A Python web-scraping project that collects book information from [Books to Scrape](https://books.toscrape.com/) and saves the results as a CSV dataset.

## Features

- Scrapes book titles, prices, ratings, and availability.
- Uses BeautifulSoup to parse the website's HTML.
- Uses pandas to organize the scraped data and display basic statistics.
- Stores the collected data in `books_dataset.csv`.

## Project Files

- `web_scraping.py` — Python script that scrapes book data and performs basic data analysis.
- `books_dataset.csv` — Sample dataset generated from the scraped book information.

## Requirements

- Python 3.8 or later
- `requests`
- `pandas`
- `beautifulsoup4`

Install the dependencies with:

```bash
pip install requests pandas beautifulsoup4
```

## Usage

Run the scraper from the project directory:

```bash
python web_scraping.py
```

The script prints the scraped book details and summary information in the terminal. To save a new dataset, extend the script to export the pandas DataFrame to `books_dataset.csv` using `df.to_csv("books_dataset.csv", index=False)`.

## Dataset Columns

| Column | Description |
| --- | --- |
| `title` | Title of the book |
| `price` | Listed price of the book |
| `rating` | Star rating represented as a word, such as `One` or `Five` |
| `availability` | Stock availability shown on the website |

## Data Source

The data is collected from [Books to Scrape](https://books.toscrape.com/), a website intended for web-scraping practice and learning.

## Notes

This project is for educational purposes and demonstrates basic web scraping, data cleaning, and exploratory analysis with Python.
