# 📊 dbt Project – Sales Data Transformation

This repository contains a **dbt (Data Build Tool)** project that transforms raw source data into structured, analytics-ready datasets using a **Bronze → Silver** modeling approach.
![LuxuryFashionBrandsEmbraceSustainabilitywithEcoMaterials-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/59e70d82-1d53-4263-b0b0-fa70feb49836)


---

## 📌 Project Overview

### 🔹 Source Tables (Raw Data)

* `dim_customer`
* `dim_product`
* `fact_sales`

### 🔹 Bronze Layer (Staging / Cleansing)

* `bronze_customer` – cleans and standardizes customer dimension data.
* `bronze_product` – prepares product dimension data.
* `bronze_sales` – processes raw sales transactions.

### 🔹 Silver Layer (Business Models)

* `silver_salesinfo` – combines customer, product, and sales data for reporting and analytics.

This layered approach ensures:

* ✅ Clear separation between raw and transformed data
* ✅ Easier debugging and auditing
* ✅ Reusable models for advanced analytics

---

## 🛠️ Tech Stack

* **dbt Core / dbt Cloud**
* **SQL** (adapter can be Postgres, BigQuery, Snowflake, or Redshift – update based on your setup)
* **GitHub** for version control

---

## 🚀 Getting Started

### 1️⃣ Clone the repo

```bash
git clone https://github.com/your-username/your-dbt-project.git
cd your-dbt-project
```

### 2️⃣ Install dbt

```bash
pip install dbt-core dbt-postgres   # replace with your adapter
```

### 3️⃣ Configure your profile

Add database connection details in `~/.dbt/profiles.yml`:

```yaml
your_project_name:
  target: dev
  outputs:
    dev:
      type: databricks      # or snowflake/bigquery/redshift
      host: localhost
      user: your_user
      password: your_password
      dbname: your_db
      schema: analytics
      threads: 4
```

### 4️⃣ Run dbt

```bash
dbt run
```

### 5️⃣ Test dbt models

```bash
dbt test
```

---

## 📸 Lineage Graph

Below is the lineage graph of this project (Bronze → Silver flow):
<img width="1336" height="966" alt="Screenshot 2025-09-23 at 08 55 03" src="https://github.com/user-attachments/assets/257f83bf-0ae6-452d-902f-320cab949026" />


---

<img width="1440" height="900" alt="Screenshot 2025-09-10 at 14 09 56" src="https://github.com/user-attachments/assets/0d037e4c-d5ed-41a8-ac2c-69fb9b47ca8a" />
<img width="1440" height="900" alt="Screenshot 2025-09-14 at 22 38 44" src="https://github.com/user-attachments/assets/4fca4afa-2663-4cc7-ab48-15f599d53ef8" />
<img width="1440" height="900" alt="Screenshot 2025-09-16 at 22 23 14" src="https://github.com/user-attachments/assets/8b3fa580-e9dd-4107-b7a8-0ed0beef7f9a" />
<img width="1920" height="1077" alt="Screenshot 2025-09-18 at 13 58 39" src="https://github.com/user-attachments/assets/4a79f006-0218-4aa2-a65d-6f3105b9f0c9" />
<img width="1340" height="1033" alt="Screenshot 2025-09-22 at 20 01 18" src="https://github.com/user-attachments/assets/2bf80236-9414-4256-96a5-761595a60064" />
<img width="1080" height="1350" alt="Luxury Fashion Brands Embrace Sustainability with Eco Materials (1)" src="https://github.com/user-attachments/assets/5e778e10-53ec-495c-aded-313905fbf004" />
<img width="1080" height="1350" alt="Luxury Fashion Brands Embrace Sustainability with Eco Materials" src="https://github.com/user-attachments/assets/35318ca3-780e-4e6b-99d6-3e35d1d8fce8" />

