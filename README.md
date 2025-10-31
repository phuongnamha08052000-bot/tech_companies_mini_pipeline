# tech_companies_mini_pipeline
A lightweight data pipeline on a large tech-company dataset

Overview
I built a lightweight data pipeline on a large tech-company dataset (public Crunchbase export) to practice data wrangling, format conversion, and a quick web UI. The project ingests CSV, cleans and filters companies, converts to JSON, and serves a searchable HTML table for New York–based firms via a tiny Flask app. 

Process
Ingest & profiling: Loaded a 1.1M-row CSV into pandas and audited schema/nulls.
Cleaning: Dropped nameless orgs; filtered to US companies; then further filtered names starting with “ad*” (case-insensitive).
Serialization: Converted the filtered DataFrame to a structured JSON file (records orientation) for reuse and interchange.
City filter: Re-hydrated JSON to a DataFrame and isolated New York companies.
Delivery: Published a minimal Flask app that renders the NY subset as a styled HTML table (fast way to “productize” a dataset).
Skills: pandas (ETL), JSON I/O, basic data quality checks, rapid Flask prototyping.

