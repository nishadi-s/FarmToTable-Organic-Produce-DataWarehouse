# 🥕 Farm-to-Table Produce Delivery Tracker – DWBI Project

🚜 A complete Data Warehousing & Business Intelligence (DWBI) solution to track organic produce delivery from farm to retailer – built for the IT3021 module at 🇱🇰 Sri Lanka Institute of Information Technology.

---

## 📦 Project Overview

This project simulates a real-world organic produce delivery system, capturing the full lifecycle from:

- 🧑‍🌾 **Farmers** and organic certification
- 🥬 **Products** with seasonal availability
- 🛒 **Retailers** and order placements
- 🚚 **Deliveries** with logistics tracking
- 💰 **Payments** and performance analytics

📅 Covers data for the **entire year of 2024** with:
- 50,000+ orders
- 150,000+ order items
- Multiple sales, delivery, and payment insights

---

## 🏗️ Architecture

### 1️⃣ Data Sources (Raw Files)
- 📊 Excel: `Farmers.xlsx`, `Products.xlsx`, `Retailers.xlsx`
- 📄 TXT: `Orders.txt`, `OrderDetails.txt`
- 🧾 CSV: `DeliveryRoutes.csv`, `Payments.csv`, `FarmerUpdates.csv`, `AccmTxnUpdates.csv`

### 2️⃣ ETL Layer – SSIS
- 🔄 Extract, 🧹 Transform (SCD Type 1), 📥 Load
- 🗃️ Intermediate staging tables
- 👮 Data validation, deduplication, integrity checks

### 3️⃣ Data Warehouse – SQL Server
- 📐 Star Schema with:
  - 🧮 `OrderSalesFact`
  - 🧑‍🌾 `FarmerDim`
  - 🥕 `ProductDim`
  - 🏬 `RetailerDim`
  - 📅 `DateDim`
  - 🚚 `DeliveryDim`

### 4️⃣ Analytical Layer – SSAS
- 🧊 `SalesCube` deployed using SSDT
- 📈 Dimensions with hierarchies:
  - 🗓️ Date: Year → Quarter → Month → Day
  - 🌽 Product: Category → SubCategory
  - 🌍 Retailer / Farmer: State → City → Zip

### 5️⃣ Reporting Layer – Power BI
- 📊 Interactive dashboards for:
  - 📦 Product Sales
  - 🚚 Delivery Efficiency
  - 🧑‍🌾 Farmer Performance
  - 🏪 Retailer Trends
  - 📉 Organic Impact on Sales
  - 💳 Payment Method Analysis

---

## 📊 OLAP Operations

| Operation   | Description                                                      |
|-------------|------------------------------------------------------------------|
| 🔼 **Roll-Up**    | Monthly → Quarterly sales aggregation                      |
| 🔽 **Drill-Down** | Category → SubCategory → Month                             |
| 🧪 **Slice**      | Filtered view (e.g., only Certified Farmers)               |
| 🎯 **Dice**       | Focused multi-dimensional filter (Product, Time, Retailer) |
| 🔁 **Pivot**      | Reoriented perspective of the same data                    |

---

## 🛠️ Tools & Technologies

- 🧰 **SSIS** – ETL automation
- 🧊 **SSAS** – OLAP cube development
- 📈 **Power BI** – Reporting & dashboards
- 🧮 **SQL Server** – Data warehouse & star schema
- 🗂️ **Excel, TXT, CSV** – Heterogeneous data sources

---

## 📁 Folder Structure

/📦 CubeProject/CUBE/NDW/  
└── SSAS cube project files

/📂 Data Sources/  
├── CSV/  
│   ├── DeliveryRoutes.csv  
│   ├── Payments.csv  
│   ├── FarmerUpdates.csv  
│   └── AccmTxnUpdates.csv  
├── Excel/  
│   ├── Farmers.xlsx  
│   ├── Products.xlsx  
│   └── Retailers.xlsx  
└── TXT/  
    ├── Orders.txt  
    └── OrderDetails.txt  

/📂 DataWarehouse/  
├── FarmToTableDW_ETL/      # SSIS project files  
└── FarmToTableDW_ETL.sln   # SSIS solution file  

/📂 Documents/  
├── Assignment 01.pdf  
└── Assignment 02.pdf  

/📂 Excel/  
└── FarmToTableOrganicProduce.xlsx  

/📂 PowerBIReports/  
└── Power BI dashboard (.pbix)  

📄 FarmToTableDW.bak         # SQL Server DW backup  
📄 README.md                 # Project overview
