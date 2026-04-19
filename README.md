# Microsoft Fabric Earthquake Data Pipeline

End-to-end data engineering pipeline built using Microsoft Fabric, implementing a medallion architecture (Bronze, Silver, Gold) with real-time USGS earthquake data.

---

## 🔧 Architecture Overview

USGS API → Bronze (Raw JSON) → Silver (Structured Delta Table) → Gold (Aggregated Data) → Reporting

---

## 🧱 Pipeline Design

### Bronze Layer
- Ingest raw earthquake data from USGS API
- Store JSON files in OneLake
- Support bootstrap and incremental ingestion

### Silver Layer
- Flatten nested JSON structure
- Standardize schema
- Deduplicate using event_id

### Gold Layer
- Create analytics-ready datasets:
  - Daily earthquake summary
  - Regional activity
  - Magnitude distribution

---

## ⚙️ Orchestration

- Microsoft Fabric Data Pipeline
- Scheduled hourly execution
- Notebook-based transformations

---

## 🚀 Deployment Considerations

- Designed for promotion across Dev → Test → Prod
- Supports parameterization and environment separation
- Aligns with Microsoft Fabric deployment pipeline best practices

---

## 📊 Data Source

- USGS Earthquake API  
https://earthquake.usgs.gov/

---

## 📁 Repository Structure
