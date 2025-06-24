# 💧 Descriptive Analysis of Issued Operating Permits – Water Systems (Downtown Vancouver)

## 📌 Project Overview  
This project analyzes the **"Issued Operating Permits – Water Systems"** dataset from the City of Vancouver's Open Data Portal, focusing specifically on Downtown Vancouver.  
The goal is to uncover temporal trends in water system permits and water quality indicators—such as **temperature** and **turbidity**—to enhance **permit compliance**, **maintenance strategies**, and overall **urban water safety**.

---

## 🎯 Objectives

- Identify patterns in **permit issuance**, **system activity**, and **system types**.
- Detect trends in water quality indicators like **turbidity** and **temperature**.
- Provide actionable recommendations to improve monitoring and policy enforcement.

---

## 🧰 Tools & Technologies

| Tool                | Purpose                                              |
|---------------------|------------------------------------------------------|
| Amazon S3           | Data storage and organization                        |
| AWS Glue DataBrew   | Data profiling and cleaning                          |
| AWS Glue Catalog    | Data schema creation and cataloging                  |
| Amazon Athena       | SQL querying and descriptive statistics              |
| Microsoft Excel     | Visualizations and trend analysis                    |
| draw.io             | Workflow and root-cause diagrams                     |

---

## 🗂️ Dataset Description

**Source**: City of Vancouver Open Data Portal  
**Records**: 594 (Filtered to Downtown Vancouver)

**Key Features:**

- `Permit ID`: Unique identifier  
- `System Type`: Cooling Tower, Decorative Water Feature, etc.  
- `Status`: Active or Inactive  
- `Average Temperature`: Water temperature (°C)  
- `Average Turbidity`: Water clarity (NTU)  
- `Permit Renewal Date`: Last renewal date  
- `Voluntary Participation`: Compliance flag  
- `Marker Color`: Visualization category

---

## 🔍 Methodology

### 1. Data Ingestion & Profiling
- Uploaded raw data to **Amazon S3**
- Used **AWS Glue DataBrew** for profiling and quality checks
- Minor transformations applied in DataBrew to clean the dataset

### 2. Cataloging & Querying
- Created catalog in **AWS Glue**
- Queried data with **Amazon Athena** to:
  - Count active vs. inactive systems
  - Analyze system types
  - Observe monthly changes in turbidity & temperature

### 3. Visualization
- Created **line graphs** in Excel for trends
- Used **Athena exports** for dashboarding
- Designed **fishbone diagram** (draw.io) to visualize root causes

---

## 📊 Key Insights

- 🌡️ **Water Temperature** peaks in winter — likely due to indoor or heated systems  
- 🌫️ **Turbidity levels** are rising over time — possibly due to infrequent maintenance  
- ❄️ **Inactive Systems** might relate to seasonal shutdowns  
- 🕒 **Permit Renewals** often coincide with drops in water quality

---

## ✅ Recommendations

- Implement **scheduled maintenance** based on seasonal trends  
- Deploy **real-time water monitoring sensors**  
- Streamline **permit renewal** with digital reminders  
- Review and audit **inactive systems**  
- Update city **policies and inspector training**

---

## 📦 Deliverables

- 🧹 Cleaned Dataset (AWS S3 + Glue Catalog)
- 🗃️ Athena SQL Query Outputs
- 📈 Visual Charts (Temp & Turbidity)
- 📄 Project Report (Insights + Recommendations)
- 🧠 Diagrams (Fishbone, Pipeline Design)

---

## 👤 Author

**Hasan Ali Ahmed**  
_MBA Candidate | Data Analyst | AWS Enthusiast_  
📧 [hasanaliahmmed3912@gmail.com](mailto:hasanaliahmmed3912@gmail.com)

---

## 🔗 Related Projects

- [AWS Analysis Pipelines Project](#)
- [Gigsup Career Platform Insights](#)
