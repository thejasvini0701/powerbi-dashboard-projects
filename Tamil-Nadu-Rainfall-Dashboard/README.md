# Tamil Nadu Rainfall Analysis Dashboard (2020–2024)

An interactive Power BI dashboard that compares **actual vs normal rainfall** across **39 districts of Tamil Nadu** from 2020 to 2024, with season-wise and year-wise analysis.

## Objective
- Compare actual and normal rainfall for each district
- Find districts with above-normal and below-normal rainfall
- Analyze seasonal rainfall (South-West monsoon, North-East monsoon, winter, hot weather)
- Track annual rainfall trends across years

## Tools Used
- Power BI Desktop
- Power Query (data cleaning and transformation)

## Dataset
- File: `TamilNadu_Rainfall_Analysis_Sample.csv`
- Records: 195 (39 districts × 5 years)
- Period: 2020–2024
- Note: This is a sample dataset used for practice and analysis.

| Column | Description |
|---|---|
| Year | Year of record (2020–2024) |
| District | Tamil Nadu district name |
| Rainfall_Range | Rainfall category (High / Moderate) |
| SW / NE Monsoon, Winter, Hot Weather | Normal and actual rainfall for each season |
| Annual_Total_Normal | Normal annual rainfall |
| Annual_Total_Actual | Actual annual rainfall |
| Deviation_% | Percentage difference from normal rainfall |

## Data Preparation (Power Query)
- Loaded the CSV file and promoted headers
- Set correct data types for all columns
- Unpivoted the seasonal actual-rainfall columns for season-wise analysis
- Renamed columns for clarity (`SW_rainfall`, `NE_rainfall`, `Winter_rainfall`, `Hot_rainfall`)

## Dashboard Overview

### Page 1: District Overview
- KPI cards: Annual Actual Rainfall, Annual Normal Rainfall, Deviation %
- District-wise Annual Rainfall: Actual vs Normal
- Season-wise Normal Rainfall by District
- Rainfall Range by Year
- Slicers: Year, District, Rainfall Range

### Page 2: Trends and Deviation
- Rainfall Deviation by District (%)
- Seasonal rainfall trend by year (line chart)
- Annual Actual vs Normal rainfall by year (line chart)

## Key Insights
- The North-East monsoon gives the most rainfall (about 633 mm on average), followed by the South-West monsoon (about 510 mm).
- Annual rainfall was slightly below normal in 2020–2022 and above normal in 2023–2024.
- Erode, Tiruppur and Tiruvallur had the highest average rainfall above normal.
- Dindigul and Namakkal had the highest average rainfall below normal.

## How to Use
1. Download the `.pbix` file from this repository
2. Open it in Power BI Desktop
3. Update the data source path to your local CSV file if needed
4. Use the slicers to filter by year, district and rainfall range


