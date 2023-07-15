# HackerNews Scraper

This script fetches and saves HackerNews articles from multiple pages. It uses the `requests` library to make HTTP requests, the `BeautifulSoup` library to parse HTML, and the `os` library for file handling.

## Prerequisites

Before running the script, make sure you have the following:

- Python 3.x installed on your system.
- The `requests`, `beautifulsoup4`, and `lxml` libraries installed. You can install them using pip:

  ```
  pip install requests beautifulsoup4 lxml
  ```

## Usage

Follow the steps below to use the script:

1. Save the script in a Python file (e.g., `hackernews_scraper.py`).
2. Open a terminal or command prompt.
3. Navigate to the directory where the script is saved.
4. Run the script using the following command:

   ```
   python hackernews_scraper.py
   ```

5. The script will prompt you to enter the number of pages you want to fetch from HackerNews (maximum 20 pages).
6. Enter the desired number of pages and press Enter.
7. The script will then ask if you want verbose output. Enter `y` for verbose output or `n` for silent mode.
8. The script will start fetching the articles from each page and save them in the "HackerNews" directory.
9. For each page, a text file named "NewsPageX.txt" will be created (where X is the page number), containing the articles and their details.
10. Once the script has finished fetching all the pages, it will exit.

## Additional Information

The script checks if the "HackerNews" directory exists in the current working directory. If it doesn't exist, the script creates it using `os.makedirs()`.

The `fetch()` function is responsible for fetching the articles from a given page. It uses `requests.get()` to retrieve the page content and `BeautifulSoup` to parse the HTML. The articles' details (such as rank, title, URL, author, score, etc.) are extracted and written to a text file using `open()` and `write()`.

The main part of the script uses a loop to iterate through each page number and calls the `fetch()` function for each page. It also handles input validation and ensures the number of pages entered is within the limit.

You can modify the script according to your requirements, such as changing the directory name, modifying the text file format, or customizing the information extracted from the HackerNews pages.

Note: Scraping websites might be subject to the website's terms of service. Make sure you comply with the terms and use this script responsibly.