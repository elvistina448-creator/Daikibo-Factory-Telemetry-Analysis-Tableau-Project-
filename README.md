# Daikibo Factory Telemetry Analysis (Tableau Project)
## Project Overview

This project analyzes machine telemetry data from four Daikibo factories to identify where machine failures occur most frequently and which machine types contribute the most to downtime.

Using Tableau, telemetry messages were analyzed to calculate machine downtime and visualize performance across different factory locations.

The goal of this analysis was to answer two key questions:

. Which factory experienced the most machine downtime?

. Which machine types contributed the most to downtime in that factory?

## Dataset

The dataset contains telemetry messages collected every 10 minutes from machines across four Daikibo factories during May 2021.

## Factory Locations

. Daikibo Factory Meiyo – Tokyo, Japan

. Daikibo Factory Seiko – Osaka, Japan

. Daikibo Berlin – Berlin, Germany

. Daikibo Shenzhen – Shenzhen, China

Each factory has 9 different machine types sending status updates every 10 minutes.

The dataset was provided as a single JSON file.

## Tools Used

Tableau – Data visualization and analysis

JSON – Telemetry data format

GitHub – Project documentation and portfolio

## Data Preparation

To measure downtime, a calculated field called Unhealthy was created in Tableau.

Each telemetry message represents 10 minutes of machine activity. When a machine reports an unhealthy status, it indicates 10 minutes of potential downtime.

### Calculated Field
IF [status] = "unhealthy" THEN 10
ELSE 0
END

This allows Tableau to sum downtime across machines and locations.

## Visualizations

Two bar charts were created:

1. Down Time per Factory

Shows the total downtime for each factory.

2. Down Time per Device Type

Shows which machine types experienced the most downtime.

### Interactive Dashboard

A Tableau dashboard was created combining both charts.

The Factory chart acts as a filter, allowing users to click a factory and see downtime by machine type for that specific location.

This makes it easy to quickly identify which machines are responsible for failures in the most affected factory.

#### Key Insight

By selecting the factory with the highest downtime, the dashboard reveals the specific machine types contributing most to the failures.

This type of analysis can help operations teams:

1. detect reliability issues

2. prioritize maintenance

3. improve factory productivity

## Dashboard Screenshot
