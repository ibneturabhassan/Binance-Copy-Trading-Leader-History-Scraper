# Binance Copy Trading Leader History Scraper

## Overview

This repository contains a Python notebook designed to scrape and process the trading history of a copy trading leader on Binance. It is structured to first gather data from the Binance API, and then convert the collected JSON data into a more accessible CSV format. This tool is particularly useful for anyone interested in analyzing the performance and strategies of successful traders on Binance's platform.

## How it Works

### Data Collection

The script uses the `requests` library to make POST requests to Binance's API. It targets the endpoint `https://www.binance.com/bapi/futures/v1/public/future/copy-trade/lead-portfolio/trade-history` to retrieve the trading history of a specified copy trading leader.

- **Pagination Handling:** The script iterates over pages of data, collecting a predefined number of entries per page.
- **Data Storage:** Retrieved data is stored in a combined list, ensuring a comprehensive collection from all pages.

### Data Conversion

After collecting the data, the script then converts the JSON data into a CSV format. This step is crucial for making the data more accessible and easier to analyze using various data analysis tools.

- **CSV Format:** The script creates a CSV file with the same structure as the JSON data, allowing for seamless integration into data analysis workflows.

## Setup

1. **Clone the Repository:** Start by cloning this repository to your local machine or development environment.
2. **Install Dependencies:** Ensure you have Python installed along with the `requests` library. You can install the required libraries using `pip`:
   ```
   pip install requests
   ```
3. **Run the Notebook:** Open the notebook in your preferred Python environment and execute the cells sequentially.

## Usage

- **Specify the Leader:** Update the `portfolioId` in the payload to the ID of the copy trading leader you wish to analyze.
- **Run the Script:** Execute the script to start the data collection process. Data will be saved in `combined_list_data.json`.
- **Convert to CSV:** Run the CSV conversion part of the script to get a CSV file named `combined_list_data.csv`.

---

> Note: This tool is intended for educational and research purposes only. Always adhere to Binance's terms of service when using their API.
