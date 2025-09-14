# Dashboard Design Rationale

## Design Philosophy
The dashboards were designed following core principles of data visualization: clarity, accuracy, efficiency, and visual appeal. The goal was to present complex information in an intuitive way, enabling users to quickly identify trends, outliers, and key metrics.

## 1. Finance Dashboard Design

### Layout & Widgets:
*   **Top Section:** KPI Cards for high-level summary (Revenue, Expenses, Net Income).
*   **Middle Left:** Profit & Loss Trend Line Chart to show performance over time.
*   **Middle Right:** Expense Breakdown Pie Chart to show cost composition.
*   **Bottom Left:** Cash Flow Waterfall Chart to show cash movements.
*   **Bottom Right:** Actual vs. Budget Bar Chart for variance analysis.

### Color Scheme:
*   **Green** for positive values (Revenue, Net Income).
*   **Red** for negative values (Expenses, Cash Outflow).
*   **Blue** for neutral/balance figures (Assets, Liabilities).

### Interactivity:
*   A centralized **Date Range** filter controls all widgets.
*   **Drill-down** enabled on the P&L chart from Year → Quarter → Month.

## 2. Sales Dashboard Design

### Layout & Widgets:
*   **Top Section:** KPI Cards for Total Sales, Profit, and Pipeline Value.
*   **Middle Left:** Sales Funnel Chart to visualize the conversion pipeline.
*   **Middle Right:** Geo Map to show sales performance by country/region.
*   **Bottom Left:** Forecast vs. Actual Line Chart for time-series analysis.
*   **Bottom Right:** Table with Product Category sales (with drill-down to product names).

### Color Scheme:
*   **Gradient of Blue** for the funnel chart stages (dark to light).
*   **Green-Yellow-Red** gradient on the geo map to indicate performance.

### Interactivity:
*   **Region Filter** to focus on specific geographic areas.
*   **Product Category Filter** to analyze specific product lines.
*   **Cross-filtering:** Clicking on a region in the map filters other charts.

## 3. HR Dashboard Design

### Layout & Widgets:
*   **Top Section:** KPI Cards for Headcount, Attrition Rate, and Open Positions.
*   **Middle Left:** Attrition Trend Line Chart (12-month period).
*   **Middle Right:** Headcount by Department Bar Chart.
*   **Bottom Left:** Hiring vs. Attrition Combo Chart.
*   **Bottom Right:** Donut Chart showing attrition by Job Role.

### Color Scheme:
*   **Neutral Blues and Greys** for general metrics.
*   **Highlighted Red** for attrition-related metrics to draw attention.

### Interactivity:
*   **Department and Location Filters** for segmented analysis.
*   **Tooltips** on charts show detailed numbers on hover.

## Accessibility Considerations
*   Used color-blind friendly palettes where possible.
*   Ensured sufficient contrast between text and background colors.
*   Added clear labels and titles to all charts for clarity.
