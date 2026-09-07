# dia-market-data-visualization
Java application for collecting DIA market prices and visualizing price changes over time using Python.

# DIA Market Data Visualization

## Overview

This project was developed as part of a Forage job simulation. It demonstrates how Java can be used to retrieve financial market data from the Twelve Data API, store collected data points in a queue, and visualize DIA price changes over time using Python.

## Project Objectives

- Retrieve the latest DIA market price using the Twelve Data API.
- Capture the timestamp for each data point.
- Store market data in a Java queue.
- Retrieve data every 15 seconds.
- Process the collected data using Python.
- Create a line graph showing DIA price changes over time.

## Technologies Used

- Java
- Python
- Google Colab
- Twelve Data API
- Pandas
- Matplotlib
- Git & GitHub

## Project Workflow

Twelve Data API
        ↓
Java Application
        ↓
DIA Price + Timestamp
        ↓
Java Queue
        ↓
Collected Data
        ↓
Python
        ↓
Pandas DataFrame
        ↓
Matplotlib Line Graph

## Java Implementation

The Java application uses:

- `HttpClient` to communicate with the Twelve Data API.
- `Queue` to store market data points.
- `Instant` to capture timestamps.
- A custom `PriceRecord` class to represent each data point.

## Data Visualization

Python is used to extract the price and timestamp values from the Java application's output.

The resulting visualization displays:

- X-axis: Timestamp
- Y-axis: DIA Price

## Security

The Twelve Data API key is stored using an environment variable and is not included in the repository.

Example:

```python
os.environ["TWELVE_DATA_API_KEY"] = getpass("Enter your Twelve Data API key: ")
