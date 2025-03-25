# Big Data with PySpark using Anaconda & Jupyter Notebook

## Overview

This project involves performing big data analysis on weather datasets for Cincinnati and Florida using PySpark within a Jupyter Notebook environment. The project covers various data manipulation and analysis tasks, including data loading, filtering, aggregation, statistical calculations, and time series forecasting.

## Project Requirements and Implementation

This project fulfills the following requirements:

**1. Anaconda Python, PySpark, and Jupyter Notebook Setup:**

**2. Load the CSV files and display the count of each dataset:**

**3. Find the hottest day (column MAX) for each year:**

**4. Find the coldest day (column MIN) for the month of March across all years (2015-2024):**

**5. Find the year with the most precipitation for Cincinnati and Florida:**

**6. Count the percentage of missing values for wind gust (column GUST) for Cincinnati and Florida in the year 2024:**

**7. Find the mean, median, mode, and standard deviation of the temperature (column TEMP) for Cincinnati in each month for the year 2020:**

**8. Find the top 10 days with the lowest Wind Chill for Cincinnati in 2017:**

**9. Investigate how many days had extreme weather conditions for Florida (fog, rain, snow, etc.) using the FRSHTT column:**

**10. Predict the maximum Temperature for Cincinnati for November and December 2024, based on the previous 2 years of weather data:**

  For predicting the maximum temperature for Cincinnati for the months of November and December 2024 based on the previous 2 years of weather data, I have tried using a few approaches. 
  * Approach 1 - Average of historical maximum temperatures
  * Approach 2 - Last value + trend (of last 2 years)
  * Approach 3 - Weighted average (recent years have more weight)
  * Approach 4 - SARIMA
  * Approach 5 - XGBoost

* **Prediction Results:**
    * November 2024 Predicted MAX Temperature: 80.57°F
    * December 2024 Predicted MAX Temperature: 66.22°F
      
* **Model Performance and Potential Improvements:**
    The MAX Temperature predicted by the SARIMA model for November 2024 is 80.57°F and for December 2024 is 66.22°F.
    SARIMA had the best performance with November 2024 Prediction Error: 0.47°F and December 2024 Prediction Error: 3.22°F. It effectively captured temperature patterns, particularly for November.
    It was also computationally less expensive and took 2.004 seconds to train.

    In terms of potential improvement, the model would benefit greatly if trained on more data. For example, if the training dataset included weather data from 2015 to 2024 October, the model predictions would be a lot better.
    In such a case, the XGBoost model would probably also produce better predictions.
    The SARIMA model could be refined by tuning the parameters to better capture December patterns.

## Data Sources

* [https://www.ncei.noaa.gov/data/global-summary-of-the-day/access/]

## Technologies Used

* Anaconda Python
* PySpark
* Jupyter Notebook / JupyterLab
