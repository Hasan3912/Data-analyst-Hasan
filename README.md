<table style="border: none; border-spacing: 0;">
  <tr>
    <td style="vertical-align: top;">
      <img src="https://github.com/Hasan3912/Data-analyst-Hasan/blob/a332c2289f926c20c6e85b62b72d0b6c0c9f8726/photo-012.jpg?raw=true"
           alt="Hasan Ali Ahmed"
           width="200"
           style="display: block; object-fit: cover;">
    </td>
    <td style="vertical-align: top; padding-left: 10px; font-size: 14px; line-height: 1.4;">
      <h2 style="margin: 0 0 6px;">Cloud-Based Data Analytics & AWS Project Portfolio</h2>
      <p style="margin: 0;"><strong>Developed for BUSI 653 – Cloud Computing Technologies</strong></p>
      <p style="margin: 0;">Supervised by <a href="https://www.ucanwest.ca/directory/mahmood-dehkordi">Dr. Mahmood Mortazavi Dehkordi</a></p>
      <p style="margin: 0;">Assistant Professor, Dept. of Marketing, Strategy & Entrepreneurship</p>
      <p style="margin: 0;">Created by <a href="https://www.linkedin.com/in/hasanaliahmed3912/">Hasan Ali Ahmed</a> | MBA UCW</p>
    </td>
  </tr>
</table>
# About This Portfolio

This portfolio presents a complete collection of AWS cloud-based projects and weekly implementations completed as part of a 10-week course at University Canada West. It covers end-to-end data engineering concepts including:

- Data Ingestion  
- Data Cleaning  
- Data Summarization  
- Data Analysis  
- Data Enrichment  
- Data Security  
- Data Governance  
- Data Observability  

All tasks were performed using core AWS modules such as **Amazon S3**, **AWS Glue**, **AWS DataBrew**, **Amazon Athena**, and **Amazon EC2**—demonstrating real-world cloud architecture, ETL pipelines, and analytics workflows.

The final project was delivered in two parts and focused on analyzing **urban water system performance** using open data from the **City of Vancouver**. The dataset titled **"Issued Operating Permits – Water Systems"** included 594 records filtered for the Downtown area, detailing system types like cooling towers and water treatment units.

We used AWS tools to process and visualize trends in:

- **Average Temperature**  
- **Average Turbidity**  

plotted over **Permit Renewal Dates** to evaluate changes in water quality and maintenance practices.

This portfolio reflects practical experience in designing cloud infrastructure and executing data workflows using AWS technologies




## Portfolio Contents
| Module     | Focus Area                   | Key Deliverables                                     |
|------------|------------------------------|------------------------------------------------------|
| Week 2     | AWS Infrastructure & Architecture | Design: VPC, EC2, Architecture Diagram, Fishbone Diagram <br> Implementation: Raw Dataset Folder Structure |
| Week 3     | Data Ingestion & Cleaning    | Design: Cleaning Plan (Excel), Cost Estimation Model <br> Implementation: AWS Glue Job Execution, Screenshots |
| Week 4     | Profiling & ETL Pipeline     | Design: ETL Workflow, Partition Strategy <br> Implementation: DataBrew Profiling, Transformed Dataset in S3 |
| Project 1  | Water System Compliance Analysis | Athena Analysis, Trend Graphs, Visualized Dashboard  |
| Project 2  | Budget Forecasting System    | Financial ETL Pipeline, Excel Forecasting Model, Final Report |


## Technical Skills Demonstrated
- **Cloud Infrastructure**: Amazon EC2, S3, VPC
- **ETL & Data Transformation**: AWS Glue
- **Data Profiling & Cleaning**: AWS DataBrew, Excel
- **Querying & Analysis**: Amazon Athena, SQL
- **Visualization**: Excel Dashboards, draw.io Diagrams
- **Cost Evaluation**: S3 Tiering, Compute Pricing

---

## 🗕️ Weekly Breakdown

### Week 2: Infrastructure Design & Problem Definition

### Project Description:
This week focused on establishing the foundational architecture for conducting descriptive analytics on customer purchase data from UCW’s Finance Department. The emphasis was on understanding business questions, analyzing operational datasets, and preparing a secure and scalable environment for data ingestion and analytics.

