# End-to-End Big Data Analytics Pipeline Using MRJob, Pig & Hive

> Designed and implemented a distributed data processing pipeline on Hadoop using Python MRJob, Apache Pig, and Apache Hive to analyze large-scale NOAA weather records.

**Author:** Amisha Farhana Shaik  
**Project Type:** Big Data Engineering | Distributed Analytics | Hadoop Ecosystem Integration  

---

## Project Overview

This project builds a complete big data analytics pipeline on a Hadoop cluster using real NOAA NCDC weather data.

The pipeline consists of three stages:

1. **Python MRJob (MapReduce)** – Extract Year and Temperature from raw weather records  
2. **Apache Pig** – Compute yearly minimum and maximum temperatures  
3. **Apache Hive** – Compute yearly average temperatures  

The objective was to demonstrate how raw distributed data can be transformed into structured, queryable analytics outputs across multiple Hadoop ecosystem tools.

---

## Dataset

- NOAA NCDC weather records  
- Compressed `.gz` files  
- Large-scale historical climate dataset  
- Fixed-width raw record format  

---

# Part 1: Python MRJob – Distributed Data Extraction

## Objective

Extract `(Year, Temperature)` pairs from raw NCDC weather records using a distributed MapReduce job written in Python.

## Implementation

- Transferred dataset and MRJob script to Hadoop cluster  
- Decompressed `.gz` weather files  
- Consolidated records into a single dataset  
- Executed MRJob script on Hadoop  
- Generated structured output directory  
- Cleaned output formatting  
- Produced final text file: `year_temperature_data.txt`

## Key Learning

- Writing MapReduce jobs in Python using MRJob  
- Parsing fixed-width large-scale datasets  
- Running distributed jobs on Hadoop  
- Generating structured intermediate data  
- Handling output formatting in distributed environments  

This stage transforms raw climate records into structured year-temperature data.

---

# Part 2: Apache Pig – Yearly Min & Max Analysis

## Objective

Load processed temperature data into Pig and compute:

- Minimum temperature per year  
- Maximum temperature per year  

## Implementation

- Loaded structured text file into Pig  
- Defined schema explicitly  
- Grouped records by year  
- Applied aggregation functions (`MIN`, `MAX`)  
- Stored distributed output in HDFS  

## Key Learning

- Schema handling in Pig  
- Distributed grouping and aggregation  
- Large-scale data summarization  
- Intermediate analytics processing layer  

Pig provides a higher-level abstraction over MapReduce for analytical workflows.

---

# Part 3: Apache Hive – Yearly Average Temperature

## Objective

Use Hive (SQL on Hadoop) to compute:

- Average temperature per year  

## Implementation

- Created Hive table with defined schema  
- Loaded structured text file into Hive  
- Executed aggregation query:

```sql
SELECT year, AVG(temperature) AS avg_temp
FROM year_temp
GROUP BY year
ORDER BY year;
```

## 📌 Key Learnings

- Schema-on-read architecture  
- SQL-based analytics over HDFS  
- Data warehousing concepts in Hadoop  
- Distributed aggregation using Hive  
- Hive enables structured querying over distributed storage  

---

## 🏗️ End-to-End Architecture
Raw NOAA Data (.gz files)
        ↓
Python MRJob (MapReduce Processing)
        ↓
Structured Year–Temperature Dataset
        ↓
Apache Pig (Min / Max Aggregation)
        ↓
Apache Hive (Average Aggregation via SQL)

This pipeline demonstrates **layered distributed processing** across multiple Hadoop ecosystem components.

---

## 🛠️ Technical Skills Demonstrated

- Python MRJob development  
- Hadoop cluster execution  
- Distributed file processing  
- Fixed-width record parsing  
- Apache Pig scripting  
- Apache Hive table modeling  
- SQL over HDFS  
- Data transformation and cleaning  
- End-to-end distributed data pipeline design  

---

## 🚀 Why This Project Is Important

This project demonstrates:

- Multi-tool Hadoop ecosystem integration  
- Real-world large-scale dataset processing  
- Distributed system execution  
- Structured analytics on big data  
- Hybrid programming across Python, Pig, and Hive  
- Production-style data pipeline thinking  

It showcases the ability to move from **raw distributed data** to **structured analytical insights** using scalable big data technologies.

---

## 📊 Applications

This project demonstrates applications in:

**Big Data Engineering | Distributed Data Pipelines | Hadoop Ecosystem | Data Warehousing | Scalable Analytics**

---
