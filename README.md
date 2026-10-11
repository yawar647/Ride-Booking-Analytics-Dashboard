# Ride-Booking Analytics Dashboard

## Project Overview

The **Ride-Booking Analytics Dashboard** is an interactive business intelligence project developed using Microsoft Power BI to analyze sample ride-booking data.

The dashboard provides insights into booking trends, booking value, trip distance, trip duration, vehicle preferences, payment methods, and pickup and drop-off locations.

The project transforms raw ride-booking data into meaningful visual insights through key performance indicators (KPIs), interactive charts, dynamic measure selection, and location-based analysis. It demonstrates how data analytics and visualization can support informed business decisions.

## Business Objectives

- Analyze ride-booking trends and booking value over time.
- Evaluate trip efficiency using distance and duration metrics.
- Compare booking performance across payment methods and trip types.
- Identify popular vehicle types and high-demand locations.
- Analyze pickup and drop-off patterns to understand location-based demand.
- Present business metrics through an interactive dashboard.

## Dashboard Features

### 1. Overview Analysis

The overview dashboard summarizes key metrics used to evaluate ride-booking performance.

**Key Performance Indicators (KPIs)**

### Key Performance Indicators (KPIs)

- **Total Bookings:** Total number of trips booked during the selected period.
- **Total Booking Value:** Sum of booking values recorded in the dataset.
- **Average Booking Value:** Average booking value per trip.
- **Total Trip Distance:** Combined distance covered across all recorded trips.
- **Average Trip Distance:** Average distance traveled per trip.
- **Average Trip Time:** Average duration of a trip.

These KPIs help users understand overall booking activity, booking value, and trip characteristics.

These KPIs help users understand overall booking activity, booking value, and trip characteristics.

### 2. Dynamic Measure Analysis

A dynamic measure selector allows users to switch between metrics without creating a separate chart for each measure.

**Available measures:**
- Total Bookings
- Total Booking Value
- Total Trip Distance

**Additional features:**
- Dynamic chart titles based on the selected measure.
- Analysis by payment type, such as card, cash, or wallet, where available.
- Comparison of day and night trips.
- Interactive slicers for dates, cities, and other available dimensions.
- Tooltips showing additional information, such as average booking value and trip distance.

### 3. Vehicle Type Analysis

A table or matrix compares the performance of different vehicle types using the following metrics:

- Total Bookings
- Total Booking Value
- Average Booking Value
- Total Trip Distance

Conditional formatting highlights differences in performance, while sorting and filtering help users compare vehicle categories and identify booking patterns.

### 4. Daily Booking Analysis

This analysis examines booking volumes across days to identify demand patterns and fluctuations.

**Key objectives:**
- Identify peak and off-peak booking days.
- Observe changes in daily trip volumes.
- Compare booking activity across selected periods.
- Support demand analysis for operational planning.

External factors such as holidays, weather, and special events can only be evaluated if the relevant data is available.

### 5. Location Analysis

Location analysis uses the available location data to examine ride demand and travel patterns.

- **Most Frequent Pickup Point:** Identifies the most common pickup locations based on recorded bookings.
- **Most Frequent Drop-off Point:** Identifies the most common destinations.
- **Farthest Trip:** Identifies the trip with the greatest recorded travel distance.
- **Top 5 Locations by Total Bookings:** Highlights the five locations with the highest booking volumes.
- **Most Preferred Vehicle by Pickup Location:** Identifies the most frequently booked vehicle type for each pickup location, where the necessary data is available.

For pickup and drop-off analysis, an inactive relationship can be activated in a DAX measure using `USERELATIONSHIP`, provided the data model is configured correctly.

### 6. User Experience Enhancements

**Data Details Panel**

A bookmark-based panel provides supporting information about the dashboard, including:

- Definitions of key performance indicators.
- Descriptions of data tables.
- Dataset source and refresh information, where known.

**Clear Filters Button**

A dedicated button resets slicer selections to the saved default state, allowing users to restart their analysis.

**Data Export**

Users can export permitted underlying or summarized data using Power BI's supported export functionality. Additional automation may be configured if required.

## Data Model

The project uses two primary tables: `Location` and `Uber Trip Details`.

### 1. Location

The `Location` table contains location-related information used for pickup and drop-off analysis.

It supports:
- Identifying frequent pickup and drop-off points.
- Analyzing booking volumes by location.
- Comparing vehicle preferences across pickup locations.
- Filtering and grouping trips by available location attributes.

### 2. Uber Trip Details

The `Uber Trip Details` table contains trip-level information used to calculate KPIs and analyze booking characteristics.

Depending on the available columns, it supports:
- Booking counts and booking values.
- Trip distance and trip duration.
- Payment type analysis.
- Day and night trip comparisons.
- Vehicle type comparisons.
- Date-based booking analysis.

### Data Relationships

The data model connects trip records with the relevant location information. Where pickup and drop-off locations require different relationships to the same location table, an inactive relationship can be activated in a DAX measure using `USERELATIONSHIP`.

The exact relationship keys and cardinality depend on the dataset structure.

## Tools and Technologies

- **Microsoft Power BI:** Dashboard development and interactive data visualization.
- **DAX (Data Analysis Expressions):** KPI calculations, dynamic measures, and relationship-dependent analysis.
- **Power Query:** Data preparation and transformation.
- **Data Modeling:** Relationships between trip and location data.
- **Business Intelligence:** KPI reporting and exploratory analysis.

## Key Insights and Expected Outcomes

The dashboard is designed to help users:

- Understand overall ride-booking activity and booking value.
- Compare trip patterns across payment methods, vehicle types, and time periods.
- Evaluate typical trip distances and durations.
- Identify frequently used pickup and drop-off locations.
- Explore booking concentration across locations.
- Examine vehicle preferences by pickup location.
- Support data-driven discussions about operational efficiency and demand patterns.

Actual findings depend on the dataset analyzed. The dashboard does not, by itself, establish improvements in pricing, resource allocation, or customer satisfaction.

## Repository Contents

The repository may include:

- Power BI dashboard file (`.pbix`).
- Sample dataset, if redistribution is permitted.
- Dashboard screenshots.
- Project documentation (`README.md`).

## How to Use the Project

1. Clone or download this GitHub repository.
2. Open the `.pbix` file using Microsoft Power BI Desktop.
3. Refresh the data source if the dataset is included and the source path needs updating.
4. Explore the KPI cards, charts, and vehicle type matrix.
5. Use the slicers to filter by available dates, cities, and other dimensions.
6. Select a metric in the dynamic measure selector to update the relevant visualizations.
7. Explore pickup and drop-off analysis.
8. Use the reset button to restore the default filter state.

## Dataset and Disclaimer

This project uses a sample ride-booking dataset for learning, analysis, and portfolio demonstration purposes.

The `Uber Trip Details` table name reflects the source or naming convention of the provided project data. The analysis should not be interpreted as official company reporting.

The dataset's origin, completeness, and representativeness determine the reliability of any conclusions. No actual business impact is claimed.

## Author

Developed as a data analytics and business intelligence portfolio project using Microsoft Power BI.
