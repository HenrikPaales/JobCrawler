# Job Crawler

## Overview

This Python script is a job crawler designed to fetch job listings based on specific criteria from the CV-Online job portal (https://cv.ee/et/). The script utilizes web scraping techniques to extract relevant information such as job title, company, location, salary, and expiry date from the job listings. The extracted data is then stored in a CSV file for further analysis or reference.

## Requirements

Make sure you have the following Python libraries installed:

- BeautifulSoup: Used for parsing HTML content.
- requests: Used for making HTTP requests.
- urllib: Used for URL manipulation.
- csv: Used for handling CSV files.

You can install these libraries using the following command:

```bash
pip install beautifulsoup4 requests
```

## Usage

1. Clone the repository:

```bash
git clone <repository_url>
cd <repository_directory>
```

2. Open the Jupyter Notebook:

```bash
jupyter notebook Job_Crawler.ipynb
```

1. Execute the cells in the notebook.

Alternatively, you can run the Jupyter Notebook directly in Google Colab by clicking the following link:

[Open in Google Colab](https://colab.research.google.com/github/HenrikPaales/JobCrawler/blob/main/Job_Crawler.ipynb)

The script will fetch job listings based on the provided parameters, and you can execute the cells in Colab just like in a local Jupyter environment.
```

Users can simply click the "Open in Google Colab" link to access and run the notebook in Google Colab.

The script will fetch job listings based on the provided parameters and store the results in a CSV file named "JobList.csv".

## Configuration

You can customize the job search criteria by modifying the parameters in the script. The current parameters are set to search for jobs related to Terraform, with a limit of 1300 results, including remote work options.

```python
# Query parameters
params = {
    "limit": "1300",
    "offset": "0",
    "keywords[0]": "terraform",
    "fuzzy": "true",
    "towns[0]": "312",
    "suitableForRefugees": "false",
    "isRemoteWork": "true",
    "isHourlySalary": "false",
    "isQuickApply": "false",
    "sorting": "LATEST",
}
```

Adjust these parameters according to your specific job search requirements.

## Results

The script will generate a CSV file named "JobList.csv" with columns for job title, URL, company, location, salary, and expiry date. The file will be overwritten each time the script is executed.

## Disclaimer

This script is intended for educational and personal use only. Ensure that you comply with the terms of service of the targeted website, and consider the impact of your web scraping activities on the website's performance and server load. Use responsibly and ethically.