# Portfolio-Esteban
Overview of the Projects done within my MBA 

# Project 1: AWS Data Analytic Platform Part 1

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

Tools and Technologies

    AWS S3: For scalable storage of raw and cleaned datasets.
    AWS Glue: For data cleaning, transformation, and ETL pipeline creation.
    AWS Glue DataBrew: For data profiling and initial cleaning.
    AWS Athena: For querying and analyzing data with SQL.

Deliverables

A Data Analytic Platform supporting:

    Descriptive analysis (e.g., identifying most common permit categories).
    Exploratory analysis (e.g., understanding patterns by permit type and category).
    A cost analysis showing a monthly AWS expense of approximately $8.57.

Key Insights

    The platform effectively handles data ingestion, profiling, cleaning, and transformation.
    Downtown Vancouver's most common permits in 2024 are categorized under [insert key insight here, e.g., "Commercial Use"].
    The platform demonstrates scalability and cost-efficiency, with potential for further enhancements in performance and sustainability.
