# book list

## Table Summary
- Row Count: 93
- Grain: one row per book
- Primary key: no explicit primary key


## Raw Text Pattern
* Leading list number, period and space
* Book title enclosed in asterisks
* Author follows the delimiter ' by '

## Required Checks
* Import the file as a single text column
* Remove leadings
* Extract book title and author into separate columns
* Preserve original text for validation
* Trim and clean extracted texts
* Check for duplicate book names
* Macth book names against product names
* Record matched, unmatched and ambigious titles