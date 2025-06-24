Descriptive Analysis of Issued Operating Permits – Water Systems (Downtown Vancouver)
Project Objective
This project focuses on analyzing the "Issued Operating Permits – Water Systems" dataset for Downtown Vancouver. The objective is to uncover patterns in water system permits and water quality indicators over time, in order to inform better management and maintenance practices for urban water systems. By examining trends in permit renewals, system types, operational status, and water quality metrics (such as temperature and turbidity), the analysis aims to improve urban water system safety and efficiency
file-ydc3qc32tqpvvjo9ebvx7u
. Insights from this descriptive analysis will help identify potential gaps in policy enforcement, technology, and processes, ultimately guiding recommendations for safer and more compliant water systems.
Dataset Description
The dataset was obtained from the City of Vancouver Open Data Portal and contains 594 records filtered to the Downtown area
file-ydc3qc32tqpvvjo9ebvx7u
. Each record represents a permitted water system and includes detailed attributes such as:
Permit ID: Unique identifier for the operating permit of a water system.
System Type: The type of mechanical water system (e.g., Cooling Tower, Decorative Water Feature, or Building Water Treatment System)
file-ydc3qc32tqpvvjo9ebvx7u
.
Status: Operational status of the system, indicating whether it is Active or Inactive
file-ydc3qc32tqpvvjo9ebvx7u
.
Average Temperature: The average water temperature recorded for the system (a water quality indicator).
Average Turbidity: The average turbidity (water clarity) level of the system, another key water quality metric.
Permit Renewal Date: The date when the permit was issued or last renewed (used to track temporal trends and seasonality).
Voluntary Participation: A flag indicating if the system is part of a voluntary compliance or monitoring program
file-ydc3qc32tqpvvjo9ebvx7u
.
Marker Color: A categorical marker used for mapping the system on city maps (e.g., color-coding different types or statuses).
This dataset is highly relevant for analyzing patterns in permit issuance, the types of water systems in operation, and their maintenance practices over time
file-ydc3qc32tqpvvjo9ebvx7u
. In particular, it provides a basis for examining how water quality parameters fluctuate throughout the year and how active vs. inactive systems are distributed in the downtown core.
Methodology
The analysis followed a structured data analytics methodology, leveraging AWS cloud tools for data handling and analysis. The workflow included data collection, preparation, statistical analysis, visualization, segmentation, and interpretation of insights, as outlined below.
1. Data Collection and Preparation
Data Ingestion: The project began with defining the business questions and goals, then setting up a data storage solution. A dedicated Amazon S3 bucket was created with a folder (e.g., "WaterSystemPermits") to store the raw dataset
file-ydc3qc32tqpvvjo9ebvx7u
. Prior to ingestion, a root-cause analysis (using a Fishbone diagram) was conducted to understand factors affecting permit management – including Policy (e.g., inconsistent enforcement of renewals), Technology (lack of real-time monitoring systems), Process (manual or delayed renewals), and People (limited inspection staff)
file-ydc3qc32tqpvvjo9ebvx7u
file-ydc3qc32tqpvvjo9ebvx7u
. This context informed the data requirements and quality checks.
Data Profiling: Using AWS Glue DataBrew, a data profiling job was run on the S3 data to assess data quality and structure. A Glue DataBrew dataset was created for Vancouver Water System Permits and a profiling job executed to detect any anomalies or missing values
file-ydc3qc32tqpvvjo9ebvx7u
. The profiling results indicated no critical data issues – the dataset was clean, well-structured, and ready for analysis
file-ydc3qc32tqpvvjo9ebvx7u
. This step ensured confidence in the accuracy of subsequent analysis.
Data Cleaning: Although the profiling showed the data was largely clean, an additional cleaning step was performed to address any minor inconsistencies (from system-generated entries or manual data entry). A data cleaning workflow was first designed using draw.io and Excel to map out necessary transformations (e.g. standardizing formats, handling any outliers)
file-ydc3qc32tqpvvjo9ebvx7u
. Then, an AWS Glue DataBrew project was implemented to apply these cleaning operations. A job (named "Vancouver-WaterSystemPermits-Cleaning-Job") was run to transform and clean the data
file-ydc3qc32tqpvvjo9ebvx7u
. After cleaning, the refined dataset was stored back in S3 as the curated data source for analysis.
Data Cataloging: To enable easy querying, the cleaned data was cataloged in AWS Glue Data Catalog. A new database (e.g., vancouver-waterpermits-catalog) was created, and an AWS Glue crawler was configured to scan the cleaned dataset and create a schema-defined table in the catalog
file-ydc3qc32tqpvvjo9ebvx7u
file-ydc3qc32tqpvvjo9ebvx7u
. This made the data readily accessible via SQL queries in Amazon Athena for the next steps.
2. Descriptive Statistics (Amazon Athena Queries)
With the data prepared and cataloged, Amazon Athena was used to perform descriptive statistical analysis on the dataset. Several SQL queries were written and executed to summarize key aspects of the data
file-ydc3qc32tqpvvjo9ebvx7u
:
Permit Status Counts: A query counted how many water systems are Active vs. Inactive. This revealed the distribution of operational systems versus those that have been taken offline. Understanding the share of inactive systems helps indicate potential compliance issues or seasonal shutdowns that might require follow-up. (For example, if a significant number of systems are inactive, it may signal periods of non-use or decommissioned facilities that still hold permits.)
System Type Distribution: Another query aggregated the number of permits by system type (Cooling Towers, Decorative Water Features, Building Water Treatment Systems). This provided insight into which types of water systems are most common in Downtown Vancouver and allowed further analysis of whether certain system types tend to be inactive more frequently or have different renewal patterns.
Temporal Patterns: Using the permit renewal dates, data was grouped by time (by month and year) to compute average temperature and turbidity over time. This helped identify seasonal or temporal trends in water quality indicators. For instance, monthly averages of water temperature and turbidity were calculated to see how these values change throughout the year.
Summary Statistics: Additional summary metrics were obtained, such as the overall average temperature and turbidity across all records, and the range (min–max) of these values. These statistics establish baseline water quality conditions for the city's systems and highlight any extreme values that might warrant attention.
The use of Athena for these queries made it possible to quickly derive insights from the data stored in S3 without needing to move it, thanks to serverless SQL querying. The results of these queries were saved for reporting and visualization.
3. Data Visualization
To communicate the findings, key data visualizations were generated. Two primary trends were visualized using line graphs:
Monthly Temperature and Turbidity Trends: Using the analytical tools (the Open Data portal’s analysis feature and later refined in Excel), Average Temperature and Average Turbidity were plotted against the timeline of permit renewal dates on a monthly basis
file-ydc3qc32tqpvvjo9ebvx7u
. Figure 1 in the project (an example line chart) illustrates these monthly trends in temperature and turbidity for the permitted water systems in Downtown Vancouver
file-ydc3qc32tqpvvjo9ebvx7u
. This visualization makes it easy to observe how water quality parameters fluctuate over time in relation to the permit cycle.
Summary Trend Graph (Excel): The summary statistics from Athena were also exported and visualized in Excel to create a clear line graph (referenced as Figure 24 in the project)
file-ydc3qc32tqpvvjo9ebvx7u
. This graph reinforced the trends found in the Athena analysis by showing the combined timeline of water quality indicators alongside permit renewals.
By plotting these variables, patterns such as seasonal changes and long-term trends became apparent at a glance. The visual approach helped validate the statistical findings and served as a communication tool for stakeholders. All charts were prepared in a clean, simple format for inclusion in the final report and for presentation to relevant city departments.
4. Segmentation by System Type and Status
The dataset was further segmented to drill down into patterns by category:
By System Type: The records were grouped by the type of water system. This segmentation allowed the analysis to determine if different system types exhibit different behaviors. For example, the number of Cooling Towers vs. Decorative Water Features was compared to see which type is more prevalent in downtown. Additionally, average turbidity and temperature were examined per system type to check if, say, cooling towers tend to run hotter or more turbid than decorative fountains. Such distinctions can point to type-specific maintenance needs or regulatory focus (e.g., cooling towers might need more frequent water treatment due to higher turbidity).
By Status (Active/Inactive): The data was also segmented by operational status. This involved identifying all Inactive systems and analyzing their characteristics (such as which system types they are, and when their last renewal dates were) versus Active systems. This trend analysis of inactive systems is important: for instance, if many decorative water features are inactive during winter months, it might reflect seasonal shutdowns. Or if certain systems remain inactive long-term, it could indicate they were decommissioned or non-compliant. Understanding inactive system trends helps prioritize which permits may need attention (renewals, inspections or closures).
Through segmentation, the analysis could highlight, for example, if certain types of systems are more prone to becoming inactive or if they have consistently different water quality readings. This granularity adds depth to the descriptive analysis, ensuring that insights are actionable for each category of water system.
5. Insights and Findings
Combining the descriptive statistics and visualizations, several key insights emerged from the analysis:
Seasonal Temperature Patterns: The average water temperature in the systems showed a clear seasonal pattern, peaking in winter and dipping by late summer
file-ydc3qc32tqpvvjo9ebvx7u
. This is somewhat counter-intuitive for outdoor water systems (which typically might be warmer in summer), suggesting that many measured systems could be indoor or mechanically heated systems (e.g., building water treatments or heated features) that run hotter in colder months. It highlights the influence of seasonal operations or heating on water systems.
Increasing Turbidity Over Time: Turbidity levels have been gradually rising over the period analyzed
file-ydc3qc32tqpvvjo9ebvx7u
. This upward trend in turbidity (decreasing water clarity) could indicate accumulating sediments or biological growth in systems, or a lapse in regular maintenance. The finding signals a potential deterioration in water quality over time if left unaddressed. It underlines the need for more frequent water treatment or flushing of systems to maintain clarity.
Active vs. Inactive Systems: The analysis of permit status found that a subset of the systems are marked Inactive. These inactive systems could correspond to seasonal shut-offs (such as fountains turned off in winter) or systems that have not renewed permits and are effectively out of operation. This trend is important because a higher number of inactive systems might mean certain facilities are not being used or maintained despite having permits. It raises questions about whether those systems are pending renewal, require inspection, or should be retired from the registry. Tracking inactivity can help the city ensure permits are up to date and identify systems that need attention or follow-up.
Permit Renewal Timing: By looking at the permit renewal dates alongside quality metrics, it was observed that certain dips or spikes in water quality coincided with specific times of the year. For instance, turbidity increases might cluster just before renewal dates, hinting that systems degrade in quality as they approach their renewal/maintenance cycle. This insight suggests that timely permit renewals (and the maintenance usually associated with renewal) are critical – delays in renewal could lead to extended periods of suboptimal water quality.
Overall, these findings emphasize the dynamic nature of water system conditions and the importance of regular oversight. Seasonal changes affect system performance, and continuous monitoring can catch gradual declines (like increasing turbidity) before they become compliance issues. The identification of inactive systems and their patterns provides an opportunity for the city to tighten its permit management process.
6. Recommendations
Based on the above insights, the following recommendations are proposed to improve water system management and permit compliance in Vancouver:
Implement Scheduled Inspections and Maintenance: Establish a more regular inspection schedule for permitted water systems, especially timed around seasonal peaks. For example, since water quality (temperature/turbidity) fluctuates seasonally, performing check-ups and maintenance before the winter peak and during late summer lows could help stabilize conditions. Regular maintenance should address the rising turbidity trend by cleaning tanks, filters, or pipes more frequently.
Integrate Real-Time Monitoring & Alerts: Address the technology gap by deploying digital water quality monitoring sensors for key systems (especially large cooling towers or important public water features). Real-time data on temperature and turbidity can feed into a dashboard, and automatic alerts can be sent if turbidity or temperature exceed safe thresholds. This will enable proactive responses – for instance, if turbidity is trending upward rapidly, maintenance can be scheduled immediately rather than waiting for the next inspection. Moreover, an automated alert for upcoming permit renewal dates (e.g., notifications to system owners and city inspectors) would ensure renewals are not overlooked
file-ydc3qc32tqpvvjo9ebvx7u
file-ydc3qc32tqpvvjo9ebvx7u
.
Enhance Permit Renewal Processes: Simplify and digitize the renewal workflow. An online system that tracks permit status and renewal deadlines could reduce manual delays
file-ydc3qc32tqpvvjo9ebvx7u
. This system should flag permits that are about to expire or those associated with inactive systems, prompting timely action. Streamlining this process addresses the identified process inefficiencies and ensures no permits lapse without review.
Focus on Inactive Systems: Conduct a targeted review of all systems listed as Inactive. Determine whether these are seasonal or permanent, and ensure that inactive systems are either safely decommissioned or brought back into compliance before reactivation. If many inactive systems correspond to a particular type (for example, if Decorative Water Features are largely inactive in winter), tailor the inspection schedule to check these systems before they go active again (spring/summer). Prioritizing inactive or long-uninspected systems for audits will close any gaps in safety oversight.
Policy and Training Updates: In light of the findings, update city policies to enforce consistent standards. For instance, if turbidity is rising citywide, consider stricter regulations on water treatment frequency for permit holders. Also, provide training and resources to personnel (People) – more certified inspectors or better training can help in recognizing issues early and ensuring all systems adhere to best practices
file-ydc3qc32tqpvvjo9ebvx7u
. A well-informed team combined with clear policies will uphold higher water quality standards.
By implementing these recommendations, the City of Vancouver can better ensure that operating permits translate to actual operational safety: water systems will be maintained in a timely manner, water quality will remain within safe parameters, and the administrative process will support (not hinder) proactive maintenance.
Tools and Deliverables
Throughout this project, a variety of AWS cloud services and other tools were used to manage the data and extract insights, with several key deliverables produced:
Tools Used:
Amazon S3: for data storage, serving as a data lake for the raw and cleaned datasets. The S3 bucket organized the input data and outputs (profiles, cleaned data) in a structured manner
file-ydc3qc32tqpvvjo9ebvx7u
.
AWS Glue DataBrew: for data profiling and cleaning. DataBrew’s visual interface was used to run the Profiling Job (to assess data quality) and the Cleaning Job that applied transformations to standardize the dataset
file-ydc3qc32tqpvvjo9ebvx7u
file-ydc3qc32tqpvvjo9ebvx7u
.
AWS Glue Data Catalog: to catalog the cleaned data. The Glue Catalog made the data schema available for querying, enabling Athena to easily access the permits dataset
file-ydc3qc32tqpvvjo9ebvx7u
.
Amazon Athena: for querying and computing descriptive statistics. Athena’s SQL queries were the backbone for summarizing data (counts, averages, trends) directly from S3
file-ydc3qc32tqpvvjo9ebvx7u
.
Microsoft Excel: for additional data visualization and analysis. Excel was used to create the final line graphs (e.g., the combined temperature and turbidity trend chart) and to tabulate summary statistics for the report
file-ydc3qc32tqpvvjo9ebvx7u
.
draw.io and Microsoft Excel (diagrams): for planning and design diagrams. draw.io was used to sketch the data architecture and workflow diagrams (e.g., fishbone diagram for root causes, data lake design) and Excel was sometimes used to layout process flows before implementation
file-ydc3qc32tqpvvjo9ebvx7u
file-ydc3qc32tqpvvjo9ebvx7u
.
Key Deliverables:
Cleaned Dataset: A refined version of the "Issued Operating Permits – Water Systems" dataset, cleaned and stored in S3, ready for analysis. This dataset is also cataloged in Glue for easy access.
Data Profile Report: A summary from the DataBrew profiling job, confirming data quality and highlighting any anomalies (which in this case were minimal).
Athena Query Results: A set of query outputs (in CSV/Excel or saved query forms) summarizing the counts of active/inactive systems, distribution of system types, and monthly averages of temperature and turbidity. These results form the basis of the insights.
Visualizations: Line charts and potentially bar charts generated from the analysis – for example, the monthly temperature and turbidity trend graph
file-ydc3qc32tqpvvjo9ebvx7u
, and any other supporting charts (such as a breakdown of system statuses or types if created). These visuals are prepared for inclusion in reports or presentations.
Project Report: A comprehensive report (such as this document) detailing the analysis process, findings, and recommendations. This report is a professional write-up intended for the project portfolio, demonstrating the use of AWS data analytics services on a real-world dataset.
All the above deliverables are organized and ready to be shared with stakeholders. They showcase the end-to-end journey of the data – from raw data ingestion in the cloud, through cleaning and analysis, to the final actionable insights for the City of Vancouver’s water systems. The project exemplifies how cloud-based data analytics can drive informed decision-making for urban infrastructure management.# Data-analyst
