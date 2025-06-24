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
| Week 2     | AWS Infrastructure & Architecture | VPC, EC2, Architecture Diagram, Fishbone Diagram, Raw Dataset |
| Week 3     | Data Ingestion & Cleaning    | Cleaning Plan (Excel), AWS Glue Job, Cost Evaluation |
| Week 4     | Profiling & ETL Pipeline     | DataBrew Profiling, ETL Workflow, Transformed Dataset |
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
**Key Achievements**
- Created `Finance-VPC-Men` and secured it with `Finance-SG-Men`
- Launched a public EC2 instance using `t3.micro`
- Designed system architecture linking UCW to AWS
- Built a Fishbone diagram to diagnose cash flow issues
- Organized datasets in `finance-raw-bim` S3 bucket

**Problem Focus**
> Improve the accuracy of departmental budget forecasts by leveraging historical financial data and addressing barriers like outdated tools and miscommunication.

**Visual Preview**
- Week 2 Architecture Diagram (draw.io)

### Week 3: Data Ingestion & Cleaning Pipeline
**Key Achievements**
- Evaluated ingestion and storage costs on AWS S3
- Created a detailed cleaning plan (null handling, standardization, deduplication)
- Implemented data transformation using AWS Glue

**Visual Preview**
- Week 3 Cleaning Job Screenshot

### Week 4: Profiling & ETL Implementation
**Key Achievements**
- Conducted profiling jobs with AWS Glue DataBrew
- Designed ETL pipeline: Extract (S3) → Transform (Glue) → Load (Curated S3)
- Deployed and validated the ETL flow

**Visual Preview**
- Week 4 ETL Pipeline Diagram

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
│   ├── architecture_diagram.drawio
│   ├── fishbone_diagram.drawio
│   └── finance-raw-bim/
├── week3
│   ├── cleaning_plan.xlsx
│   ├── glue_job_screenshot.png
│   └── cost_evaluation.pdf
├── week4
│   ├── profiling_report.png
│   ├── etl_pipeline_diagram.drawio
│   └── transformed_dataset/
└── reports
    ├── Week2_Report.pdf
    ├── Week3_Report.pdf
    └── Week4_Report.pdf
```

---

## 👤 Author
**Hasan Ali Ahmed**  
MBA Candidate | Cloud & Data Analytics Enthusiast  
📍 British Columbia, Canada  
📧 hasanaliahmmed3912@gmail.com

---

## 📁 Appendix
- 📄 Week 2 Report (PDF)
- 📄 Week 3 Report (PDF)
- 📄 Week 4 Report (PDF)
