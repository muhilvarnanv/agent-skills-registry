name: data-product-sensible-defaults
description: This skill should be used when establishing, evaluating, or auditing technical stacks for analytical data management, analytics, data engineering, and data product lifecycle management.
triggers:
- data product
- analytical data
- data engineering
- batch analytical processing
- data platform
- data warehouse
---

# Data Product Sensible Defaults

[cite_start]An overview of the recommended technical stack and guidelines for Analytical Data Management, Analytics, and Data Products to prevent ecosystem fragmentation and maximize time-to-value[cite: 24].

## Core Instructions

When building, deploying, or managing data infrastructure and analytics pipelines, adhere to the following directives:

* [cite_start]**Platform Enforcement:** Avoid handcrafting Data Products or managing data infrastructure manually[cite: 23]. [cite_start]It is strongly recommended to leverage **Self-Service Data Platform services** to automate the lifecycle, infrastructure management, monitoring, and alerting[cite: 23, 24].
* [cite_start]**Primary Programming Language:** Use **Python** as the standard language[cite: 24]. [cite_start]The Python ecosystem provides universal support for workflow management, data processing, and machine learning[cite: 24].
* [cite_start]**Cloud Infrastructure Environment:** Default to **Google Cloud Platform (GCP)**[cite: 24]. [cite_start]GCP provides a highly optimized suite of managed services for analytical data management, analytics, machine learning, and business intelligence[cite: 24].
* [cite_start]**Business Intelligence (BI):** Standardize on **Sisense** as the organization's corporate BI platform choice[cite: 24].
* [cite_start]**Data Governance & Access:** Utilize platform-provided services consisting of a **Metadata Management Service** (built on top of Google Data Catalog) and centralized **Data Access Management** via an AuthZ system[cite: 24].

## Common Patterns

### 1. Processing Small to Medium Datasets (Megabytes up to 1 GB)
[cite_start]For batch analytical processing of smaller data footprints that do not require highly complex transformations[cite: 24]:
* [cite_start]**Workflow Management:** Google Cloud Composer (Apache Airflow)[cite: 24].
* [cite_start]**Object Store:** Google Cloud Storage[cite: 24].
* [cite_start]**Output Ports File Format:** Parquet[cite: 24].
* [cite_start]**Data Warehouse:** BigQuery[cite: 24].
* [cite_start]**Data Processing / Transformations:** Pandas[cite: 25].
* [cite_start]*Note on Dask:* Teams can experiment with **Dask** to evaluate lazy processing and memory optimization, but it is currently classified under "Assess" rather than a firm sensible default[cite: 24, 25].

### 2. Processing Large Datasets (> 1 GB)
[cite_start]For large-scale data engineering batches or medium datasets containing highly complex transformation logic[cite: 25]:
* [cite_start]**Workflow Management:** Google Cloud Composer (Apache Airflow)[cite: 25].
* [cite_start]**Object Store:** Google Cloud Storage[cite: 25].
* [cite_start]**File Format:** Parquet[cite: 25].
* [cite_start]**Data Warehouse:** BigQuery[cite: 25].
* [cite_start]**Data Processing / Transformations:** **PySpark with Dataproc** or **Google Cloud Dataflow** depending on specific project use cases[cite: 25].

### 3. Streaming & Microbatch Processing
* [cite_start]**Status:** There are currently no official sensible defaults established for end-to-end streaming architectures due to a lack of historic operational use cases[cite: 25]. [cite_start]Core recommendations will expand once more real-world production telemetry is evaluated[cite: 25].

## Additional Resources

* `TechOps TechStack Sensible Defaults - 2023 Edition.pdf` — Section: "The Recommended Tech Stack for Analytical Data Management & Analytics" (Pages 6–7).