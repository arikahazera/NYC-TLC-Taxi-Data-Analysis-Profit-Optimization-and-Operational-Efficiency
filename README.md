# NYC-TLC-Taxi-Data-Analysis-Profit-Optimization-and-Operational-Efficiency

## Background

The New York City (NYC) Taxi and Limousine Commission (TLC) is the city government agency responsible for regulating and licensing taxis, for-hire vehicles, limousines, commuter vans, and paratransit vehicles in New York City. It was officially established on March 2, 1971.

NYC’s taxi system operates on strict service zone rules, which determine where each type of vehicle is allowed to pick up passengers. Yellow medallion taxis are permitted to pick up street hails anywhere in the city, while green boro taxis can only pick up street hails in the outer boroughs and in northern Manhattan.

## Problem Statement

TLC operates across all five boroughs, but lacks a clear, data-driven understanding of customer preferences, which zones and what time range generate the highest revenue, and which areas contribute to operational inefficiencies. Without zone-level profitability insights, TLC cannot optimize fleet distribution, minimize wasted mileage, or allocate resources efficiently.

The question that we want to address is:

**How do revenue, demand patterns, and customer preferences vary across different time periods and locations in NYC, and what does this reveal about opportunities to improve profit and operational efficiency?**

## Objectives

1. To analyze NYC taxi trip data to understand how revenue, demand patterns, and customer preferences vary across time and geography.
2. To identify opportunities for profit improvement and operational efficiency.

## Executive Summary

**Key findings:**

1. Strong revenue concentration in Manhattan (revenue by borough)
2. Peak demand and high revenue hours → 4 PM - 6 PM
3. Zones show significant revenue inequality
4. Distance does not strongly determine revenue
5. Tip behavior varies by time
6. Statistical tests confirm significant relationships

## Data

1. NYC TLC Trip Record (Raw main dataset)
2. taxi_zone_lookup (Complementary dataset)
3. taxi_zones (Complementary dataset)
4. TLC NYC Taxi Cleaned (Clean Dataset)

## Key Features
| Feature | Description | dtype |
| :--- | :----: | ---: |
| VendorID | An LPEP provider code | int64 |
| lpep_pickup_datetime | The date and time when the meter was engaged | datetime64 |
| lpep_dropoff_datetime | The date and time when the meter was disengaged | datetime64 |
| store_and_fwd_flag | A trip record flag in vehicle memory | object |
| RatecodeID | The final rate code is in effect at the end of the trip | object |
| PULocationID | TLC Taxi Zone ID in which the taximeter was engaged | int64 |
| PU_Zone | The zone of taxi pick up | object |
| PU_Borough | The borough of taxi pick up | object |
| DOLocationID | TLC Taxi Zone ID in which the taximeter was disengaged | int64 |
| DO_Zone | The zone of taxi drop off | object |
| DO_Borough | The borough of taxi drop off | object |
| passenger_count | The number of passengers in the vehicle | float64 |
| trip_distance | The elapsed trip distance in miles was reported by the taximeter | float64 |
| fare_amount | The time-and-distance fare is calculated by the meter | float64 |
| extra | Miscellaneous extras and surcharges | float64 |
| mta_tax |  $0.50 MTA tax that is automatically triggered based on the metered rate in use | float64 |
| tip_amount | This field is automatically populated for credit card tips | float64 |
| tolls_amount | The total amount of all tolls paid in the trip | float64 |
| improvement_surcharge | $0.30 improvement surcharge assessed on hailed trips at the flag drop | float64 |
| total_amount | The total amount charged to passengers | float64 |
| payment_type | A numeric code signifying how the passenger paid for the trip | float64 |
| trip_type | A code indicating whether the trip was a street hailor a dispatch | float64 |
| congestion_surcharge | A fee drivers charge to passengers because they need to pay to enter a specific, congested area | float64 |
| tip_percent | The percentage of tip per ride | float64 |
| hour | The hour when taxi ride is conducted | float64 |
| day_name | The day of week when taxi ride is conducted | float64 |

## Python & Library Specification
    
1. python version 3.13.7

2. pandas version 2.3.3

3. numpy version 2.3.3
   
4. matplotlib version 3.10.7
   
5. seaborn version 0.13.2
   
7. plotly version 6.4.0
