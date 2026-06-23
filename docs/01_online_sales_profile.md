# Online Sales

## Table Summary

 - Row Count: 127,965
 - Grain Candidate: One sales record per date, product and ship-to state.
 - Primary key: No explicit primary key is available.

## Year
* Column Role: Date component
* Distinct Values: 4
* Range: 2022 - 2025
* Empty: 0
* Error: 0
* Data type: Whole Number

## Month
* Column Role: Date component
* Distinct Values: 12
* Range: 1 - 12
* Empty: 0
* Error: 0
* Data type: Whole Number

## Day
* Column Role: Date component
* Distinct Values: 31
* Range: 1 - 31
* Empty: 0
* Error: 0
* Data type: Whole Number

## Prod Num
* Column Role: Foreign key -> Products
* Distinct Values: 31
* Empty: 0
* Error: 0
* Data type: Text

## Sales Total
* Column Role: Additive fact
* Min: 2.4
* Max: 14,109.6
* Empty: 0
* Error: 0
* Data type: Decimal Number
* No zero or negative value

## Ship-to State
* Column Role: Geographic dimension attribute
* Distinct Values: 29
* Empty: 0
* Error: 0
* Data type: Text

## Required Checks

* Create and validate a Date column
* Confirm that every Prod Num exists in Products
* Test whether Date + Prod Num + Ship-to State is unique
* Trim Prod Num and Ship-to State
* Rename Prod Num to Product ID
* Rename Sales Total to Sales Amount
* Rename Ship-to State to Ship To State
