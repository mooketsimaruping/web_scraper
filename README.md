# Web Scraper and Data Visualizer

This Jupyter Notebook provides a Python script for web scraping product data from an eBay webpage and visualizing it using matplotlib. The script is organized into two main classes: `WebScraper` and `DataVisualizer`.

## Web Scraper

### WebScraper Class

The `WebScraper` class is responsible for scraping product data from a specified eBay webpage. Here's how it works:

#### Initialization

```python
web_scraper = WebScraper(url)
```

You need to create an instance of the `WebScraper` class by providing the URL of the eBay webpage you want to scrape.

#### Scraping Data

```python
data = web_scraper.scrape_data()
```

The `scrape_data()` method sends an HTTP request to the provided URL, extracts product information such as name, price, and number of reviews, and returns this data as a list of dictionaries.

## Data Visualizer

### DataVisualizer Class

The `DataVisualizer` class helps you visualize the scraped data using matplotlib. Here's how to use it:

#### Visualization

```python
DataVisualizer.visualize_data(data)
```

The `visualize_data(data)` method takes the scraped data as input and creates two bar charts. One chart shows product prices, and the other shows the number of reviews for each product.

## Running the Script

To run the script, make sure you have installed the required libraries (`requests`, `beautifulsoup4`, `pandas`, and `matplotlib`) in your Python environment. You can run the script as follows:

1. Set the `url_to_scrape` variable to the eBay webpage URL you want to scrape.

```python
url_to_scrape = 'https://www.ebay.com/b/PC-Laptops-Netbooks/177/bn_317584'
```

2. Execute the script.

The script will perform the following steps:

- Send an HTTP request to the specified eBay webpage.
- Extract product data.
- Create bar charts for product prices and reviews.
- Display the charts in the Jupyter Notebook.

If no valid data is found on the webpage, a message will be displayed indicating that there is no data to visualize.

Please ensure that you have a stable internet connection, as the script relies on internet access to fetch data from the eBay webpage.

