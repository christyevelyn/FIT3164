# FIT3164
# GrainCast

GrainCast is a static web dashboard for comparing Australian wheat-growing locations using short-term weather forecast data and historical weather trends.

## Project Overview

The website allows users to:

- Select a primary weather station location
- Select up to two secondary locations for comparison
- Choose a wheat type
- View a 7-day forecast summary
- Receive a basic planting recommendation based on temperature, rainfall, and wind speed
- Compare historical rainfall, wind speed, and temperature data across locations

## Files

- `index.html` contains the main page structure.
- `help.html` contains the help and project information page.
- `styles.css` contains the visual styling and responsive layout.
- `app.js` contains the dashboard logic, user interactions, map rendering, recommendations, and chart rendering.
- `forecast-data.json` stores the processed forecast dataset.
- `forecast-data.js` loads the forecast dataset into the browser.
- `historical-data.json` stores the processed historical weather dataset.
- `historical-data.js` loads the historical dataset into the browser.
- `map-data.js` contains the SVG map path data used for the Australian station map.
- `extract_forecast_data.py` processes spreadsheet and CSV/ZIP source data into JSON and JavaScript data files.

## How To Run

Open `index.html` in a web browser.

No server is required because the project uses static HTML, CSS, JavaScript, and local JavaScript data files.

## Data Processing

The Python script `extract_forecast_data.py` reads the source weather datasets, groups the historical data by station, year, and month, and writes the processed results into JSON files.

The generated JavaScript files wrap the same data in browser-readable variables so the dashboard can access them directly.

## Recommendation Logic

The planting recommendation is based on simple threshold rules using the 7-day average forecast:

- Average maximum temperature
- Average rainfall
- Average wind speed

The recommendation is intended as a basic decision-support indicator, not as a professional agricultural advisory tool.

## Limitations

- The dashboard depends on the provided processed data files.
- The recommendation logic is simplified and does not include soil type, crop stage, pests, disease risk, or market conditions.
- The historical comparison uses monthly aggregated values.
- Forecast accuracy depends on the quality of the source forecast data.

## Technologies Used

- HTML
- CSS
- JavaScript
- Python
- pandas
