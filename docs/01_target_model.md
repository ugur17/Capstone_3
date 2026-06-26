# Target data model


## Global Analysis Scope
- Date Range: 2022 - 2025
- Region (Filter by): Northeast
- Sales channels: Online Sales and Store Sales

## Modeling Purpose and Required Analysis

* To create a model that 2022-2025 online and store sales can be compared by date, geography and product.
- Sales trends over the full period covered in the data 
- Sales performance by category 
- Relative sales for each state in the region 
- A list of top-selling books, including author names, for Northeast (general audience, 
excluding textbooks) 


## Analysis-to-Model Mapping

* Sales trends
- Measure: Sales amount
- Analyze by: date
- Compare: Online sales vs Store sales
- Target Dimension: DimDate
- Dimension sources: Online Sales Data field and Store Sales Transaction Date
- Fact Tables: FactOnlineSales and FactStoreSales

* Sales by category
- Measure: Sales amount
- Analyze by: category
- Target Dimension: DimProduct
- Dimension sources: Products
- Fact Tables: FactOnlineSales and FactStoreSales

* Relative Sales by State
- Measure: Sales amount
- Analyze by: State
- Target Dimension: DimGeography
- Dimension sources: Store Locations, Team management, Online Sales
- Fact Tables: FactOnlineSales and FactStoreSales

* Top selling books and authors
- Measures: Sales amount
- Analyze by: book title and author name
- Target Dimension: DimProduct
- Dimension Sources: Products and book list
- Fact Tables: FactOnlineSales and FactStoreSales

## Target Tables

### Fact Tables
- FactOnlineSales -> One sales record per date, product, and state
- FactStoreSales -> One sales record per date, product, and store

### Dimension Tables
- DimDate -> One row per date
- DimProduct -> One row per product id
- DimGeography -> One row per state
- DimStore -> One row per store id

## Relationships

DimDate[Date] 1 → * FactOnlineSales[Date]
DimDate[Date] 1 → * FactStoreSales[Transaction Date]

DimProduct[Product ID] 1 → * FactOnlineSales[Product ID]
DimProduct[Product ID] 1 → * FactStoreSales[Product ID]

DimGeography[State] 1 → * FactOnlineSales[Ship To State]
DimGeography[State] 1 → * FactStoreSales[Store State]

DimStore[Store ID] 1 → * FactStoreSales[Store ID]

Cardinality: One-to-many
Cross-filter direction: Single
Filter direction: Dimension → Fact
Relationship: Active

## Open Questions

- Can book list titles be reliably macthed to Product names?