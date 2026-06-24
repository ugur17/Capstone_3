# Inventory Categories

## Table Summary
- Row Count: 6
- Grain: One row of record for each category
- Primary Key: Column1

## Column1
* Column Role: Primary Key
* Distinct Values: 6
* Error: 0
* Empty: 0
* Data type: Text

## Column2 
* Column Role: Descriptive attribute
* Distinct Values: 6
* Error: 0
* Empty: 0
* Data type: Text


## Required Checks
* Trim all text fields
* Rename Column1 to Category Name
* Rename Column2 to Category Description
* Compare Category Name values with Products Category after trimming
* Decide whether this query needs to be loaded into the model