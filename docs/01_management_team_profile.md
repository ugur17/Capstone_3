# Management Team

## Table Summary
- Source row count: 11
- Structure: Three logical tables stored side by side
- Grain: No single grain
- Primary key: No single primary key

## Logical Tables
* Region-Director Mapping: One row per region
* State-Manager Mapping: One row per state
* State-Region Mapping: One row per state

## Required Checks
* Split the raw sheet into three seperate queries
* Remove seperator and irrelevant columns
* Remove blank rows for each queries
* Trim all text columns
* Check key uniquness for each queries