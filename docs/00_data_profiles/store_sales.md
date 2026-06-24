# Store Sales

## Table Summary

- Row Count: 335,129
- Grain candidate: One sales record per date, store and product
- Primary key: No explicit primary key

## Transaction Date
* Column Role: Date component
* Min: 1/1/2022
* Max: 12/31/2025
* Error: 0
* Empty: 0
* Data type: Date

## Store ID
* Column Role: Foreign Key -> Store Locations
* Distinct Values: 111
* Error: 0
* Empty: 0
* Data type: Whole number

## Prod Num
* Column Role: Foreign Key -> Products
* Distinct Values: 669
* Error: 0
* Empty: 0
* Data type: Text

## Category
* Column Role: Hierarchy attribute
* Error: %15 (53,282)
* Empty: -
* Data type: Any

## Sale Amount
* Column Role: Additive fact
* Error: 0
* Empty: 0
* Min: 2.4
* Max: 1763.7
* Data type: Decimal Number

## Required Checks
* Test whether Transaction Date + Store ID + Prod Num is unique
* Confirm that every Store ID exists in Store Locations
* Confirm that every Prod Num exists in Products
* Change Category data type form Any to Text
* Check for Category errors
* Compare valid category values with Products
* Decide whether to remove Category and use Products as the canonical source
* Trim Prod Num
* Rename Prod Num to Product ID
* Rename Sale Amount to Sales Amount
* Rename Transaction Date to Sales Date