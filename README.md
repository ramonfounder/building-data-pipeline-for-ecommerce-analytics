**Project:** Building a Data Pipeline for E-commerce Analytics

**Scenario:** You are working for an e-commerce company that wants to analyze customer purchase data to gain insights into buying patterns and optimize inventory management.

#### Steps and Deliverables

**1. Apache Nifi: Data Ingestion Pipeline**
   - **Goal:** Ingest customer purchase data from various sources (CSV files, APIs) and store it in a staging area.
   - **Tasks:**
     - Install Apache Nifi and create a flow to ingest data from a CSV file.
     - Use Nifi processors to clean and transform the data.
     - Store the transformed data in a staging database (PostgreSQL).
   - **Deliverable:** Apache Nifi flow configuration file and a brief report with screenshots and explanations.

**2. Python Programming: Data Transformation and ETL**
   - **Goal:** Use Python to further clean, transform, and prepare the data for analysis.
   - **Tasks:**
     - Write Python scripts to read data from the staging database.
     - Perform data cleaning (handling missing values, data type conversions).
     - Transform the data into a suitable format for analytics and load it into a PostgreSQL analytics database.
   - **Deliverable:** Python scripts and a report detailing the ETL process.

**3. PySpark: Large-Scale Data Processing**
   - **Goal:** Process and analyze large datasets using PySpark.
   - **Tasks:**
     - Set up a PySpark environment.
     - Write PySpark scripts to perform data aggregation (e.g., total sales per product, average purchase value per customer).
     - Save the processed data back into the PostgreSQL analytics database.
   - **Deliverable:** PySpark scripts and a summary of the data processing tasks performed.

**4. PostgreSQL: Database Management and Query Optimization**
   - **Goal:** Manage and optimize the PostgreSQL database for fast query performance.
   - **Tasks:**
     - Set up PostgreSQL databases for staging and analytics.
     - Create tables, indexes, and write queries to retrieve and manipulate data efficiently.
     - Optimize queries for better performance and ensure the database is well-structured.
   - **Deliverable:** SQL scripts and a report detailing the database setup, queries written, and performance optimizations.

**5. DataLake Experience: Cloud Storage and Analysis**
   - **Goal:** Implement a Data Lake to store raw and processed data, enabling advanced analytics.
   - **Tasks:**
     - Create a Data Lake on AWS/Azure/Google Cloud.
     - Ingest raw data into the Data Lake and perform basic operations.
     - Use cloud analytics tools (e.g., AWS Athena, Azure Data Lake Analytics) to query the data.
   - **Deliverable:** A report on the Data Lake setup, data ingestion process, and queries performed.

**6. Cloud Experience: Deploying and Managing Cloud Services**
   - **Goal:** Deploy and manage cloud services to support the data pipeline and analytics platform.
   - **Tasks:**
     - Set up cloud resources (e.g., EC2 instances, S3 buckets on AWS, or equivalent on other platforms).
     - Deploy the PostgreSQL database and Nifi instance on the cloud.
     - Use cloud monitoring and management tools to ensure the system's reliability and performance.
   - **Deliverable:** A summary of the cloud services used, applications deployed, and any challenges faced.

     

#### File: `customer_purchases.csv`

| CustomerID | OrderID | OrderDate  | ProductID | ProductName     | Quantity | Price | Total  |
|------------|---------|------------|-----------|-----------------|----------|-------|--------|
| 1001       | 5001    | 2024-01-01 | 101       | Widget A        | 2        | 20.00 | 40.00  |
| 1002       | 5002    | 2024-01-02 | 102       | Gadget B        | 1        | 35.00 | 35.00  |
| 1001       | 5003    | 2024-01-03 | 103       | Thingamajig C   | 3        | 15.00 | 45.00  |
| 1003       | 5004    | 2024-01-04 | 101       | Widget A        | 1        | 20.00 | 20.00  |
| 1004       | 5005    | 2024-01-05 | 104       | Doohickey D     | 5        | 12.00 | 60.00  |
| 1002       | 5006    | 2024-01-06 | 105       | Contraption E   | 2        | 50.00 | 100.00 |
| 1005       | 5007    | 2024-01-07 | 103       | Thingamajig C   | 1        | 15.00 | 15.00  |
| 1001       | 5008    | 2024-01-08 | 102       | Gadget B        | 4        | 35.00 | 140.00 |
| 1004       | 5009    | 2024-01-09 | 106       | Gizmo F         | 3        | 25.00 | 75.00  |
| 1003       | 5010    | 2024-01-10 | 101       | Widget A        | 2        | 20.00 | 40.00  |

#### Columns Description:
- **CustomerID**: Unique identifier for the customer.
- **OrderID**: Unique identifier for the order.
- **OrderDate**: Date when the order was placed.
- **ProductID**: Unique identifier for the product.
- **ProductName**: Name of the product.
- **Quantity**: Number of units purchased.
- **Price**: Price per unit of the product.
- **Total**: Total cost of the order (Quantity * Price).

### Using the Dataset in the Challenge

**1. Apache Nifi: Data Ingestion Pipeline**
   - Create a flow to ingest `customer_purchases.csv` data.
   - Clean and transform the data (e.g., convert `OrderDate` to a standard format).
   - Store the transformed data in a staging PostgreSQL database.

**2. Python Programming: Data Transformation and ETL**
   - Write Python scripts to read data from the staging database.
   - Perform data cleaning (e.g., handle missing values, ensure data types are consistent).
   - Load the cleaned data into an analytics PostgreSQL database.

**3. PySpark: Large-Scale Data Processing**
   - Set up a PySpark environment.
   - Write PySpark scripts to perform aggregations, such as:
     - Total sales per product.
     - Average purchase value per customer.
   - Save the processed data back into the PostgreSQL analytics database.

**4. PostgreSQL: Database Management and Query Optimization**
   - Set up PostgreSQL databases for staging and analytics.
   - Create tables and write optimized queries to retrieve and manipulate data.
   - Perform query optimization to enhance performance.

**5. DataLake Experience: Cloud Storage and Analysis**
   - Create a Data Lake on a cloud platform (e.g., AWS S3, Azure Data Lake).
   - Ingest raw data from `customer_purchases.csv` into the Data Lake.
   - Perform queries on the Data Lake using cloud analytics tools.

**6. Cloud Experience: Deploying and Managing Cloud Services**
   - Set up cloud resources (e.g., EC2 instances, S3 buckets on AWS).
   - Deploy PostgreSQL and Nifi instances on the cloud.
   - Use cloud monitoring tools to ensure system reliability and performance.

