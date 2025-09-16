# London Bike Rides Analysis

A comprehensive data analysis project exploring London's bike-sharing dataset with moving averages and heatmap visualizations using Tableau.

## 📊 Project Overview

This project analyzes London's bike-sharing data to understand usage patterns, seasonal trends, and the impact of weather conditions on bike rentals. The analysis includes data preprocessing, exploratory data analysis, and interactive visualizations.

## 📁 Project Structure

```
LondonBikeRides-main/
├── london_bikes.ipynb                    # Jupyter notebook with data processing
├── london_merged.csv                     # Raw dataset (17,414 records)
├── london_bikes_final.xlsx              # Processed dataset for Tableau
├── london-bike-sharing-dataset.zip      # Original dataset from Kaggle
├── London Bike Rides - Moving Average and Heatmap.twbx  # Tableau workbook
└── README.md                            # This file
```

## 🚴 Dataset Information

The dataset contains **17,414 hourly records** of bike-sharing data from London, spanning from 2015 onwards. Each record includes:

### Original Columns
- `timestamp` - Date and time of the record
- `cnt` - Total number of bike rentals
- `t1` - Real temperature in Celsius
- `t2` - "Feels like" temperature in Celsius
- `hum` - Humidity percentage
- `wind_speed` - Wind speed in km/h
- `weather_code` - Weather condition code
- `is_holiday` - Binary indicator for holidays
- `is_weekend` - Binary indicator for weekends
- `season` - Season code (0=Spring, 1=Summer, 2=Autumn, 3=Winter)

### Processed Columns (for Tableau)
- `time` - Renamed timestamp
- `count` - Renamed cnt (bike rentals)
- `temp_real_C` - Real temperature
- `temp_feels_like_C` - Feels like temperature
- `humidity_percent` - Humidity as percentage (0-1)
- `wind_speed_kph` - Wind speed
- `weather` - Mapped weather conditions:
  - Clear, Scattered clouds, Broken clouds, Cloudy
  - Rain, Rain with thunderstorm, Snowfall
- `is_holiday` - Holiday indicator
- `is_weekend` - Weekend indicator
- `season` - Mapped seasons (spring, summer, autumn, winter)

## 🛠️ Data Processing

The Jupyter notebook (`london_bikes.ipynb`) performs the following data transformations:

1. **Data Download**: Downloads the dataset from Kaggle using the Kaggle API
2. **Data Extraction**: Extracts the CSV file from the downloaded zip archive
3. **Data Exploration**: Analyzes data structure, types, and basic statistics
4. **Column Renaming**: Renames columns for better readability
5. **Data Type Conversion**: Converts numeric codes to meaningful text labels
6. **Data Mapping**: Maps weather codes and season codes to descriptive names
7. **Data Export**: Exports the processed data to Excel format for Tableau

## 📈 Visualizations

The Tableau workbook (`London Bike Rides - Moving Average and Heatmap.twbx`) contains:

- **Moving Average Analysis**: Time series analysis showing bike rental trends
- **Heatmap Visualizations**: Interactive heatmaps showing usage patterns
- **Seasonal Analysis**: Comparison of bike usage across different seasons
- **Weather Impact**: Analysis of how weather conditions affect bike rentals

## 🚀 Getting Started

### Prerequisites

- Python 3.x
- Jupyter Notebook
- Tableau Desktop (for viewing the workbook)
- Required Python packages:
  ```bash
  pip install pandas kaggle openpyxl
  ```

### Setup

1. **Clone or download** this repository
2. **Install dependencies**:
   ```bash
   pip install pandas kaggle openpyxl
   ```
3. **Set up Kaggle API** (if you want to re-download the data):
   - Get your Kaggle API key from [Kaggle Account Settings](https://www.kaggle.com/account)
   - Place `kaggle.json` in `~/.kaggle/` directory
   - Set proper permissions: `chmod 600 ~/.kaggle/kaggle.json`

### Running the Analysis

1. **Open the Jupyter notebook**:
   ```bash
   jupyter notebook london_bikes.ipynb
   ```
2. **Run all cells** to process the data
3. **Open the Tableau workbook** to explore the visualizations

## 📊 Key Insights

Based on the data analysis, some key patterns emerge:

- **Seasonal Patterns**: Bike usage varies significantly across seasons
- **Weather Impact**: Weather conditions strongly influence bike rental numbers
- **Time Patterns**: Usage patterns differ between weekdays and weekends
- **Temperature Correlation**: Both real and "feels like" temperature affect usage

## 🔗 Data Source

- **Original Dataset**: [London Bike Sharing Dataset](https://www.kaggle.com/datasets/hmavrodiev/london-bike-sharing-dataset) on Kaggle
- **Dataset Author**: Hristo Mavrodiev
- **License**: CC0: Public Domain

## 📝 Notes

- The dataset contains hourly data from London's bike-sharing system
- All temperature values are in Celsius
- Weather codes have been mapped to descriptive names for better analysis
- The processed Excel file is optimized for Tableau visualizations

