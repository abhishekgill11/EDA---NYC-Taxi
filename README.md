# NYC Yellow Taxi Analytics | Python

An end-to-end data analytics project exploring NYC Yellow Taxi trip patterns, fare behavior, tipping trends, and geographic activity using Python.

The project transforms raw taxi trip data into analytical insights through data cleaning, exploratory data analysis, geographic analysis, and data visualization.

---

## Project Overview

New York City's taxi industry generates large volumes of trip data containing information about pickup and drop-off locations, trip distances, fares, payment methods, and timestamps.

This project analyzes NYC Yellow Taxi trip records from 2023 to understand:

* When taxi pickup activity is highest.
* How trip distance and duration relate to fare amounts.
* Which pickup and drop-off zones experience the most activity.
* How fare per mile varies across distance categories, time periods, and vendors.
* How tipping behavior differs across payment methods.
* How additional charges vary by location and time.

The objective is to demonstrate practical data analytics skills and communicate meaningful findings from real-world transportation data.

## Business Questions

1. When is taxi demand highest, and how does it vary across weekdays and months?
2. How do trip distance and duration relate to fare amounts?
3. Which pickup and drop-off zones generate the most activity?
4. How do fare-per-mile and tipping patterns vary across different trip characteristics?
5. What operational observations can be drawn from the analysis?

## Dataset

**Source:** NYC Taxi & Limousine Commission (TLC) — Yellow Taxi Trip Records.

**Period:** January–December 2023.

The project uses a sampled dataset for exploratory analysis.

| Dataset stage                                  | Records |
| ---------------------------------------------- | ------: |
| Initial sampled dataset                        | 265,487 |
| Cleaned dataset                                | 260,308 |
| Final dataset after extreme-distance filtering | 260,301 |

Additional geographic information was obtained from the NYC Taxi Zone shapefile to associate location IDs with zone names and boroughs.

**Note:** The analysis is based on sampled records and should not be interpreted as a complete count of all NYC Yellow Taxi trips.

## Technology Stack

| Technology       | Purpose                        |
| ---------------- | ------------------------------ |
| Python           | Data analysis and processing   |
| Pandas           | Data cleaning and manipulation |
| NumPy            | Numerical operations           |
| Matplotlib       | Data visualization             |
| Seaborn          | Statistical visualization      |
| GeoPandas        | Geographic data processing     |
| Jupyter Notebook | Exploratory data analysis      |

## Project Workflow

```text
Raw Taxi Trip Data
        |
        v
Data Loading and Inspection
        |
        v
Data Cleaning and Preprocessing
        |
        v
Exploratory Data Analysis
        |
        v
Temporal and Financial Analysis
        |
        v
Geographic Analysis
        |
        v
Operational and Pricing Analysis
        |
        v
Business Insights and Reporting
```

## Exploratory Data Analysis

### 1. Temporal Analysis

Examined pickup activity across different time periods.

Analyses include:

* Hourly pickup distribution.
* Pickup activity by day of the week.
* Monthly pickup trends.

**Key observations:**

* Pickup activity reaches its highest level around 6 PM.
* Early morning hours, particularly 4–5 AM, show relatively low activity.
* Thursday records the highest pickup count among weekdays.
* May records the highest monthly pickup count, while September records the lowest.

### 2. Financial and Fare Analysis

Investigated fare behavior and the relationship between trip characteristics and pricing.

Analyses include:

* Fare and trip distance relationships.
* Fare and trip duration relationships.
* Monthly and quarterly revenue patterns.
* Fare per mile by passenger count.
* Fare per mile by hour and day.
* Fare per mile by vendor.
* Fare per mile across distance categories.

**Key observation:**

Median fare per mile decreases as trip distance increases.

| Distance category     | Vendor 1 | Vendor 2 |
| --------------------- | -------: | -------: |
| Very short (≤1 mile)  |    10.20 |    10.12 |
| Short (1–2 miles)     |     7.60 |     7.72 |
| Medium (2–5 miles)    |     6.10 |     6.25 |
| Long (5–10 miles)     |     5.59 |     5.49 |
| Very long (>10 miles) |     4.00 |     4.02 |

The two vendors show broadly similar fare-per-mile patterns across distance categories.

### 3. Geographic Analysis

Integrated taxi trip records with NYC Taxi Zone geographic information.

Analyses include:

* Pickup activity by zone and borough.
* Drop-off activity by zone and borough.
* Pickup-to-drop-off ratios.
* Overnight pickup and drop-off patterns.
* Daytime and nighttime revenue distribution.
* Route-level trip analysis.

**Key observation:**

The analysis identified 9,437 unique pickup-to-drop-off routes. Route speeds varied considerably, with slower observed trip speeds concentrated around Manhattan locations.

### 4. Operational and Customer Analysis

Explored trip characteristics and customer payment behavior.

Analyses include:

* Passenger counts by time and pickup zone.
* Route-speed analysis.
* Tip percentage by payment type.
* Low-tip versus high-tip trip comparisons.
* Additional charges by zone and time.

**Key observations:**

* Card-payment trips show higher observed tipping percentages than trips associated with other payment types.
* Median additional charges vary by pickup zone.
* Airport-related pickup zones show higher median additional charges than many other analyzed locations.

## Repository Structure

```text
nyc-yellow-taxi-analysis/
│
├── data/
│   └── README.md
│
├── notebooks/
│   └── taxi_eda.ipynb
│
├── README.md
└── requirements.txt
```

## How to Explore the Project

1. Clone or download this repository.
2. Install the required Python dependencies.
3. Open the Jupyter Notebook.
4. Review the data cleaning and exploratory analysis sections.

Install Python dependencies:

```bash
pip install pandas numpy matplotlib seaborn geopandas jupyter
```

Dataset files are not necessarily included in this repository. Refer to the NYC TLC data source and the data documentation before running the notebook.

## Key Skills Demonstrated

* Data cleaning and preprocessing.
* Exploratory data analysis.
* Statistical and descriptive analysis.
* Temporal trend analysis.
* Geographic data analysis.
* Data visualization.
* Business-oriented analytical thinking.

## Data Source

NYC Taxi & Limousine Commission (TLC):

https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

NYC Taxi Zone Maps and Shapefiles:

https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

---


