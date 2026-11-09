# Urban Mobility Analytics Pipeline: NYC Transit Big Data

## 📌 Overview
As urban mobility data grows at an unprecedented scale, traditional analytical tools struggle to process the sheer volume of daily dispatch records. This project builds a robust, distributed Big Data architecture to analyze over 4.5 million Uber rides across New York City in real time, mapping transit density and related spatial anomalies. 

Beyond tracking peak dispatch hours, these mobility patterns form the foundation for assessing localized transit hubs, predicting high-density scenarios, and uncovering hidden spatial dynamics pivotal for smart policing and emergency response resource allocation.

## 🏗️ Architecture & Tech Stack
To bypass the slow disk I/O of traditional methods, this system utilizes in-memory processing to create a high-performance Online Analytical Processing (OLAP) pipeline capable of querying millions of rows in milliseconds.

* **Compute Engine:** Apache Spark (PySpark)
* **Distributed Storage:** Hadoop Distributed File System (HDFS)
* **Visualization & BI:** Apache Zeppelin
* **Languages:** Python, SQL

## 📂 Repository Structure
* `mobility_analytics_pipeline.ipynb`: The core PySpark notebook containing data ingestion, relational joins between the transit and weather datasets, data cleaning, and OLAP query logic.
* `Urban_Mobility_Presentation.pdf`: Architectural overview and project presentation slides.
* `nyc_trips_sample.csv` & `weather_sample.csv`: Truncated data samples (first 500 rows) provided for schema reference and pipeline testing. *(Note: The full 4.5M+ row dataset is excluded due to size constraints).*

## 📊 Interactive Analytics & Dashboarding
To make backend insights accessible, the infrastructure is wired directly into **Apache Zeppelin**, serving as an interactive data visualization layer. 

Rather than relying on static reports, Zeppelin connects directly to the Spark cluster via a PySpark interpreter. This allows complex, distributed SQL queries to be executed dynamically and instantly translated into presentation-ready visual charts, creating a seamless environment for exploratory data analysis (EDA). Ultimately, this pipeline bridges the gap between complex backend data engineering and intuitive visual analytics.
