# Uber Trip Data: ETL Pipeline, BigQuery, and Dashboarding with Looker


## Overview
This project demonstrates an end-to-end ETL pipeline for processing and analyzing New York City's Taxi and Limousine Commission (TLC) trip data. The workflow starts from data cleaning in Jupyter, followed by using MAGE (an open-source ETL tool) to extract, transform, and load the data to Google BigQuery. A dashboard is then created using Looker to visualize and analyze the data. 

The dataset was sourced from the [NYC TLC Trip Record Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page).


![Uber_data_model drawio](https://github.com/user-attachments/assets/369ed4f0-d21a-4df0-9621-081c88b55cf0)

![Uber_ETL_pipeline](https://github.com/user-attachments/assets/781b6130-74ba-44ac-a97a-cadfcd24c96c)


## Key Components
1. **Data Cleaning**: Initial data cleaning was done using Jupyter Notebook, which involved handling missing values, correcting data types, and removing unnecessary columns from the raw dataset.
   
2. **ETL Pipeline with MAGE**:
   - **Extract**: The cleaned dataset was uploaded to a cloud storage solution (e.g., Google Cloud Storage).
   - **Transform**: Data transformations were performed using MAGE to prepare the dataset for analysis.
   - **Load**: Transformed data was loaded into a Google BigQuery instance for efficient querying and analysis.

3. **BigQuery**: The data in BigQuery is structured to allow optimized query execution for analysis and reporting. SQL queries are used to explore and extract insights from the dataset.

4. **Visualization using Looker**: A custom dashboard was created in Looker to visualize key metrics from the TLC trip data. It includes charts and graphs for:
   - Number of trips over time
   - Trip distances
   - Passenger counts
   - Payment methods
   - Popular pick-up and drop-off locations

## Prerequisites
To replicate this project, you need the following tools:
- Python (for data cleaning in Jupyter)
- MAGE (ETL tool)
- Google Cloud (for BigQuery and Cloud Storage)
- Looker (for dashboard creation)

## Installation and Setup

### 1. Virtual Machine SSH
```bash
sudo apt-get update
sudo apt-get install python3-distutils
sudo apt-get install wget
sudo apt install python3-pip
python3 -m venv myenv
sudo apt install python3-venv
source myenv/bin/activate
python3 -m venv myenv
source myenv/bin/activate
python3 -m pip install --upgrade pip
python3
quit()
pip3 install pandas
pip3 install mage-ai
pip3 install google-cloud
pip install google-cloud-bigquery
pip install db-dtypes
mage start uber_shubham_project
