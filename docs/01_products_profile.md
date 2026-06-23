# Products

## Table Summary

 - Row Count: 669
 - Grain: One row per product, identified by Prod Num
 - Primary Key: Prod Num

## Prod Num

 * Column Role: Primary Key
 * Distinct Values: 669
 * Unique Values: 669
 * Error: 0
 * Empty: 0
 * Data type: Text

## Product

 * Column Role: Descriptive attribute
 * Count: 669
 * Empty: 0
 * Error: 0
 * Data type: Any

## Category

 * Column Role: Hierarchy attribute
 * Distinct Values: 6
 * Count: 669
 * Error: 0
 * Empty: 0
 * Data type: Text

## Subcategory

 * Column Role: Hierarchy attribute
 * Distinct Values: 52
 * Count: 669
 * Error: 0
 * Empty: 0
 * Data type: Text

## Required Checks
 * Change Product data type from Any to Text
 * Trim Prod Num, Product, Category and Subcategory
 * Rename Product to Product Name
 * Rename Prod Num to Product ID
 * Check whether Product Names contain duplicates
 * Validate Product Name matches against the book list
 * Compare Category values across related tables