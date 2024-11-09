# DELAYED-OIL-TRANSFER-PROJECTS

### PROJECT OVERVIEW

### Objectives
This project investigates the root causes of delays in the oil transfer process and proposes a strategic solution plan. Through data analysis of operational workflows, resource allocation, and process efficiency, this project seeks to identify trends and key areas for improvement.

### Scope
The analysis covers:
- Current transfer and handling protocols
- Staffing and equipment utilization patterns
- Service delay patterns and external influencing factors
- Operational bottlenecks and improvement opportunities

### Methodology
- Data Collection: Gathering logs, staffing data, equipment status, and service records.
- Analysis: Identifying delay trends and correlating with operational factors.
- Root Cause Analysis: Diagnosing main delay contributors.
- Solution Proposal: Recommending solutions, such as process optimization and resource allocation.

### DATA SOURCE
Data set provided by the client as a CSV file, which was downloaded and processed for analysis.

### Tools
1. Microsoft Excel: Utilized for preliminary data correction and initial review of the dataset.
2. SQL Server: Employed for data cleaning and in-depth analysis to extract meaningful insights.
3. Power BI: Used to visualize insights and provide detailed, interactive reports.

### EXPLORATORY DATA ANALYSIS (EDA)
In this EDA phase, we will examine the human resource dataset to address key operational questions that can impact the efficiency and reliability of oil transfer services. These insights will help identify potential areas for improvement and facilitate data-driven decision-making.

### Key Questions to Address:
1. **Total Number of Truck Drivers:**
   Determine the number of truck drivers to assess if current staffing meets operational demands.
2. **Number of Efficient Trucks:**
   Identify the count of trucks classified as efficient to understand fleet reliability and potential operational constraints.
3. **Coverage Areas (Distances in Kilometers):**
   Analyze distances covered to evaluate the geographic reach and the adequacy of logistical support across areas served.
4. **Truck Breakdown and Maintenance Frequency:**
   Assess the frequency of truck breakdowns and scheduled maintenance to pinpoint areas needing additional support or preventive measures.

### USED USED SQL CODES(In case you are working with only Excel, always include your formulas)
```SELECT COUNT(*) AS TotalTruckDrivers
FROM employees
WHERE job_title = 'Truck Driver';
SELECT COUNT(*) AS EfficientTrucks FROM trucks WHERE efficiency_status = 'Efficient';
SELECT truck_id, SUM(distance_in_km) AS TotalDistanceCovered FROM deliveries GROUP BY truck_id;
SELECT truck_id, COUNT(*) AS BreakdownCount FROM maintenance_log WHERE maintenance_type = 'Breakdown' GROUP BY truck_id.


### REPORT
![dashboard](https://github.com/user-attachments/assets/707f5ab8-511b-4364-93a8-5cad5cc91f61)

### RECOMMENDATIONS
Based on the Exploratory Data Analysi(EDA) and insights derived from the SQL queries, here are some recommendations to improve the efficiency and reliability of the oil transfer service:
1. **Optimize Workforce Allocation:**
   Recommendation: Based on the total number of truck drivers, assess if the current workforce is sufficient to meet demand, especially during peak periods. If there are shortages,          consider hiring additional drivers or redistributing work hours to avoid delays.
2. **Actionable Steps:**
   Evaluate whether the number of drivers matches the number of trucks and expected delivery volumes.


