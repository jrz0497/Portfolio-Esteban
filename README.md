# Portfolio-Esteban
Overview of the Projects done within my MBA 

# Project 1: City of Vancouver AWS Data Analytic Platform Part 1

**Objective**

To design and implement a Data Analytic Platform (DAP) for the City of Vancouver using AWS services, addressing key requirements:

    1. Support descriptive analysis for identifying trends and insights.
    2. Add features for exploratory analysis to discover patterns in data.
    3. Calculate the monthly cost of running the platform in AWS.

**Dataset**

The project utilizes the Issued Building Permits dataset from the City of Vancouver, filtered to include only permits issued in Downtown Vancouver in 2024. Key fields include:

    Permit Category: Classification of permits (e.g., Commercial, Residential).
    Specific Use Category: Detailed subcategories of permits.
    Type of Work: Type of construction work associated with the permits.
    Property Use: General use classification of properties.

![Screenshots/Project Part 1 Diagram.png](https://github.com/jrz0497/Portfolio-Esteban/blob/772fcc995fdacc7e0fead93de365a468d873dce0/Screenshots/Project%20Part%201%20Diagram.png)

**Methodology**

    Data Ingestion:
        Stored raw data in AWS S3 for scalable and reliable access.

    Data Profiling:
        Used AWS Glue DataBrew to analyze schema, null values, and inconsistencies.

    Data Cleaning:
        Applied transformations in AWS Glue to handle missing values, standardize formats, and ensure data consistency.

    Data Pipeline Design:
        Built an ETL pipeline using AWS Glue for seamless data flow from raw to cleaned and transformed datasets.

    Descriptive Analysis:
        Conducted analysis in AWS Athena to answer key business questions, such as identifying the most requested permit categories.

![Screenshots/Project Part 1 Glue.png](https://github.com/jrz0497/Portfolio-Esteban/blob/e5568bb1ff7f9ecb98880c0b033ff2d297a8ab43/Screenshots/Project%20Part%201%20Glue.png)

**Tools and Technologies**

    AWS S3: For scalable storage of raw and cleaned datasets.
    AWS Glue: For data cleaning, transformation, and ETL pipeline creation.
    AWS Glue DataBrew: For data profiling and initial cleaning.
    AWS Athena: For querying and analyzing data with SQL.

**Deliverables**

A Data Analytic Platform supporting:

    Descriptive analysis (e.g., identifying most common permit categories).
    Exploratory analysis (e.g., understanding patterns by permit type and category).
    A cost analysis showing a monthly AWS expense of approximately $8.57.

**Key Insights**

    The platform effectively handles data ingestion, profiling, cleaning, and transformation.
    Downtown Vancouver's most common permits in 2024 are categorized under [insert key insight here, e.g., "Commercial Use"].
    The platform demonstrates scalability and cost-efficiency, with potential for further enhancements in performance and sustainability.
---

# Project 1: City of Vancouver AWS Data Analytic Platform Part 2

**Objective**

To enhance the AWS Data Analytic Platform by incorporating additional steps to enrich, protect, govern, and observe data. These enhancements address key requirements for improving data quality, security, and monitoring for the City of Vancouver.

# EDIT THIS FOTO TO FIT THIS PART
![Screenshots/Project Part 1 Diagram.png](https://github.com/jrz0497/Portfolio-Esteban/blob/772fcc995fdacc7e0fead93de365a468d873dce0/Screenshots/Project%20Part%201%20Diagram.png)

**Methodology**

1. Data Enriching

Objective: Analyze how holidays affect the issuance of building permits.
   
    Method:
        Downloaded the latest dataset for 2024 and filtered it for Downtown Vancouver.
        Added a holiday indicator column to flag if permits were issued near Canadian holidays.

Enhanced the data pipeline with a comparison of:

            Days to the next holiday
            Specific use category
            Count of permits issued
        
Created aggregated outputs to help the city analyze trends in permit approval near holidays.

Results:

    Used AWS Athena to query enriched data, showing 67 permits issued in April.

2. Data Protection

    Objective: Secure data and ensure recovery of older file versions.

       Method:
        Created and assigned AWS Key Management Service (KMS) for server-side encryption of all S3 buckets.
        Enabled bucket versioning for historical tracking and recovery.
        Restricted bucket access to approved users only (no public access).
        Added a replication rule to backup buckets with encryption, reducing costs for new objects.

3. Data Governance

    Objective: Ensure data quality and prevent exposure of sensitive information.
   
       Method:
       Detected and removed sensitive data, such as email addresses, SIN numbers, and geographical locations.
       Ensured data uniqueness by verifying permit numbers to prevent duplicates.
   
        Implemented a quality pipeline:
            Passed folder: Permits that meet quality criteria.
            Failed folder: Permits that fail quality checks.
   
    Results:

       Improved data accuracy and compliance with privacy standards.

4. Data Observability

    Objective: Monitor the platform’s performance and ensure budget adherence.

       Method:
        Set up CloudWatch alarms:
            Alert when bucket items exceed 500.
            Email notifications for city officials.
   
   Created a CloudWatch dashboard:

       Tracked object counts and bucket sizes for key buckets (e.g., raw, trf).
       Monitored budget alarms and compared costs between S3 and Glue services.

   Included number indicators and gauges for:

       Total platform cost
       Glue charges
   
   Results:
   Dashboard insights enabled better cost management and streamlined bucket monitoring.
    
# EDIT THIS FOTO TO FIT THIS PART
![Screenshots/Project Part 1 Glue.png](https://github.com/jrz0497/Portfolio-Esteban/blob/e5568bb1ff7f9ecb98880c0b033ff2d297a8ab43/Screenshots/Project%20Part%201%20Glue.png)

Tools and Technologies

AWS Services:

    S3 (Storage, Versioning, Replication)
    Glue (ETL Pipelines, Crawlers)
    Athena (SQL Queries)
    KMS (Encryption)
    CloudWatch (Monitoring and Alerts)

Programming:

    SQL for Athena queries

Deliverables

Enhanced Data Analytic Platform with:

    Enriched datasets analyzing holiday effects on permit issuance.
    Secure and compliant storage practices with KMS encryption and bucket versioning.
    Governed data pipelines ensuring quality and sensitivity controls.
    Observable metrics and dashboards for platform performance and cost tracking.

Key Insights

    Holidays had no significant effect on the number of permits issued, as determined from the enriched dataset.
    Versioning and replication rules ensure data recovery while minimizing costs for new objects.
    CloudWatch dashboards provide real-time insights into platform usage, helping the city optimize operations and manage expenses effectively.
