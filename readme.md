# Earthquake Data Analysis Project

## Overview
This project analyzes earthquake data from Turkey and surrounding regions, focusing on seismic activity patterns, magnitudes, depths, and geographical distribution. The analysis includes data cleaning, exploration, statistical analysis, and visualization.

## Dataset
The dataset (`deprem_son24saat_duzenli.csv`) contains:
- 284 earthquake records
- Fields:
  - **Olus_Zamani**: Timestamp of earthquake
  - **Enlem**: Latitude
  - **Boylam**: Longitude
  - **Derinlik_km**: Depth in kilometers
  - **Buyukluk**: Magnitude
  - **Yer**: Location description

## Requirements
- Required libraries:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn (for dataset loading if using Iris dataset example)

Install requirements:
pip install pandas numpy matplotlib seaborn scikit-learn


## Code Structure

### Data Loading and Cleaning
- Loads CSV data with proper datetime parsing
- Checks for missing values
- Adds derived features:
  - Hour of day
  - Time of day categories (Night/Morning/Afternoon/Evening)
  - Cleaned location names

### Data Analysis
- Basic statistics (mean, max, count) for numerical columns
- Grouped analysis by:
  - Location
  - Time of day
- Key findings about magnitude and depth distributions

### Visualizations
- Six main visualizations created:
  - **Magnitude Over Time**: Line chart showing earthquake magnitudes chronologically
  - **Average Magnitude by Location**: Bar chart of top 5 locations
  - **Depth Distribution**: Histogram of earthquake depths
  - **Depth vs Magnitude**: Scatter plot showing relationship
  - **Geographical Distribution**: Map plot showing earthquake locations
  - **Hourly Distribution**: Count of earthquakes by hour

## How to Run
- Place the CSV file (`deprem_son24saat_duzenli.csv`) in the same directory as the Jupyter notebook file
- Run the Jupyter notebook file

## Key Findings
- Strongest earthquake: 5.2 magnitude in Marmara Sea
- Average depth: ~15 km
- Most frequent location: Marmara Sea region
- No clear correlation between depth and magnitude
- Earthquakes distributed fairly evenly throughout the day

## Customization Options
- Adjust visualization styles by modifying `seaborn.set()` parameters
- Change time bins by modifying the `Day_Part` categorization
- Filter specific locations by editing the `top_locations` selection

## Note
The script includes warning suppression for cleaner output. Remove `warnings.filterwarnings('ignore')` if you need to see warnings during development.
