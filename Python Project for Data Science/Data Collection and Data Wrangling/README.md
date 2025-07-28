🔹 Module 1: Data Collection and Data Wrangling
This first module of the Python Project course was the perfect step into practical data science. The main focus was learning how to collect data from different sources and transform it into a usable form. Unlike earlier courses, here the tasks were hands‑on and project‑oriented, so I had to put my skills into action.

The technologies and libraries used were Pandas, NumPy, Requests, BeautifulSoup, and APIs. We started with collecting CSV and Excel files using Pandas’ read_csv() and read_excel(), and I also learned to set parameters like header, index_col, and usecols to control how the data loads. Then we moved into working with APIs, where I used the requests library to fetch JSON data from endpoints. Parsing JSON using Python’s built‑in .json() method gave me structured dictionaries that I could easily convert into Pandas DataFrames.

A highlight for me was web scraping with BeautifulSoup. I learned how to fetch an HTML page, parse the structure, and extract tabular data from <table> tags. Writing code like:

> `python code
>  import requests
>  from bs4 import BeautifulSoup
>  page = requests.get("https://example.com")
>  soup = BeautifulSoup(page.text, "html.parser")
>  tables = soup.find_all("table")
helped me understand how flexible Python is for extracting unstructured data.

Once the data was collected, the next step was data wrangling. I applied Pandas techniques to clean and organize the dataset:

Handling missing values using .fillna() and .dropna()

Changing data types with .astype()

Removing duplicates with .drop_duplicates()

Creating new calculated fields (e.g., ratios or growth percentages)

Renaming and reordering columns for clarity

This module is intermediate level because it assumes you already know Python basics and Pandas, but it pushes you to combine those skills creatively. Personally, I found this module exciting because I wasn’t just following examples — I was building my own data pipeline. It felt like the moment where everything I’d learned in the past few courses clicked together.

What I found most useful was learning how to automate data collection. Instead of manually downloading CSVs, I could now call an API or scrape a website and refresh my dataset whenever I needed. That’s a professional skill I know companies expect in real projects.

After completing this module, I gained confidence in:

Using APIs to fetch live data

Scraping websites for information not available in CSVs

Wrangling messy data into clean, structured DataFrames

Documenting each step in Jupyter so others can follow my logic

Overall, this module trained me not just to use data, but to go out and get it, clean it, and make it analysis‑ready — which is the heart of any real data science project. It was challenging at times (especially debugging scraping code), but it gave me a serious upgrade in technical skills and confidence.
