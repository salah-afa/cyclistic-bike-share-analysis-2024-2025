# 🚲 Cyclistic Bike-Share Analysis: Converting Casual Riders to Members

**Author:** Salah Afaghani  
**Date:** February 2026  
**Project:** Google Data Analytics Professional Certificate Capstone  

📊 **[Click here to view the full interactive HTML Data Report](https://salah-afa.github.io/cyclistic-bike-share-analysis-2024-2025/Riders.html)**

## 📝 Introduction & Business Task
Cyclistic is a fictional bike-share company operating in Chicago. The company's finance analysts have concluded that annual members are significantly more profitable than casual riders. 

The Director of Marketing believes the company’s future success depends on maximizing the number of annual memberships. My objective as a Junior Data Analyst was to analyze historical bike trip data to answer one key business question: **How do annual members and casual riders use Cyclistic bikes differently?** The insights from this analysis will be used to design a new targeted marketing strategy to convert casual riders into annual members.

## 🗄️ Data Source
The data used in this project is public bicycle-sharing data from the **Divvy** system, which is owned by the City of Chicago and operated by **Lyft Bikes and Scooters, LLC**. It is made publicly available under a data license agreement.
* **Data Source Link:** [Divvy Trip Data](https://divvy-tripdata.s3.amazonaws.com/index.html)
* **License:** [Divvy Data License Agreement](https://divvybikes.com/data-license-agreement)
* **Timeframe Analyzed:** Q4 2024 (Oct-Dec) vs. Q4 2025 (Oct-Dec)
* *Note: Due to GitHub's file size limits, the raw CSV files (containing hundreds of thousands of rows) are not hosted in this repository. The cleaned and aggregated summary files are provided instead.*

## 🛠️ Tools & Technologies Used
* **Language:** R
* **Environment:** RStudio
* **Key Packages:** `tidyverse` (data manipulation), `lubridate` (date/time parsing), `skimr` (summary statistics), `ggplot2` (data visualization), `scales` (formatting).
* **Deliverable:** R Markdown (`.Rmd`) rendered to HTML.

## 🧹 Data Cleaning & Manipulation
To ensure data integrity, a custom "master cleaning script" was built in R to:
1.  Standardize mismatched data types (converting strings to `POSIXct` datetime formats).
2.  Calculate exact trip durations (`ride_length`) and extract the day of the week.
3.  Filter out "false starts" (trips under 60 seconds) and abandoned bikes (trips over 24 hours).
4.  Remove faulty GPS check-ins using latitude/longitude bounding boxes for the Chicago area.
5.  Remove duplicate `ride_id` logs to ensure accurate trip counts.

## 💡 Key Insights
1.  **The Commuter vs. Leisure Pattern:** Annual members take consistent, high-volume trips during the weekdays, indicating they primarily use the service for commuting. Casual riders show the opposite pattern, with ridership surging on weekends.
2.  **Trip Duration:** While members ride more frequently, casual riders take significantly longer trips on average. Members use the bikes efficiently to get from point A to point B, while casual riders are likely riding for leisure and exploration.

## 📂 Repository Structure
* `Riders.Rmd`: The complete R Markdown script containing all code for data cleaning, aggregation, and visualization.
* `Riders.html`: The knitted, web-friendly final report.
* `cyclistic_weekly_summary.csv`: The aggregated dataset used to build the final visualizations.
* `README.md`: Project overview and summary.

***
