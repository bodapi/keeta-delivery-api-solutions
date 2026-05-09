# 🇧🇷 Brazil E-Commerce & Food Delivery Data Hub (São Paulo)

This module represents **BODAPI’s** technical framework for large-scale data acquisition within the Brazilian food delivery ecosystem, specifically targeting the **Keeta** platform. We specialize in high-fidelity extraction of nested menu structures, promotional intelligence, and localized logistical data.

### 🛠 Technical Capabilities

* **Geospatial Data Acquisition**: 
    * Implements a multi-modal collection strategy using both **Shop ID** and **Coordinate-based (GPS) point switching**.
    * Radius-based scanning (2km per point) to ensure 100% coverage of specific urban zones like São Paulo.
* **Protocol-Level Extraction**: 
    * Capable of handling both **Logged-in** and **Non-login states** via App-side protocol interfaces.
    * Optimized for peak-hour collection (10:00-14:00 & 17:00-20:00 BRT) to capture real-time availability and dynamic pricing.
* **Deep-Nested Data Mapping**: 
    * **Menu Intelligence**: Extraction of parent dish items and all associated **Sub-dish/Customization** options.
    * **Promotion Tracking**: Real-time parsing of `activityInfoList` to capture "Must-Try" tags, percentage discounts, and slashed original prices.

### 📊 Data Schema Highlights

| Field | Description | Technical Status |
| :--- | :--- | :--- |
| `batchno` | Unique collection timestamp (yyyyMMdd) | Verified |
| `shop_id` | Unique Merchant Identifier | Verified |
| `item_price` | Current selling price (decimal precision) | Verified |
| `customization` | Full JSON string of sub-dish specs & options | Verified |
| `item_tags` | Multi-tag concatenation (e.g., #1 Best Seller) | Verified |

### 🔍 Specialized Implementation
Our engine handles complex field mapping, ensuring that unit names, order counts, and promotional JSON strings are structured for immediate business analysis or integration into price-comparison models. 

---
