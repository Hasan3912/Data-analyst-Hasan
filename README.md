# Cloud-Based Data Analytics & AWS Project Portfolio

**Developed as part of BUSI 653 – Cloud Computing Technologies**  
**Supervised by [Dr. Mahmood Mortazavi Dehkordi](https://www.ucanwest.ca/directory/mahmood-dehkordi)**
Assistant Professor, Department of Marketing, Strategy & Entrepreneurship  
**Hasan Ali Ahmed | MBA, Spring 2025 Cohort**
---

## About This Portfolio
This portfolio presents a complete collection of AWS cloud-based projects and weekly implementations focused on infrastructure setup, data cleaning, profiling, and ETL automation. Each segment showcases real-world cloud solutions that address problems in financial forecasting and urban water system management.

These projects are designed to demonstrate applied technical skills, data-driven problem solving, and modern infrastructure planning using Amazon Web Services (AWS).


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

## 🧽 Project Overview
This repository documents the development of a cloud-based financial data system built during Weeks 2–4 of BUSI 653: Cloud Computing Technologies.  
It demonstrates applied cloud skills in data storage, profiling, transformation, cost optimization, and process visualization.

---

## 🗕️ Weekly Breakdown


### Week 2: Infrastructure Design & Problem Definition

### Project Description:
This week focused on establishing the foundational architecture for conducting descriptive analytics on customer purchase data from XYZ Retail (simulated as UCW’s Finance Department). The emphasis was on understanding business questions, analyzing operational datasets, and preparing a secure and scalable environment for data ingestion and analytics.

### Objective:
To analyze the business question provided by the finance department, identify relevant datasets and metadata, and create a cloud-based data lake (AWS S3) with a structured folder and tagging system to support future data ingestion and transformation processes.


## Dataset
Transactional data spanning one year from XYZ Retail, including:
- **Transaction ID** – Unique identifier for each purchase  
- **Customer ID** – Unique customer number  
- **Purchase Date** – Date and time of each transaction  
- **Product Category** – Category such as electronics, clothing, groceries  
- **Quantity** – Number of items purchased  
- **Price** – Total value of the transaction  
- **Payment Method** – Credit card, cash, or digital  
- **Location** – Store location of the transaction  

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


---

### Week 4: Profiling & ETL Implementation

**Design**
- ETL Workflow: Extract (S3) → Transform (Glue) → Load (Curated S3)
- Data partition strategy by categorical field (e.g., platform, failure reason)

**Implementation**
- Conducted profiling with AWS DataBrew
- Created user-friendly (CSV) and system-friendly (Parquet + Snappy) outputs
- Validated folder output and structure in user/system directories

**Visual Preview**
*Screenshots to be added in `/week4/images/` folder*

---

## 🔧 Tool Stack
| Technology      | Description                                |
|----------------|--------------------------------------------|
| Amazon S3      | Data lake for raw and curated datasets     |
| Amazon EC2     | Compute instance for infrastructure testing|
| AWS Glue       | ETL orchestration and transformation        |
| AWS DataBrew   | Profiling and quality inspection            |
| draw.io        | Visual diagrams (Architecture, Fishbone)    |
| Excel          | Cleaning logic, cost models, data previews  |

---

## 📦 Deliverables
- AWS VPC, EC2 setup with documentation
- Cleaned datasets in organized S3 folders
- Data profiling and cost estimates
- Working ETL pipeline in AWS Glue
- Architecture & root cause diagrams
- Weekly project reports (PDF)

---

## 📁 Repository Structure
```bash
/aws-project-portfolio
├── week2
│   ├── images
│   │   ├── Finance Data Lake Design - Hasan-CC Solution #2.jpg
│   │   └── Implementation w2.png
│   ├── architecture_diagram.drawio
│   ├── fishbone_diagram.drawio
│   └── finance-raw-bim/
├── week3
│   ├── images/
│   ├── cleaning_plan.xlsx
│   ├── glue_job_screenshot.png
│   └── cost_evaluation.pdf
├── week4
│   ├── images/
│   ├── profiling_report.png
│   ├── etl_pipeline_diagram.drawio
│   └── transformed_dataset/
└── reports
    ├── Week2_Report.pdf
    ├── Week3_Report.pdf
    └── Week4_Report.pdf
