# Setup Instructions

## Prerequisites
1.  **SAP Analytics Cloud Trial Account:** You must have access to an SAC tenant.
    *   Sign up for a free trial here: [https://www.sap.com/products/analytics-cloud/trial.html](https://www.sap.com/products/analytics-cloud/trial.html)

## Step-by-Step Guide

### 1. Data Preparation
*   Download the sample CSV files from the `data/` directory in this repository.
*   Ensure the data is clean:
    *   Check for and remove any blank rows.
    *   Standardize date formats (e.g., to YYYY-MM-DD).
    *   Ensure categorical values (like Department or Region) are consistent.

### 2. Creating Models in SAC
1.  **Navigate to the Modeler:** From your SAC homepage, go to the main menu and select **Modeler**.
2.  **Create a New Model:** Click on the `+` icon and select **Import from a File**.
3.  **Upload Data:** Choose the `finance_data.csv` file and click **Import**.
4.  **Define Dimensions and Measures:**
    *   SAC will auto-detect types. Ensure:
        *   `Date` is set as a **Date** dimension.
        *   `Account Type`, `Department` are set as **Generic** dimensions.
        *   `Actual Amount`, `Budget Amount` are set as **Measures**.
5.  **Create a Hierarchy:** Right-click on the `Date` dimension and create a hierarchy: **Year > Quarter > Month**.
6.  **Repeat:** Repeat steps 2-5 for the `sales_data.csv` and `hr_data.csv` files to create their respective models.
7.  **Save Models:** Save each model with a clear name (e.g., "Finance_Model", "Sales_Model").

### 3. Building the Stories (Dashboards)
1.  **Create a New Story:** From the homepage, click **Create** and select **Story**.
2.  **Choose Canvas Page:** Select a blank canvas for full design flexibility.
3.  **Add Widgets:**
    *   Click **Add Chart** to insert visualizations (e.g., Bar Chart for P&L, Geo Map for Sales).
    *   Click **+** and select **Input Control** to add filters for Date, Region, etc.
    *   Use **Structured Text** for titles and labels.
4.  **Connect Data:** For each widget, choose the corresponding model you created.
5.  **Design and Format:** Use the **Styling** panel on the right to adjust colors, fonts, and formatting.
6.  **Repeat:** Create three separate stories: `Finance_Dashboard`, `Sales_Dashboard`, and `HR_Dashboard`.

### 4. (Optional) Enabling Planning
*   This step is for the Finance planning model.
*   In the **Modeler**, open your `Finance_Model`.
*   Click on the **Planning** tab and enable planning features.
*   Assign necessary permissions and create a version dimension for "Actual" and "Plan" data.

### 5. Taking Screenshots for Documentation
*   Navigate to each completed dashboard.
*   Use your browser's screenshot tool (or a tool like Lightshot) to capture the full dashboard.
*   Save the images as `.png` files in the `screenshots/` directory.
*   Ensure the images are clear and showcase the main features.

## Data Import Steps for Each Dataset

### Financial Data Import:
1. In SAC Modeler, click **+ → Import from File**
2. Upload `financial_performance_dataset.csv`
3. **Critical Step:** Convert the "Month" column to proper date format:
   - Select the "Month" column
   - Change type to **Date**
   - Set date format to `MMM-YY` (e.g., Jan-23)
4. Create hierarchy: **Year → Quarter → Month**
5. Set all numeric columns as **Measures** with Currency format

### HR Data Import:
1. Upload `hr_analytics_sample.csv`
2. Set "EmployeeID", "Attrition", "Department", "JobRole", "EducationField" as **Dimensions**
3. Set "Age", "MonthlyIncome", "YearsAtCompany" as **Measures**
4. For "MonthlyIncome", set aggregation to **Average** for meaningful analysis

### Sales Data Import:
1. Upload `sales_dataset_sample.csv`
2. Set "OrderDate" as **Date** dimension with hierarchy: **Year → Quarter → Month → Day**
3. Set "Region", "Category", "ProductName" as **Dimensions**
4. Set "Sales", "Quantity", "Profit" as **Measures**
5. Enable **Geo Enrichment** for "Region" to enable map visualizations
