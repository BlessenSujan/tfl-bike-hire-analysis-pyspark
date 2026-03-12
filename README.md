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
