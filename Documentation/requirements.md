# Project Requirements

## 1. Functional Requirements

### Finance Dashboard
- [x] Display Key Performance Indicators (KPIs) for Revenue, Expenses, and Net Income.
- [x] Show a trend analysis of Profit & Loss statements over time.
- [x] Visualize Balance Sheet components (Assets, Liabilities, Equity).
- [x] Illustrate Cash Flow from operating, investing, and financing activities.
- [x] Provide a comparison of Actuals vs. Budget forecasts.

### Sales Dashboard
- [x] Visualize the Sales Pipeline stages (Leads → Opportunities → Closed Deals).
- [x] Display a comparison of Forecasted vs. Actual Sales figures.
- [x] Show sales performance by Region using a geo map.
- [x] Analyze sales by Product Category.
- [x] Include time-based filters (Year, Quarter, Month).

### HR Dashboard
- [x] Track Attrition Rate with monthly and yearly trend lines.
- [x] Monitor Hiring Metrics and Open Positions by department.
- [x] Display Employee Headcount distribution by Department and Location.
- [x] Provide filters for Department, Location, and Tenure.

## 2. Technical Requirements
- [x] **SAP Analytics Cloud Account:** Utilized a trial account for development.
- [x] **Data Modeling:** Created SAC models with defined measures, dimensions, and hierarchies.
- [x] **Data Sources:** Used sample CSV files for Finance, Sales, and HR data.
- [x] **Planning Model:** Built and configured a planning model for the Finance dashboard.
- [x] **Version Control:** Maintained project documentation and screenshots on GitHub.

## 3. Data Requirements
The following sample data fields were used to build the models:

### Finance Data
*   Date (Hierarchy: Year > Quarter > Month)
*   Account Type (Revenue, COGS, Expense, Asset, Liability, Equity)
*   Account Description
*   Department
*   Actual Amount
*   Budget Amount

### Sales Data
*   Date (Hierarchy: Year > Quarter > Month)
*   Region, Country
*   Product Category, Product Name
*   Sales Stage (Lead, Qualified Lead, Proposal, Negotiation, Closed Won)
*   Sales Amount, Quantity, Profit

### HR Data
*   Date (Hierarchy: Year > Month)
*   Employee ID
*   Department, Job Role
*   Location, Country
*   Hiring Date, Attrition Date
*   Tenure, Performance Rating
