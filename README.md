# Data-Engineering-Project-Beginner-
Extract API Data and Store in CSV

## Goal
Fetch data from a public API and save it to a CSV file.

## Tools
- Python
- requests
- csv

## Example APIs
- Anime quotes
- Weather data
- News headlines

## Introduction
This project demonstrates how to extract data from a public API and store it in a CSV file using Python. 

## Prerequisites
- Python 3.x
- requests library: `pip install requests`

## Installation
1. Clone the repository:
    ```sh
    git clone https://github.com/KhidirSuhaimi/Data-Engineering-Project-Beginner-.git
    ```
2. Navigate to the project directory:
    ```sh
    cd Data-Engineering-Project-Beginner-
    ```

## Usage
1. Run the script:
    ```sh
    python fetch_data.py
    ```
2. The data will be saved in a file named `output.csv`.

## Example
Here is an example of how to fetch anime quotes and save them to a CSV file:
```python
import requests
import csv

response = requests.get('https://example.com/api/anime-quotes')
data = response.json()

with open('output.csv', mode='w') as file:
    writer = csv.writer(file)
    writer.writerow(['Quote', 'Character'])
    for item in data:
        writer.writerow([item['quote'], item['character']])
