# medallion-vehicle-pipeline
Chicago Transit Lakehouse

An end-to-end data engineering pipeline built with Apache PySpark to ingest, clean, and model Chicago vehicle data using the Medallion Architecture (Bronze, Silver, Gold layers) and a Star Schema design, featuring automated Parquet storage and Spark SQL querying.

Architecture Overview

Bronze Layer: Ingests raw JSON data straight from the Chicago Open Data API (tx35-q6ia), handling schema structures and persisting them reliably as Apache Parquet files.

Silver Layer: Cleans datasets by dropping duplicates, handling nulls, enforcing strict data types (strings, integers, dates), and standardizing column naming conventions.

Gold Layer (Star Schema): Implements relational dimensional modeling containing a fact table (fact_vehicles) and dimension tables (dim_vehicle, dim_company) using cryptographic hashing for company keys.
