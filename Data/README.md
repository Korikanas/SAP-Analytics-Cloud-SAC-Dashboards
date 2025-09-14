# Data Dictionary

##  Financial Data (`financial_performance_dataset.csv`)
| Field Name | Data Type | Description | SAC Modeling Recommendation |
|------------|-----------|-------------|----------------------------|
| Month | Text (Date) | Month-Year of financial data | Convert to **Date** dimension, create hierarchy: Year → Quarter → Month |
| Revenue | Number | Total sales revenue | **Measure** (Currency format, SUM aggregation) |
| CostOfGoodsSold | Number | Direct costs of producing goods | **Measure** (Currency format, SUM aggregation) |
| OperatingExpenses | Number | Indirect business operating costs | **Measure** (Currency format, SUM aggregation) |
| NetIncome | Number | Revenue minus all expenses | **Measure** (Currency format, SUM aggregation) |
| Assets | Number | Company-owned resources | **Measure** (Currency format, SUM aggregation) |
| Liabilities | Number | Company debts and obligations | **Measure** (Currency format, SUM aggregation) |
| Equity | Number | Assets minus Liabilities | **Measure** (Currency format, SUM aggregation) |

##  HR Analytics Data (`hr_analytics_sample.csv`)
| Field Name | Data Type | Description | SAC Modeling Recommendation |
|------------|-----------|-------------|----------------------------|
| EmployeeID | Text | Unique employee identifier | **Dimension** (Generic) |
| Age | Number | Employee age | **Measure** (Number format, AVG aggregation) |
| Attrition | Text | Whether employee left (Yes/No) | **Dimension** (Generic) - Key metric for analysis |
| Department | Text | Employee department | **Dimension** (Generic) - Use for filtering |
| JobRole | Text | Specific job title | **Dimension** (Generic) |
| MonthlyIncome | Number | Monthly salary | **Measure** (Currency format, AVG aggregation) |
| YearsAtCompany | Number | Tenure in years | **Measure** (Number format, AVG aggregation) |
| EducationField | Text | Field of education | **Dimension** (Generic) |

##  Sales Data (`sales_dataset_sample.csv`)
| Field Name | Data Type | Description | SAC Modeling Recommendation |
|------------|-----------|-------------|----------------------------|
| OrderID | Text | Unique order identifier | **Dimension** (Generic) |
| OrderDate | Date | Date of order | **Date** dimension, create hierarchy: Year → Quarter → Month → Day |
| Region | Text | Geographic region | **Dimension** (Generic) - Use for geo mapping |
| Category | Text | Product category | **Dimension** (Generic) - High-level grouping |
| ProductName | Text | Specific product name | **Dimension** (Generic) - Drill-down from Category |
| Sales | Number | Total sale amount | **Measure** (Currency format, SUM aggregation) |
| Quantity | Number | Number of units sold | **Measure** (Number format, SUM aggregation) |
| Profit | Number | Profit from sale | **Measure** (Currency format, SUM aggregation) |
