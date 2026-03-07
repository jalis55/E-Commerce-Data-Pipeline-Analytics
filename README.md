# eCommerce Data Pipeline & Analytics

A comprehensive data engineering project that implements a **Medallion Architecture** to process and analyze eCommerce data. This project transforms raw eCommerce data (customers, products, orders) into actionable business insights through a series of structured data processing layers.

---

## 🏗️ Project Architecture

This project follows the **Medallion Architecture** (Bronze, Silver, Gold) to ensure data quality, reliability, and scalability.

-   **Bronze (Raw)**: Captures raw ingestion data in its original format.
-   **Silver (Cleansed & Conformed)**: Performs data validation, cleaning, and normalization.
-   **Gold (Curated Business-Level)**: Aggregates and denormalizes data for high-performance reporting and analytics.

---

## 📂 Project Structure

The project is organized into four main functional areas:

### 1. `0_data/`
Contains the raw data sources for the eCommerce platform.
-   **`ecomm-raw-data/`**: Subdirectories for `brands`, `category`, `customers`, `date`, `order_items`, and `products`.

### 2. `1_codes/`
The core engine of the project, containing the processing logic.
-   **`1_setup/`**: Initial infrastructure and catalog setup.
-   **`2_medallion_processing_dim/`**: Dimension table processing (Bronze -> Silver -> Gold).
-   **`3_medallion_processing_fact/`**: Fact table processing (Bronze -> Silver -> Gold).

### 3. `2_genie_exploration/`
Focuses on data discovery and answering critical business questions.
-   **`questions.txt`**: A collection of analytical queries regarding revenue trends, top products, customer distribution, and regional performance.

### 4. `3_dashboard/`
Assets for visualization and reporting.
-   **`denormalise_table_query.txt`**: SQL queries to create a high-performance denormalized view (`fact_transactions_denorm`) joining fact and dimension tables for dashboard consumption.

---

## 🚀 Getting Started

### Prerequisites
-   **Databricks** or a compatible **PySpark** environment.
-   **Python 3.x** and **Jupyter Notebooks**.

### Processing Flow
1.  Run `1_setup/setup_catalog.ipynb` to initialize the database environment.
2.  Execute dimension processing notebooks in `2_medallion_processing_dim/` in order (Bronze -> Silver -> Gold).
3.  Execute fact processing notebooks in `3_medallion_processing_fact/` in order (Bronze -> Silver -> Gold).
4.  Use the SQL in `3_dashboard/` to create analytical views for reporting.

---

## 📊 Business Insights

The project is designed to answer key business questions, such as:
-   **Revenue Trends**: Monthly revenue analysis and year-over-year growth.
-   **Product Performance**: Identification of top-performing products by brand and category.
-   **Customer Analytics**: Geographical distribution and average revenue per customer.
-   **Operational Excellence**: Analyzing peak revenue days and segment-driven growth.

---

## 🛠️ Technologies Used
-   **Databricks**: Unified analytics platform.
-   **Apache Spark / PySpark**: Large-scale data processing.
-   **Delta Lake**: ACID transactions and scalable metadata handling.
-   **SQL**: Advanced analytical querying and view creation.
-   **Jupyter**: Interactive development environment.