### Objective:
To analyze the business question provided by the finance department, identify relevant datasets and metadata, and create a cloud-based data lake (AWS S3) with a structured folder and tagging system to support future data ingestion and transformation processes.


### Data set Used:
This project utilized simulated transaction-like datasets from the UCW Finance Department. Each file represents a key academic or administrative process.

| File Name           | Format | Description                                  |
|---------------------|--------|----------------------------------------------|
| Course Registration | CSV    | Records of student course enrollments       |
| Course Scheduling   | CSV    | Course and timetable scheduling data        |
| Server Log          | CSV    | System/server access records                 |
| Staff Tasks         | CSV    | Task assignments and completions for staff  |
| Student Feedback    | CSV    | Collected feedback entries from students     |
| Student Holds       | CSV    | Administrative holds placed on students      |
| Support Tickets     | CSV    | Help desk and student service ticket records |


**Design**
- System architecture diagram linking UCW to AWS
- VPC configuration with `Finance-VPC-has` and security group `Finance-SG-has`
- Fishbone diagram analyzing cash flow bottlenecks
- **Visual Preview**
![Finance Architecture Diagram](https://raw.githubusercontent.com/Hasan3912/Data-analyst-Hasan/6e6d3f194963deb4f3c8ff1e89034092eb6ed61a/Finance%20Data%20Lake%20Design%20-%20Hasan-CC%20Solution%20%232.jpg)  
*Figure 1: Finance Data Lake Design*

**Implementation**
- Launched EC2 instance using `t3.micro`
- Created `finance-raw-bim` S3 bucket
- Uploaded raw datasets and structured folders by type/frequency
- ![Week 2 Implementation Screenshot](https://raw.githubusercontent.com/Hasan3912/Data-analyst-Hasan/6e6d3f194963deb4f3c8ff1e89034092eb6ed61a/Implementation%20w2.png)  
*Figure 2: S3 Folder Setup and Raw Zone Creation*

---

### Week 3: Data Ingestion & Cleaning Pipeline

### Project Description:
This phase involved preparing the raw customer purchase data for descriptive analysis. Tasks included designing a cleaning strategy, evaluating storage and processing costs, and implementing the ingestion and transformation pipeline using AWS Glue and S3.

### Objective:
To implement a structured data ingestion process for customer transaction data, perform cleaning operations such as handling null values and standardizing formats, and estimate costs of storing and managing the data within AWS—ensuring the datasets are analytics-ready for further processing in Week 4.


**Design**
- Cleaning strategy in Excel: null handling, format standardization, deduplication plan
- Cost estimation using AWS Pricing Calculator and S3 Storage Lens
- ![Data Cleaning Job](https://github.com/Hasan3912/Data-analyst-Hasan/blob/4b2eadd172304b3d7de58b30c38954962314618f/_DAP%20-%20Week%203%20-%20Data%20Cleaning.jpg?raw=true)
- *Figure 3: AWS Glue Data Cleaning Job Screenshot*


- **Implementation**
- Uploaded datasets to S3
- Created AWS Glue jobs for transformation
- Captured screenshots of AWS Glue execution and pricing breakdowns
- ![Cost Evaluation](https://github.com/Hasan3912/Data-analyst-Hasan/blob/4b2eadd172304b3d7de58b30c38954962314618f/Cost%20Evaluation%20of%20Dataset%20Ingestion%20.png?raw=true)
-  *Figure 4: AWS S3 Cost Estimation Using Pricing Calculator*



### Week 4: Profiling & ETL Implementation

### Project Description:
This week focused on profiling and transforming datasets from the UCW Finance Department using AWS Glue DataBrew. The goal was to prepare clean, analytics-ready outputs in both user-friendly and system-optimized formats using proper compression and partitioning.

### Objective:
To conduct column-wise profiling, apply cleaning operations, and generate dual outputs:
- CSV for user-readable reports
- Parquet + Snappy for efficient system storage and querying

---

### Design
- Created new S3 folder structure under `/cleaning/user/` and `/cleaning/system/`
- Selected key columns (e.g., platform, failure_reason) for partitioning strategy
- Planned two output pipelines:
  - CSV → for business users  
  - Parquet (Snappy + partitioned) → for system use

![ETL System Architecture](https://github.com/Hasan3912/Data-analyst-Hasan/blob/aea3ce73d90f335b97512398926e23c30762f3dc/Finance%20-%20DAP%20-%20Week%204%20-%20ETL%20%20Design%20-%20Hasan-CC%20Solution%20%234.jpg)  
*Figure 5: Week 4 ETL Design Architecture for Finance Data Lake*

---

### Implementation
- Built Glue DataBrew projects for each dataset
- Performed profiling to check for:
  - Missing values
  - Data type mismatches
  - Formatting issues
- Applied column-wise transformations and rules
- Generated:
  - `User Outputs` → CSV files  
  - `System Outputs` → Partitioned Parquet files with compression
- Verified outputs and partition structure in S3

![ETL Workflow in AWS Glue](https://github.com/Hasan3912/Data-analyst-Hasan/blob/aea3ce73d90f335b97512398926e23c30762f3dc/week4.png)  
*Figure 6: ETL Pipeline Workflow Using AWS Glue Studio*

---
# Project par 1 AWS Data Analytic Platform – Water Systems (Downtown Vancouver)

## Project Overview

This project is part of the “AWS Data Analytic Platform for The City of Vancouver – Phase 1” initiative. My individual work focused on conducting a full descriptive analysis and AWS cloud-based pipeline for a dataset titled “Issued Operating Permits – Water Systems”, filtered for the Downtown Vancouver region. The objective was to analyze patterns related to permit issuance, system status, water quality, and support decision-making with insights from structured analytics.

## Dataset Summary

| Column Name              | Data Type | Missing Values | Unique Values | Example Value   |
|--------------------------|-----------|----------------|----------------|-----------------|
| permit_id                | object    | 0              | 100            | PID1000         |
| system_type              | object    | 0              | 3              | Cooling Tower   |
| status                   | object    | 0              | 2              | Inactive        |
| voluntary_participation | object    | 0              | 2              | No              |
| marker_color             | object    | 0              | 4              | Green           |

## Implementation Phases

### Phase 1: Data Ingestion and Planning
- Defined the business problem and root causes using a Fishbone Diagram
- Identified policy, technology, process, and human gaps
- Designed the Data Lake structure using Excel and draw.io
- Created an S3 bucket (vancouver-raw-men) with a subfolder (WaterSystemPermits)

### Phase 2: Data Profiling
- Created the dataset: Vancouver-WaterSystemPermits-Dst-Has
- Executed profiling job: Vancouver-WaterSystemPermits-Profiling-Job-Has
- Verified schema, checked for missing values and anomalies (no critical issues found)

### Phase 3: Data Cleaning
- Designed cleaning workflow using Excel and draw.io
- Used AWS Glue DataBrew to implement the cleaning process
- Created job: Vancouver-WaterSystemPermits-Cleaning-Job-Men
- Addressed inconsistencies from both system-generated and user-input data

### Phase 4: Data Cataloging
- Designed ETL architecture and flowcharts
- Created database: vancouver-waterpermits-catalog-men
- Ran crawler on cleaned dataset to populate catalog with structured table

### Phase 5: Data Enrichment and Summarization
- Used Amazon Athena for querying enriched data
- Analyzed trends in temperature and turbidity
- Counted active vs. inactive systems
- Created Excel-based line graphs to visualize findings

## Key Findings

- Water temperature followed a seasonal trend, with peaks in winter and dips in summer
- Turbidity levels increased steadily, indicating potential degradation of water clarity
- Emphasized need for timely inspections and permit renewals to maintain water safety standards

---

## Tools and Technologies

| Category              | Tool or Platform           |
|-----------------------|----------------------------|
| Cloud Infrastructure  | AWS S3, EC2, EBS           |
| Data Wrangling        | AWS Glue DataBrew          |
| Querying              | Amazon Athena              |
| Profiling             | AWS Glue Jobs              |
| Visualization         | Excel (line graphs)        |
| Diagramming           | draw.io, Excel             |

---

## Deliverables

- PDF report summarizing analysis and implementation
- Excel charts for temperature and turbidity
- Screenshots from AWS components (S3, Athena, DataBrew)
- Folder structure and pipeline diagrams
- GitHub repository with project code and documentation

---

## Notes

This project demonstrates a real-world approach to designing and executing a data analytics platform using AWS services. It contributes to urban water system safety through data-driven insights and scalable cloud architecture.

---

GitHub Link: [Insert your repository URL here]
