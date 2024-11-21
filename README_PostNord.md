
# README for Exam Project: Advanced Visual Analytics

---

## Project Overview
This project was undertaken as part of the Advanced Visual Analytics module (MB221). The goal is to analyze and visualize logistical data from PostNord, a major logistics company, to generate actionable insights. The deliverables include:
1. A working dashboard for managers.
2. Data workflows for preprocessing and transformations.
3. A report detailing methodology, transformations, and insights.

---

## Dataset Description
The data comes from the DDS system and covers four key product types along with supporting master data. It was downloaded and cleaned to facilitate visualization and analytics.

### Products:
1. **Innight (I)**: Time-critical overnight deliveries completed before 7 AM.
2. **Groupage (G)**: Consolidated shipments of pallets up to 2,500 kg.
3. **Pallet (L)**: Transport of individual pallets weighing up to 1,000 kg.
4. **Road Freight (R)**: Part- and full-load transportation for shipments up to 53 pallets.

### Master Data
Customer and postal code information used to enrich the analysis.

### GeoNames Data
External dataset containing latitude and longitude for geospatial analysis.

### File Organization
- Files are named as `Datadump<Product Code>_YYYY_MMM`. Example: `DatadumpR_2019_Jun`.
- Prefixes:
  - `E`: Innight
  - `G`: Groupage
  - `P`: Pallet
  - `R`: Road Freight

### Data Periods
- Innight, Groupage, and Pallet: January 2017 – August 2019
- Road Freight: May 2019 – August 2019 (IT integration was completed in 2019)
- Legacy data from January 2017 to April 2019 for Road Freight is stored in a separate `Easy Forward` system.

---

## Steps Taken

### 1. Data Cleaning and Preprocessing
- **Python Notebook**: The uploaded script (`PostNord_Logistics_Visual_Analytics.ipynb`) cleans, integrates, and transforms the data for analysis. Key tasks include:
  - Handling missing values.
  - Standardizing product codes and column names.
  - Adding geospatial data using the GeoNames dataset for route analysis.
- **Output**: Cleaned datasets were structured and exported for use in Tableau dashboards.

### 2. Dashboard Development
- Developed in Tableau to address the following:
  - Insights into industry segments per product.
  - Geospatial visualization of deliveries.
  - Identification of top customers and revenue-generating routes.
  - Comparison of industry segments across products.
- Restrictions and parameters, such as weight limits for certain product types, were implemented as per the provided guidelines.

### 3. Key Variables
- **Customer_ID**: Unique identifier for corporate customers.
- **Product**: Product type (I, G, L, R).
- **Freight**: Base delivery charge.
- **Surcharges**: Additional charges for special services, e.g., dangerous goods, energy surcharge.
- **Price_Paid**: Total cost paid by the customer (sum of freight and surcharges).
- **ShipmentDate**: Date when the shipment was processed.

---

## Folder Contents
- **Dashboard**: Tableau Packaged Workbook with embedded data.
- **Python Code**: Jupyter Notebook (`.ipynb`) detailing the cleaning and preprocessing workflow.
- **Documentation**: Supporting documents including the variable descriptions and project guidelines.

---

## Insights and Usage
### 1. Actionable Insights
- Geospatial heatmaps identify high-demand regions.
- Industry segment analysis shows revenue breakdown by product type.
- Customer analysis highlights top contributors by revenue.
- Optimized delivery routes reduce CO2 consumption and operational costs.

### 2. Usage for Decision-Making
- Managers can use the dashboard to allocate resources efficiently.
- Insights from historical data enable prediction of future trends.
- The dashboard supports operational and strategic decisions by providing a comprehensive view of logistics operations.

---

## How to Access and Run
1. Open the Tableau file (`.twbx`) in Tableau Desktop.
2. Review the Jupyter Notebook to understand the data cleaning process.
3. Ensure all required Python libraries are installed to rerun the cleaning script if necessary.

---

## Acknowledgments
This project follows the guidelines and requirements set by Kristiania University. Special thanks to the course instructor, Lester Lasrado, for providing the resources and datasets used in this project.

For any questions, contact: LesterAllan.Lasrado@kristiania.no
