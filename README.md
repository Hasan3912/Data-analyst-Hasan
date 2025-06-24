<h1 align="center">AWS Cloud-Based Finance System</h1>
<p align="center">
  <i>A technical portfolio showcasing data infrastructure, analytics, and ETL automation using AWS.</i>
</p>

---

## 🧭 Project Overview

This repository documents the development of a cloud-based financial data system built during Weeks 2–4 of BUSI 653: Cloud Computing Technologies.  
It demonstrates applied cloud skills in data storage, profiling, transformation, cost optimization, and process visualization.

---

## 📅 Weekly Breakdown

### Week 2: Infrastructure Design & Problem Definition

**Key Achievements**
- Created `Finance-VPC-Men` and secured it with `Finance-SG-Men`
- Launched a public EC2 instance using `t3.micro`
- Designed system architecture linking UCW to AWS
- Built a Fishbone diagram to diagnose cash flow issues
- Organized datasets in `finance-raw-bim` S3 bucket

> **Problem Focus**  
> Improve the accuracy of departmental budget forecasts by leveraging historical financial data and addressing barriers like outdated tools and miscommunication.

**Visual Preview**  
<p align="center">
  <img src="images/week2_architecture.png" width="600" alt="Week 2 Architecture">
</p>

---

### Week 3: Data Ingestion & Cleaning Pipeline

**Key Achievements**
- Evaluated ingestion and storage costs on AWS S3
- Created a detailed cleaning plan (null handling, standardization, deduplication)
- Implemented data transformation using AWS Glue

**Visual Preview**  
<p align="center">
  <img src="images/week3_cleaning_job.png" width="600" alt="Week 3 Cleaning Job">
</p>

---

### Week 4: Profiling & ETL Implementation

**Key Achievements**
- Conducted profiling jobs with AWS Glue DataBrew
- Designed ETL pipeline: Extract (S3) → Transform (Glue) → Load (Curated S3)
- Deployed and validated the ETL flow

**Visual Preview**  
<p align="center">
  <img src="images/week4_etl_pipeline.png" width="600" alt="Week 4 ETL Pipeline">
</p>

---

## 🔧 Tool Stack

| Technology        | Description                                  |
|-------------------|----------------------------------------------|
| **Amazon S3**      | Data lake for raw and curated datasets       |
| **Amazon EC2**     | Compute instance for infrastructure testing  |
| **AWS Glue**       | ETL orchestration and transformation         |
| **AWS DataBrew**   | Profiling and quality inspection             |
| **draw.io**        | Visual diagrams (Architecture, Fishbone)     |
| **Excel**          | Cleaning logic, cost models, data previews   |

---

## 📦 Deliverables

- [x] AWS VPC, EC2 setup with documentation  
- [x] Cleaned datasets in organized S3 folders  
- [x] Data profiling and cost estimates  
- [x] Working ETL pipeline in AWS Glue  
- [x] Architecture & root cause diagrams  
- [x] Weekly project reports (PDF)

---

## 📁 Repository Structure


---

## 👤 Author

**Hasan Ali Ahmed**  
MBA Candidate | Cloud & Data Analytics Enthusiast  
📍 British Columbia, Canada  
📧 hasanaliahmmed3912@gmail.com  

---

## 📑 Appendix

- [📄 Week 2 Report (PDF)](./Week%202.pdf)  
- [📄 Week 3 Report (PDF)](./Week%203.pdf)  
- [📄 Week 4 Report (PDF)](./week%204.pdf)
