# Cloud-Based Data Analytics & AWS Project Portfolio

**Developed as part of BUSI 653 – Cloud Computing Technologies at University Canada West**  
**Hasan Ali Ahmed | MBA, Spring 2025 Cohort**

---

## About This Portfolio
This portfolio presents a complete collection of AWS cloud-based projects and weekly implementations focused on infrastructure setup, data cleaning, profiling, and ETL automation. Each segment showcases real-world cloud solutions that address problems in financial forecasting and urban water system management.

These projects are designed to demonstrate applied technical skills, data-driven problem solving, and modern infrastructure planning using Amazon Web Services (AWS).

---

## Portfolio Contents
| Module     | Focus Area                   | Key Deliverables                                     |
|------------|------------------------------|------------------------------------------------------|
| Week 2     | AWS Infrastructure & Architecture | Design: VPC, EC2, Architecture Diagram, Fishbone Diagram <br> Implementation: Raw Dataset Folder Structure |
| Week 3     | Data Ingestion & Cleaning    | Design: Cleaning Plan (Excel), Cost Estimation Model <br> Implementation: AWS Glue Job Execution, Screenshots |
| Week 4     | Profiling & ETL Pipeline     | Design: ETL Workflow, Partition Strategy <br> Implementation: DataBrew Profiling, Transformed Dataset in S3 |
| Project 1  | Water System Compliance Analysis | Athena Analysis, Trend Graphs, Visualized Dashboard  |
| Project 2  | Budget Forecasting System    | Financial ETL Pipeline, Excel Forecasting Model, Final Report |

---

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

**Design**
- System architecture diagram linking UCW to AWS
- VPC configuration with `Finance-VPC-Men` and security group `Finance-SG-Men`
- Fishbone diagram analyzing cash flow bottlenecks

**Implementation**
- Launched EC2 instance using `t3.micro`
- Created `finance-raw-bim` S3 bucket
- Uploaded raw datasets and structured folders by type/frequency

**Visual Preview**
[Image Alt](https://github.com/Hasan3912/Data-analyst-Hasan/blob/054d5c9d5c56162a85763d84f79b92978266d8a1/Finance%20Data%20Lake%20Design%20-%20Hasan-CC%20Solution%20%232.jpg)
*Figure 1: Finance Data Lake Design*

![Week 2 Implementation Screenshot](week2/images/Implementation%20w2.png)  
*Figure 2: S3 Folder Setup and Raw Zone Creation*

---

### Week 3: Data Ingestion & Cleaning Pipeline

**Design**
- Cleaning strategy in Excel: null handling, format standardization, deduplication plan
- Cost estimation using AWS Pricing Calculator and S3 Storage Lens

**Implementation**
- Uploaded datasets to S3
- Created AWS Glue jobs for transformation
- Captured screenshots of AWS Glue execution and pricing breakdowns

**Visual Preview**
*Screenshots to be added in `/week3/images/` folder*

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
