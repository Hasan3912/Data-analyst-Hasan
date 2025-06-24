# AWS Cloud-Based Finance System (Weeks 2–4 Progress Portfolio)

## Course: BUSI 653 – Cloud Computing Technologies  
University Canada West | Spring 2025  
Instructor: Dr. Mahmood Mortazavi Dehkordi  
Submitted by: Hasan Ali Ahmed (ID: 2239226)

---

## Project Summary

This portfolio outlines the step-by-step development of a cloud-based finance data management system using AWS. The work spans Weeks 2 to 4 and demonstrates infrastructure setup, data profiling, ingestion, transformation, cost evaluation, and ETL implementation.

---

## Week 2 – Architecture & Foundation Setup

### Technical Setup
- Created a Virtual Private Cloud (VPC) named `Finance-VPC-Men`
- Configured a Security Group `Finance-SG-Men`
- Launched a t3.micro EC2 instance with public access
- Documented CLI commands for repeatable infrastructure setup

### Diagrams & Root Cause Analysis
- Designed a system architecture diagram using draw.io to visualize UCW's integration with AWS (EC2, S3, IAM)
- Created a Fishbone (Cause-and-Effect) diagram to explore factors contributing to delayed payments

### Data Management
- Organized and stored three datasets: Historical Budgets, Department Expenses, Revenue Streams
- Used Amazon S3 bucket `finance-raw-bim` for efficient, scalable storage
- Structured folders by update frequency, storage class, and data ownership

### Problem Statement
Focused on improving department budget forecasting using historical data. Identified key issues including outdated software, lack of training, absence of standardized review processes, and poor departmental communication.

---

## Week 3 – Dataset Ingestion & Cleaning

### Cost Evaluation
- Assessed cost implications of ingesting data into AWS S3, considering storage tiering and data transfer frequency

### Cleaning Design
- Defined a dataset cleaning plan in Excel
- Outlined logic for handling missing values, standardizing column formats, and eliminating duplicate records

### Cleaning Implementation
- Implemented cleaning rules using AWS Glue
- Verified transformations and prepared datasets for profiling and analysis

---

## Week 4 – Profiling, ETL, and Implementation

### Profiling Cost Analysis
- Evaluated cost of running profiling jobs on AWS Glue DataBrew

### ETL Design
- Outlined an ETL pipeline:
  - Extract: raw financial data from S3
  - Transform: clean and normalize data using Glue scripts
  - Load: push curated data back into structured S3 folders

### ETL Implementation
- Deployed ETL pipeline using Glue jobs
- Validated the consistency and quality of final outputs

---

## Tools and Technologies

| Tool              | Purpose                                  |
|------------------|-------------------------------------------|
| AWS S3           | Cloud data storage (raw + curated)        |
| AWS EC2          | Virtual server for compute resources       |
| AWS Glue         | ETL scripting and cleaning jobs           |
| AWS DataBrew     | Profiling and data quality checks         |
| draw.io          | Architecture and root cause diagrams      |
| Microsoft Excel  | Cleaning logic design, cost tracking      |

---

## Key Deliverables

- Infrastructure setup (VPC, EC2, S3)
- System architecture and fishbone diagrams
- Cleaned and organized datasets
- Dataset profiling and cost evaluation
- ETL pipeline documentation and execution
- Weekly reports (PDF format)

---

## Author

Hasan Ali Ahmed  
MBA Candidate | AWS Cloud Projects | Business Technology  
Email: hasanaliahmmed3912@gmail.com

---

## Appendix

- [Week 2 Report (PDF)](./Week%202.pdf)  
- [Week 3 Report (PDF)](./Week%203.pdf)  
- [Week 4 Report (PDF)](./week%204.pdf)
