# Netflix-Azure-Data-Engineering-Project
![Azure](https://img.shields.io/badge/Microsoft%20Azure-0089D6?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

---

## 📌 Project Overview
This project implements an end to end data engineering workflow leveraging Azure Data Services, Databricks, and Delta Live Tables to enable incremental data processing, transformation, and reporting. The architecture follows the **Medallion Architecture**, ensuring reliability, scalability, and efficient data processing.

---

## 🎯 Business Requirements
This data pipeline is designed to:
- ✅ Automate incremental data ingestion from multiple sources.
- ✅ Securely store raw and processed data in **Azure Data Lake Gen2**.
- ✅ Use **Databricks Delta Live Tables** for real-time and incremental data transformation.
- ✅ Implement a **Medallion Architecture** (Bronze, Silver, Gold) for optimized data structuring.
- ✅ Enable high-performance querying via **Azure Synapse Analytics**.
- ✅ Deliver business insights through **Power BI dashboards**.
- ✅ Maintain **security** and **version control** using GitHub.

---

## 🏗️ Solution Overview
The pipeline follows a structured data flow based on the **Medallion Architecture**:

### 🔹 Data Sources
- 🌍 **HTTP API**: Ingested using **Azure Data Factory**.
- 📂 **File from Azure Storage Account**: Ingested using **Databricks**.

### 🔹 Data Ingestion (Bronze Layer)
📡 **Azure Data Factory** extracts HTTP data and loads it into **Azure Data Lake Gen2**.
📦 **Databricks** processes files from Azure Storage and loads raw data into **Azure Data Lake Gen2**.

### 🔹 Transformation (Silver Layer)
⚙️ **Databricks Delta Live Tables** processes raw data:
- Cleans, deduplicates, and validates data.
- Stores transformed data in the Silver layer of **Azure Data Lake Gen2**.

### 🔹 Aggregation & Serving (Gold Layer)
🗄️ The refined data is stored in the **Gold layer** of **Azure Data Lake Gen2** for optimized querying and analytics.

### 🔹 Warehouse & Reporting
🏛️ The Gold layer data is loaded into **Azure Synapse Analytics** for analytical querying.
📊 **Power BI** is used to create dynamic dashboards for business intelligence.

---
## 📋 Data Architecture
![NetflixDataArch](https://github.com/shivaaganesh3/Netflix-Azure-Data-Engineering-Project/blob/2131138912a2fefe96ad6856a2149e1ec5a744e0/netflix_project_architecture.png)


---

## 🛠️ Technology Stack
| Technology | Purpose |
|-----------------|---------------------------|
| ![Azure Data Factory](https://img.shields.io/badge/Azure%20Data%20Factory-0089D6?style=flat&logo=microsoft-azure&logoColor=white) | Data Ingestion (HTTP) |
| ![Azure Data Lake](https://img.shields.io/badge/Azure%20Data%20Lake-0089D6?style=flat&logo=microsoft-azure&logoColor=white) | Storage Layer (Bronze, Silver, Gold) |
| ![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white) | Data Transformation (Delta Live Tables) & File Ingestion |
| ![Synapse](https://img.shields.io/badge/Azure%20Synapse-0089D6?style=flat&logo=microsoft-azure&logoColor=white) | Analytical Queries & Serving |
| ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white) | Version Control & Security |

---


## 🔒 Security & Best Practices
- **GitHub Integration:** Maintain version control and CI/CD workflows.
- **Data Encryption:** Ensure data security across all layers.
- **Access Control:** Implement role-based access policies.
- **Monitoring & Logging:** Use Azure Monitor for tracking pipeline performance.

---

## 🎯 Conclusion
This project delivers an advanced data pipeline using Azure services and **Delta Live Tables**, following the **Medallion Architecture** for structured data processing. With **Synapse Analytics** and **Power BI**, the solution ensures scalable and high-performance analytics. 🚀
