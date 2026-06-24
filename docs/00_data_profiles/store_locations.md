# Store Locations

## Table Summary

- Row Count: 111
- Grain: One row per store, identified by Store ID
- Primary Key: Store ID

## Store Location
* Column Role: Geographic attribute
* Distinct Values: 111
* Unique Values: 111
* Error: 0
* Empty: 0
* Data type: Text

## State
* Column Role: Geographic attribute
* Distinct Values: 12
* Error: 0
* Empty: 0
* Data type: Text

## Store ID
* Column Role: Primary Key
* Distinct Values: 111
* Unique Values: 111
* Error: 0
* Empty: 0
* Data type: Whole Number

## Required Checks
* Trim all Texts
* Check for abbreviations and full names in State values and standardize them to only full names
* Check for the state names in Store Sales and Management Team, so they are standardized all together
* Rename State to Store State
