# Vehicle Damage & Repair Performance Dashboard

<img src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Power BI">
<img src="https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logoColor=white" alt="DAX">
<img src="https://img.shields.io/badge/Power%20Query-217346?style=for-the-badge&logoColor=white" alt="Power Query">
<img src="https://img.shields.io/badge/SQL-336791?style=for-the-badge&logoColor=white" alt="SQL">

An interactive Power BI dashboard developed to monitor vehicle damage frequency, repair costs, and repair-cycle performance across facilities and vehicle programs.

## Dashboard Preview

<img width="1568" height="788" alt="image" src="https://github.com/user-attachments/assets/f8bc1cc4-14eb-46cc-85a7-7ff0732fc7a7" />

## Project Overview

Vehicle damage information is often distributed across inventory, damage, repair-order, and billing records. This dashboard combines those records into a centralized analytical report for operational and quality-management teams.

The report provides an executive overview of damage performance while allowing users to investigate trends by facility, vehicle program, damage source, hold status, and reporting period.

It was designed to answer questions such as:

- How frequently are vehicles being damaged?
- What is the average financial impact of each damage event?
- How much has been billed for vehicle repairs?
- How long does it take to identify, log, and complete repairs?
- Which facilities or vehicle programs are driving performance?
- Are damage rates and repair-cycle times improving?

## Key Performance Indicators

| KPI | Description |
| --- | --- |
| **Damage Rate** | Damaged vehicles as a percentage of all vehicles received during the selected period. |
| **Average Cost** | Average billed repair cost per eligible damaged vehicle. |
| **Total Billed** | Total repair costs associated with the selected records. |
| **Average Time to Repair** | Average number of days between repair-order creation and repair completion. |
| **Arrival to Hold** | Average number of days between vehicle arrival and placement on damage hold. |
| **Hold to Repair Log** | Average number of days between the damage hold and creation of the repair record. |
| **50th Percentile** | The cycle time at or below which 50% of eligible records fall. |
| **85th Percentile** | The cycle time at or below which 85% of eligible records fall. |

## Dashboard Features

- Executive KPI cards for damage rate, repair cost, and cycle-time performance
- Comparisons between the latest 7 days and the preceding 7 days
- Comparisons between the latest 30 days and the preceding 30 days
- Current-week, previous-week, MTD, QTD, and YTD performance summaries
- Dynamic metric selection using interactive report controls
- Damage severity and cycle-time distributions
- Cumulative-percentage analysis
- Monthly damage-rate and average-cost trends
- Detailed severity matrix by vehicle program
- Date-range filtering
- Facility and vehicle-program filtering
- Damage-source filtering
- Hold-status filtering
- Dedicated controls for internal, marine, and transportation damage
- Clear Filters button for returning the report to its default state

## Dynamic Distribution Analysis

The distribution visual can switch between five operational metrics:

1. Damage Rate
2. Damage Severity
3. Average Time to Repair
4. Arrival to Hold
5. Hold to Repair Log

Each metric uses its own set of analytical buckets. The accompanying cumulative-percentage line shows how much of the affected vehicle population falls below each cost or cycle-time threshold.

This allows users to evaluate both typical performance and the long tail of higher-cost or longer-running cases.

## Analytical Workflow

The dashboard supports a progressive investigation process:

1. **Monitor** overall performance using the KPI cards.
2. **Compare** current results against recent and cumulative periods.
3. **Identify** unusual distributions or monthly trends.
4. **Segment** the results by facility, vehicle program, source, or hold status.
5. **Investigate** the detailed matrix to locate the groups driving the result.

## Technical Implementation

| Technology | Purpose |
| --- | --- |
| **Power BI Desktop** | Semantic modeling, report development, and visual design |
| **DAX** | KPIs, percentiles, time intelligence, dynamic metrics, and filter-aware calculations |
| **Power Query (M)** | Data extraction, transformation, cleansing, and table integration |
| **SQL** | Source-data validation, reconciliation, and data-quality analysis |
| **Bookmarks and Report Controls** | Metric selection, navigation, and filter-reset functionality |

## Data Model

The analytical model integrates several operational subject areas:

- Vehicle inventory and arrival records
- Vehicle damage records
- Damage classifications and sources
- Repair orders
- Repair completion dates
- Repair charges and billed amounts
- Facility information
- Vehicle-program information
- Calendar and reporting-period dimensions

The model was designed so that date, facility, vehicle program, damage source, and hold-status selections consistently filter both summary and detailed report visuals.

The complete report also uses context-aware calculations for:

- Rolling 7-day and 30-day comparisons
- Month-to-date performance
- Quarter-to-date performance
- Year-to-date performance
- Median and 85th-percentile cycle times
- Dynamic histogram buckets
- Cumulative percentages
- Filter-aware vehicle counts

## Data Quality and Validation

Data-quality checks were performed before building the final report, including validation for:

- Missing or invalid event dates
- Duplicate vehicle records
- Duplicate repair orders
- Unmatched damage and repair records
- Missing billing information
- Negative or implausible cycle times
- Inconsistent record counts between source tables
- Proper filter behavior across related tables

SQL reconciliation queries were used alongside Power BI validation measures to confirm record counts, date alignment, and financial totals.

## Skills Demonstrated

- Business intelligence development
- Data modeling
- DAX measure development
- Power Query transformation
- SQL validation and reconciliation
- Time-intelligence calculations
- Statistical percentile analysis
- Dynamic histogram development
- Interactive report navigation
- Executive dashboard design
- Operational performance analysis
- Data-quality validation

## Repository Structure

```text
.
├── README.md
├── dashboard-preview.png
├── S&OP KPIs - Damages.pbix
└── sql/
    └── validation-queries.sql
```

## Privacy and Data Security

This repository is intended to demonstrate Power BI development, analytical design, and data-modeling skills.

Proprietary source data, credentials, connection strings, customer information, vehicle identification numbers, and organization-specific identifiers should not be included in the public version of this repository.

Any displayed information should be anonymized, aggregated, or replaced with synthetic data.

## Author

**Joel Perez**

Data Analytics · Business Intelligence · Power BI · Power Platform
