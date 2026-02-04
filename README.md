# Supply_chain_analysis

**Tech Stack:** Python (Pandas) ➔ MySQL ➔ Power BI

**Business Domain:** Supply Chain, Logistics, and Manufacturing

## 📝 Project Overview

This project simulates a real-world enterprise data pipeline. I transformed raw, fragmented supply chain data (CSV/Excel) into a structured relational database to perform deep-dive analytics on revenue, supplier risk, and logistics efficiency. The final output is an interactive **Executive Command Center** dashboard.

---

## ⚙️ Data Pipeline Architecture

### 1. Data Cleaning & Extraction (Python)

* **Source:** Raw CSV/Excel datasets.
* **Processing:** Used `pandas` to handle missing values, correct data types (e.g., ensuring Price is numeric), and perform outlier detection.

### 2. Relational Database Modeling (MySQL)

* **Schema Design:** Imported cleaned data into `supply_chain_db`.
* **Advanced SQL (Views):** Created specialized views for modular analysis:
* `vw_inventory_status`: Tracks stock-out risks and replenishment needs.
* `vw_supplier_performance`: Analyzes defect rates and lead times per vendor.
* `vw_logistics_performance`: Calculates total fulfillment cycles.



### 3. Business Intelligence (Power BI)

* **Connectivity:** Established a live connection to MySQL Workbench.
* **Data Modeling:** Built relationships between tables and created custom DAX measures (e.g., *Stock Health %* and *Revenue Growth*).
* **UI/UX:** Designed a professional-grade dashboard with high data density, utilizing:
* **KPI Cards:** For instant Revenue/Profit snapshots.
* **Treemaps:** For SKU-level stock-out risk heatmaps.
* **Gauges:** For tracking fulfillment lead-time goals.



---

## 📊 Key Business Insights & Analytics

The project addresses 16 critical areas of supply chain management, including:

* **Risk Mitigation:** Identifying "Immediate Audit" suppliers based on defect rates > 10%.
* **Cost Efficiency:** Comparing shipping carriers to find the lowest cost-to-time ratio.
* **Inventory Optimization:** Detecting overstocked items vs. critical low-stock items using a custom Stock-to-Sales ratio.
* **Revenue Analysis:** Segmenting top-performing product types (e.g., Skincare vs. Haircare).

---

## 🛠️ Installation & Usage

1. **Python:** Run `data_cleaning.py` to generate the `cleaned_supply_chain.csv`.
2. **SQL:** Execute `schema_setup.sql` in MySQL Workbench to build the database and views.
3. **Power BI:** Open `Supply_Chain_Dashboard.pbix` and refresh the data source to link to your local MySQL instance.

---

## 🚀 Future Enhancements

* **Predictive Analytics:** Integrating a Machine Learning model in Python to predict future demand.
* **Automation:** Setting up a CRON job to auto-refresh the SQL database from a cloud folder.
