# TfL Cycle Hire Data Analysis Using PySpark

## Overview
This project analyzes the Transport for London (TfL) Cycle Hire dataset using Apache Spark and PySpark. The goal is to explore ride durations, clean the dataset, and perform statistical analysis to understand usage patterns.

The project demonstrates how big data tools such as Apache Spark can be used for efficient data processing and analysis.

## Dataset
The dataset is obtained from the TfL Open Data portal:

https://cycling.data.tfl.gov.uk/

The dataset contains detailed information about bike hire trips including:

- Ride duration
- Start station
- End station
- Start time
- End time

This project uses the **2014 cycle hire dataset**.

## Technologies Used

- Python
- Apache Spark
- PySpark
- Google Colab
- Pandas
- Matplotlib
- SciPy

## Spark Setup

Apache Spark is installed and initialized in a local environment:

- Java installation
- Spark installation
- SparkContext initialization
- SparkSession configuration

The project uses Spark in **local mode** for data processing.

## Data Processing

The following steps were performed:

1. Download the dataset from TfL Open Data
2. Extract ZIP files
3. Load CSV files into a Spark DataFrame
4. Combine multiple CSV files
5. Inspect schema and dataset structure
Example:

```python
bike = spark.read.csv(csv_files, header=True, inferSchema=True)

## Data Cleaning

The dataset was cleaned using several preprocessing steps to improve data quality and reliability.

Cleaning steps included:

- Removing missing values
- Removing duplicate records
- Converting ride duration to integer format
- Filtering invalid ride durations
- Removing rides longer than **9000 seconds (2.5 hours)**

The ride duration was also converted from **seconds to minutes** for easier interpretation and analysis.

---

## Data Analysis

Key statistical analyses were performed on the cleaned dataset, including:

- Minimum ride duration
- Maximum ride duration
- Mean ride duration
- Duration distribution statistics
- Skewness of ride duration

These statistics help understand the general usage patterns of the bike hire system.

---

## Case Study: Baylis Road Waterloo Station

A focused analysis was conducted on rides starting from **Baylis Road, Waterloo Station**.

Steps included:

- Filtering rides starting from Baylis Road station
- Separating rides from other stations
- Calculating the average ride duration
- Comparing ride duration patterns with other stations

This case study helps identify station-specific usage behavior.

---

## Hypothesis Testing

A statistical **t-test** was performed to determine whether the average ride duration at **Baylis Road Waterloo Station** is significantly different from rides starting at other stations.

### Hypotheses

**Null Hypothesis (H₀):**  
There is no difference in average ride duration between Baylis Road station and other stations.

**Alternative Hypothesis (H₁):**  
Rides starting from Baylis Road station have shorter average durations than rides from other stations.

The statistical analysis was performed using the **SciPy** library.

---

## Visualization

A bar chart visualization was created to compare:

- Average ride duration at **Baylis Road Waterloo Station**
- Average ride duration at **other stations**

This visualization helps clearly illustrate the differences in ride duration between the two groups.

---

## Results

The analysis provides insights into ride duration behavior and station-level usage patterns in London's bike-sharing system. The findings help understand how ride durations vary across stations and whether specific stations exhibit different usage patterns.

---

## Repository Structure
README.md
tfl_bike_analysis_pyspark.ipynb
data/
results/
figures/

```python
bike = spark.read.csv(csv_files, header=True, inferSchema=True)
