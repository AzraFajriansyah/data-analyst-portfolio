# US Flight Delay Analysis & Interactive Dashboard

## Overview

This project analyzes flight delays across the United States to identify operational patterns, major delay hotspots, and the primary reported causes of delays. Using monthly airline and airport data, I cleaned and prepared the dataset, analyzed delay metrics across multiple dimensions, and developed an interactive Tableau dashboard to communicate the findings.

The analysis focuses on delay volumes, temporal trends, airport and airline comparisons, and the distribution of delays by reported cause. The goal is to provide a clear overview of where delays are concentrated and which factors account for the largest share of reported delays.

This is a descriptive analysis rather than a forecasting model. It explores historical patterns and operational trends without attempting to predict future delays or establish causal relationships beyond what the data supports.

## Dataset

The primary dataset is located at `data/airline_delay_cause.csv`. It contains monthly observations for airlines and airports, along with flight counts and delay metrics.

Key fields include:

- **Time:** `year`, `month`
- **Airline information:** `carrier`, `carrier_name`
- **Airport information:** `airport`, `airport_name`
- **Flight and delay counts:** `arr_flights`, `arr_del15`
- **Delay counts by cause:** `carrier_ct`, `weather_ct`, `nas_ct`, `security_ct`, `late_aircraft_ct`
- **Delay minutes by cause:** `carrier_delay`, `weather_delay`, `nas_delay`, `security_delay`, `late_aircraft_delay`

The Tableau dashboard is packaged in `tableau/us_flight_delay.twbx`.

## Dashboard Features

The interactive Tableau dashboard explores several key questions:

- **Delay trends over time:** Examine how flight delay volumes change across months and identify periods with elevated delays.
- **Airline performance:** Compare airlines by delayed-flight counts and overall delay patterns.
- **Airport analysis:** Identify airports with the highest volumes of delayed flights.
- **Delay causes:** Evaluate the relative contributions of carrier-related, weather-related, National Airspace System (NAS), security, and late-aircraft delays.
- **Monthly delay rates:** Track changes in the proportion of delayed flights throughout the year.

These views provide an accessible overview of historical flight-delay patterns and help highlight areas that may warrant further operational investigation.

## Key Findings

The analysis reveals several notable patterns across the dataset:

- **Overall delay rate:** Approximately 5.86 million flights were delayed out of 33.99 million arrivals, resulting in a delay rate of approximately 17.25%.
- **Seasonal patterns:** Delay volumes peak during the summer months, particularly June and July.
- **Major delay contributors:** Late-aircraft and carrier-related delays account for substantial portions of delayed flights, followed by National Airspace System (NAS) delays.
- **Airport hotspots:** Major hubs, including Chicago O'Hare, Atlanta, Dallas/Fort Worth, and Denver, record high volumes of delayed flights.
- **Airline delay volumes:** Southwest, American, SkyWest, and Delta account for substantial numbers of delayed flights in absolute terms.

These findings highlight how delay patterns vary across time, airports, airlines, and reported causes. However, high absolute delay counts may partly reflect differences in flight volumes, so they should not be interpreted as direct measures of relative airline or airport performance.

## Repository Structure

```text id="m4z8q2"
.
├── data/
│   └── airline_delay_cause.csv
├── tableau/
│   └── us_flight_delay.twbx
└── README.md
```

## Tools & Technologies

- Microsoft Excel for data cleaning and preparation
- Tableau for interactive dashboards and data visualization
- Spreadsheet-based data analysis

## Limitations

This project provides a descriptive view of historical flight delays based on the available monthly airline and airport records. The analysis identifies patterns and reported delay causes but does not establish the underlying causal mechanisms behind individual delays.

The findings are also based primarily on absolute delay counts and aggregated metrics. Differences in flight volumes across airlines and airports can influence these comparisons, while additional operational context would be needed to assess relative performance more comprehensively.

The results should therefore be interpreted as historical trends and exploratory insights rather than definitive measures of operational efficiency or predictions of future delays.
