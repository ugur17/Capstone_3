# Transformation Log

## DimProduct

### Sources 
- Products
- Book List

### Transformations
- Standardized Product ID, Product Name and Category Name fields
- Standardized "Technology & Accessories" to "Technology" in Category Name field
- Parsed the Book List text into Product Name and Author
- Enriched DimProduct with Book List using fuzzy matching


### Business Rules
- Products is authoritative for Product ID and category attributes
- Book List is authoritative for book titles and authors
- General audience books exclude Study Guides and Reference Materials subcategories
- Matched Book List titles replace inconsistent Product Names in the Products table
- Author is populated only for general audience books (Excluding Study Guides and Reference Materials subcategories)
- Inventory Categories is the authoritative reference for category names
- Category Description was excluded because it is not required for the analysis

### Validation
- Product Name duplicates is 0
- General audience books: 90
- General audience books missing author: 0
- Two title inconsistencies were resolved through fuzzy matching.
- All 6 Product categories exist in Inventory Categories