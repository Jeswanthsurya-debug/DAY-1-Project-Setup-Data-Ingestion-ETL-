# DAY-1-Project-Setup-Data-Ingestion-ETL-
Bluestock Fintech
# Mutual Fund Analytics - Phase 1: Data Ingestion & ETL Pipeline

A production-ready Python data pipeline designed to ingest, profile, and cross-validate static financial datasets alongside real-time live pricing data from external AMFI public application servers. 

---

## 🚀 System Pipeline Architecture

* **Static Data Profiling:** Automatically maps structural configurations (`.shape`, `.dtypes`, `.head()`) across all core operational source tables.
* **Live NAV Synchronization:** Extends a data extraction engine to query real-time scheme metrics via REST APIs, standardizing variable schemas.
* **Data Integrity Cross-Validation:** Runs dynamic row mapping validations to identify schema structural changes or identifier code anomalies.

---

## 📁 Repository Overview

| File / Component | Primary Responsibility | Target Output Metrics |
| :--- | :--- | :--- |
| `data_ingestion.py` | Automatically searches and loads local static spreadsheets using Pandas. | Profiles rows, column types, and data structure dimensions. |
| `live_nav_fetch.py` | Queries REST API endpoints for required tracking mutual fund schemes. | Extracts 16,000+ historical entries directly to `live_nav_history.csv`. |
| `validate_master.py`| Normalizes schema header names to map missing references dynamically. | Verifies master reference alignment and logs data anomalies. |
| `requirements.txt`  | Standardizes environmental setup configurations. | Declares external modules needed (`pandas`, `requests`). |

---

## 🛠️ Environment Configuration & Deployment

### 1. Requirements Setup
Initialize a clean local terminal interface environment and execute the library collector:
```bash
pip install -r requirements.txt
