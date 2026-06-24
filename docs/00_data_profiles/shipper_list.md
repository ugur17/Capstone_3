# Shipper List

## Table Summary

- Row count: 29
- Grain: preferred shipper and volume discount per state
- Primary key: Ship-to State

## Ship-to State
* Column Role: Primary Key
* Distinct Values: 29
* Errors: 0
* Empty: 0
* Data type: Text

## Preferred Shipper
* Column Role: Descriptive attribute
* Distinct Values: 3
* Error: 0
* Empty: 0
* Data type: Text

## Volume Discount
* Column Role: Numeric attribute (non-additive)
* Min: 0.06
* Max: 0.22
* Error: 0
* Empty: 0
* Data type: Decimal Number

## Modeling Decision
* This table will be excluded from modeling because this dataset can not support a reliable conclusion about the impact of shipping discounts on sales.
