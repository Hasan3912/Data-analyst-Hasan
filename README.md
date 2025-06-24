💧 Descriptive Analysis of Issued Operating Permits – Water Systems (Downtown Vancouver)
📌 Project Overview
This project analyzes the "Issued Operating Permits – Water Systems" dataset from the City of Vancouver's Open Data Portal, focusing specifically on Downtown Vancouver. The goal is to uncover temporal trends in water system permits and water quality indicators—such as temperature and turbidity—to enhance permit compliance, maintenance strategies, and overall urban water safety.

🎯 Objectives
Identify patterns in permit issuance, system activity, and system types.

Detect trends in water quality indicators like turbidity and temperature.

Provide actionable recommendations to improve monitoring and policy enforcement.

🧰 Tools & Technologies
Tool	Purpose
Amazon S3	Data storage and organization
AWS Glue DataBrew	Data profiling and cleaning
AWS Glue Catalog	Data schema creation and cataloging
Amazon Athena	SQL querying and descriptive statistics
Microsoft Excel	Visualizations and trend analysis
draw.io	Workflow and root-cause diagrams

🗂️ Dataset Description
Source: City of Vancouver Open Data Portal
Records: 594 (Filtered to Downtown Vancouver)

Key Features:

Permit ID: Unique permit identifier

System Type: Cooling Tower, Decorative Water Feature, etc.

Status: Active or Inactive

Average Temperature: Water temperature (°C)

Average Turbidity: Water clarity (NTU)

Permit Renewal Date: Date of last renewal

Voluntary Participation: Compliance flag

Marker Color: Map visualization tag

🔍 Methodology
1. Data Ingestion & Profiling
Raw data uploaded to Amazon S3.

Profiling done via AWS Glue DataBrew to ensure quality.

Minor inconsistencies corrected via custom cleaning job.

2. Data Cataloging
Cleaned dataset cataloged with AWS Glue Crawler.

Enabled SQL-based analysis with Amazon Athena.

3. Analysis & Querying (Athena)
Permit Status Distribution (Active vs. Inactive)

System Type Breakdown (e.g., Cooling Towers most common)

Monthly Trends of temperature & turbidity

Summary Stats for all water systems

4. Visualizations
📈 Line Graphs for monthly temperature and turbidity

📊 Excel dashboards to reinforce Athena trends

Category-specific analysis by system type and status

5. Segmentation
By System Type: Compared Cooling Towers vs. Decorative Features

By Status: Explored differences between Active and Inactive systems

📌 Key Insights
🔄 Seasonal Trends: Water temp peaks in winter (heated systems?)

⚠️ Rising Turbidity: Suggests possible neglect or lack of treatment

💤 Inactive Systems: May reflect seasonal shutdowns or decommissioning

🕒 Permit Renewal Delays: Correlated with declines in water quality

✅ Recommendations
Schedule seasonal maintenance & inspections (esp. pre-winter/summer).

Implement real-time water quality monitoring sensors.

Digitize and automate permit renewal reminders.

Review and audit Inactive systems for compliance.

Update policies and inspector training to address rising turbidity.

📦 Deliverables
✅ Cleaned Dataset (S3 + Glue Catalog)

📊 Athena Query Outputs (CSV & SQL scripts)

📈 Graphs: Temperature & Turbidity Over Time

📄 Project Report (Detailed insights & recommendations)

📁 Root Cause Diagrams (Fishbone, workflows)

🔗 Related Projects
Explore more cloud-based analytics:

Project 1: AWS Analysis Pipelines

Project 2: (Insert Future Project)

🚀 Author
Hasan Ali Ahmed
MBA Candidate | Data Analyst | AWS Enthusiast
📫 hasanaliahmmed3912@gmail.com

