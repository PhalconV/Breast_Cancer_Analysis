
# APD 911 Calls Project Report

Title Page
Project Title: Enhancing Emergency Response: An Analysis of 911 Call Trends  

Team Name:
## The Data Detectives

### Project Members: 
- Evalyn Njagi (Analyst)
- Rukayat Tokosi (Analyst)
- Sunday Gabriel (Analyst)
- Toheeb Olaniyi (Project Lead)
- AbdulMuiz Akorede (Data Visualizer)
- Augustine Adams (Analyst)
- Olabisi Famoroti (Project Secretary)
- AbdulRasheed Aminu (Analyst)

  
Duration: 28/10/2024 -  (3 Weeks)

### Executive Summary  
Evalyn Summary Suggestion:
Over the years, incident-related issues have risen significantly, leading to an increase in 911 calls. This has necessitated a shift in strategy, ensuring officers are dispatched only to incidents that cannot be resolved over the phone. To support this approach, this report analyzes over Nine Hundred and Fifty-Two Thousand, Eight Hundred and Thirty-Three (952833) 911 calls to enhance emergency response efficiency, assess the mental health impact of critical incidents, and evaluate the effectiveness of resource allocation.
Using Python and SQL, we identified key trends, assessed performance metrics, and highlighted critical safety concerns. The findings aim to optimize unit dispatch processes, prioritize resources effectively, and ensure timely responses to the most urgent situations.

This report analyzes over Nine Hundred and Fifty-Two Thousand, Eight Hundred and Thirty-Three (952833) 911 calls to improve emergency response times, assess the impact of critical incidents on mental health, and evaluate the effectiveness of resource allocation. By leveraging Python and SQL queries, we uncovered trends, evaluated performance metrics, and identified key safety issues.  
Key findings include:  
911 Call summation: Total 911 calls for the whole year (2021-2024) was observed to be 952, 828 with the highest call summation falling on to 2022.
Response Times: Average response time was 2,254 seconds for the whole year, with an increase as the year moves closer to 2024.  
Unit Time on Scene: Average unit time on scene was 6,090 for the whole year round.
Critical Incidents: Mental health-related calls increased by 12% compared to the previous year.  
Resource Allocation: Areas with frequent calls had uneven officer deployment, contributing to slower responses in high-density zones.  
Recommendations include optimizing resource distribution, focusing on mental health interventions, and refining call categorization processes to enhance officer and community safety.  

### Introduction  
Emergency 911 services are the backbone of public safety, and efficient responses are crucial for minimizing harm. This project aimed to evaluate Nine Hundred and Fifty-Two Thousand, Eight Hundred and Thirty-Three (952833) 911 calls to identify patterns, improve response times, and assess the effectiveness of resource allocation. The analysis also considered the growing importance of addressing mental health-related incidents and community safety.  
Stakeholders include the Austin Police Department (APD), emergency responders, policymakers, and the broader community.  

### Data Overview 
Dataset Description: 
Source: APD’s comprehensive database of 911 calls.  
Attributes: Call type, timestamp, response time, location, priority level, and mental health incident tags.  
Timeframe: 2021 to 2024.  
Data Cleaning Process:  
Handling Missing Values: 
Deduplication: **Are there duplicate values and how are they handled ****
Data Transformation: ***any calculated field and added columns****  
Tools and Methods: 
SQL queries for trend analysis
Python for supplementary data preprocessing
Tableau for visualization.  
Analysis 
Call Volume Trends:
Total calls: 952,833 
By Priority (%) for the overall year: 
Priority 0: 12.68%
Priority 1: 18.64%
Priority 2: 50.33%
Priority 3: 18.55%
Response Time Insights: 
Average response time:   
Longest delays occur between when and when  
Evalyn 
Top Issues:
Disturbances: 349,350 incidents.
Welfare Checks: 220,516 incidents.
Suspicious Activities: 183,839 incidents.
Trespassing: 168,174 incidents.
Average Response Time: 2,254 seconds (37.5 minutes).
Average Unit Time on Scene: 6,090 seconds (101.5 minutes).
Officer & Subject Injury: Minimal incidents reported (1 officer injured, 3 subjects injured)
Officer Edward handled the highest workload with 137,979 cases, followed by David (113,262 cases) and Frank (105,073 cases).
Higher call volumes observed during late night and early morning hours on Saturdays.
Specific peak times include 12 AM to 3 AM on weekends.




Evalyn:
Dataset Description:
Incident Number- A unique integer identifying a computer-aided dispatch incident, consisting of a two-digit year number, three-digit day-of-year and four-digit incident-count number.

Incident Type - A flag indicating whether a given incident was dispatched or officer-initiated. Dispatched incidents are received via 911 calls while officer-initiated incidents are created by officers in the field.

Mental Health Flag - A flag indicating whether a given incident was mental-health related or not Mental Health 

Priority Level - The priority level assigned to the incident at the time of the first officer's arrival. Priority levels range between 0 and 4, with 0 being the highest priority and 4 being the lowest priority.

Response Datetime -The date and time that the 911 call-takers Emergency Call Taker (ECT) screen opened following the 911 call being answered in the case of dispatched incidents. SI unit seconds.

Response Day of Week - The three-character day of week of the Response Datetime.

Response Hour - An integer representing the hour of day of the Response Datetime

First Unit Arrived Datetime - The date and time that the first APD unit arrived on scene to the incident. This is the endpoint for response time calculations. 

Call Closed Datetime - The date and time that the incident was closed, indicating that all units have left the scene and it is no longer active.

Sector - The Austin Police Department patrol sector where the incident occurred.

Initial Problem Description - A preliminary description of the problem meant to be addressed by the CAD incident based on either the information given to the 911 call taker in the case of dispatched incidents, or information collected by officers in the case of officer-initiated incidents.

Initial Problem Category- A general category describing the problem that the CAD incident was meant to address based on the Initial Problem Description value.

Final Problem Description- A description of the ultimate issue that was meant to be addressed by the CAD incident. 

Final Problem Category- A general category describing the problem that the CAD incident was meant to address based on the Final Problem Description value.

Number of Units Arrived - A count of the number of APD units that arrived on scene in response to the CAD incident. 

Unit Time on Scene - The total amount of time spent on scene by all APD units in seconds.
Call Disposition Description- A description of the outcome of the call.

Report Written Flag - A flag indicating that a responding unit wrote a report in the Records Management System based on this CAD incident. Note that a report being written does not necessarily mean that a criminal offense took place.

Response Time- The amount of time between when the 911 call was answered and when the first officer arrived on scene in seconds. 

Officer Injured/Killed Count- A count of officers seriously injured or killed in a use of force related to this CAD incident where the subject of the use of force was a person with mental illness.

Subject Injured/Killed Count- A count of the subjects of a use of force who were seriously injured or killed in a use of force related to this CAD incident where those subjects had a mental illness.

Other Injured/Killed Count- The number of persons seriously injured or killed in an incident related to this CAD incident where there was also a use of force against an individual with mental illness.

Geo ID- A Census Block Group identifier; a concatenation of the current state FIPS code, county FIPS code, census tract code, and block group number.

Census Block Group- Shortened Block Group Name based on the Census Bureau's Geo ID. 

Council District - The council district where the offense occurred.

II Data Cleaning Process
The data was cleaned using excel for easy access to the entire dataset. The process started with loading the data into excel power query editor. From here I checked for inconsistent data types starting with the date columns.
The date column was coded in datetime format formatted as text values. I handled this using the locale option in each column where I changed the data type to datetime and region to United States.
There are three datetime as Response Datetime, First Arrival Datetime, First Unit Arrival Datetime, Call Closed Datetime.
I created additional columns to get the Month, Day and Time (in hours) to identify trends and patterns. Following loading of the data into excel worksheet which has 952833 total rows, there were 4 errors waiting to be addressed. These errors are null records (rows with missing data) which triggered the alert. I treated this by removing the rows entirely. These rows are 952830, 952831, 952832, 952833. The total count of the dataset became 952829.

1. Handling Missing Values
Initial Check for Missing Values:
The dataset was assessed for missing values using the .isna().sum() method. This helped identify the columns with null entries and determine the scope of the issue.
Threshold-Based Removal of Rows with Null Values:
Rows with fewer than four non-null values were dropped using police_df.dropna(thresh=4, inplace=True). This ensured that rows with insufficient data were excluded, improving the dataset's reliability.
Filling Missing Values:
After removing incomplete rows, any remaining missing values were filled with 0 using police_df.fillna(0, inplace=True). This approach prevented null values from causing issues during analysis or computation.


2. Duplication
Identifying and Removing Duplicate Records:
The dataset was checked for duplicate rows using police_df.drop_duplicates(inplace = True). Duplicate entries can inflate the importance of certain data points or introduce bias. Removing them ensures accuracy and prevents redundancy in analysis.
Excel
Duplicate values are present in the Incident Number columns which could have stood as the primary key for each record. Upon closer inspections the records hold different incident values. There were differences between the records upon closer inspection or comparison. This was the reason for leaving the records without dropping duplicates.


3. Data Transformation
Datetime Formatting:
Columns containing datetime information were converted to a consistent and correct format using the pd.to_datetime() function:
Response Datetime
First Unit Arrived Datetime2
Call Closed Datetime
The format='mixed' parameter was used to handle inconsistencies in the input formats, and dayfirst=True ensured dates were interpreted correctly in a day-month-year format.
Effect of Transformation:
Standardizing the datetime format enabled efficient temporal analysis, such as calculating response times or understanding trends over specific timeframes.


4. Final Dataset Consistency Check
Verification of Missing Values:
After handling missing data and duplicates, the dataset was reassessed using police_df.isna().sum(). This ensured no null values remained, confirming the dataset's readiness for analysis.
Column Visibility:
The setting pd.set_option('display.max_columns', None) was used to display all columns when inspecting the dataset, ensuring comprehensive review and debugging.






Rukayat:
 --What is the average response time for all incidents involving mental health issues?
SELECT 
    AVG(response_time) AS avg_response_time_mental_health
FROM 
    apd_call
WHERE 
    mental_health_flag = 'Mental Health Incident';

--Find the average response time for each incident type and compare it with the overall average response time
WITH incident_avg AS (
    SELECT 
        incident_type,
        AVG(CAST(response_time AS BIGINT)) AS avg_response_time
    FROM 
        apd_call
    GROUP BY 
        incident_type
),
overall_avg AS (
    SELECT 
        AVG(CAST(response_time AS BIGINT)) AS overall_avg_response_time
    FROM 
        apd_call
)
SELECT 
    ia.incident_type,
    ia.avg_response_time,
    oa.overall_avg_response_time
FROM 
    incident_avg ia, overall_avg oa;


--What is the total number of mental health-related incidents, and how has this changed over time?
SELECT 
    DATEPART(YEAR, response_datetime) AS year,
    DATEPART(MONTH, response_datetime) AS month,
    COUNT(*) AS total_mental_health_incidents
FROM 
    apd_call
WHERE 
    mental_health_flag = 'Mental Health Incident'
    AND TRY_CAST(response_time AS INT) IS NOT NULL  -- Ensures only numeric response_time values
GROUP BY 
    DATEPART(YEAR, response_datetime), 
    DATEPART(MONTH, response_datetime)
ORDER BY 
    year, month;

--How many incidents were initiated by officers in the field compared to those dispatched via 911 calls?
SELECT
	incident_type,
	count(*) AS incident_count
FROM
	apd_call
GROUP BY
	incident_type;

Add any necessary analysis you think should be added
Question: Which sector calls had the shortest response times, and did mental health-related incidents experience delays due to resource constraints?  (Only for people that did visualization)
Resource Allocation:  
What can you say regarding resource allocation
Safety and Mental Health Impacts:
Critical incidents linked to mental health increased by 12%, emphasizing the need for specialized training and resources.  
Findings 
Give highlight on the findings you observe when interacting with the dashboard
Examples:
Call Trends: Mental health-related incidents are rising, requiring additional attention.  
Response Delays: High-density areas like downtown face longer response times due to inadequate officer coverage.  
Uneven Resource Allocation: Resource distribution does not correlate with call frequency, impacting response effectiveness.  
Rukayat: Between 1 pm and midnight, the frequency of 911 calls reaches the highest levels.
Toheeb
The Edward sector reported the highest number of crimes at 137,979, while the David sector accounted for the highest number of mental health-related incidents, totaling 19,068. Mental health incidents show significant daily variation, with the lowest numbers occurring on weekends—16,400 on Saturday and 16,298 on Sunday. In contrast, these incidents peak on weekdays, particularly on Monday (18,148), Wednesday (18,066), and Friday (18,282). Friday stands out as the day with the highest overall incidents reported.
Evalyn:
Mental health-related calls are significantly high (122,917 cases) which is 12.9% of total., while non-mental health-related calls dominate at 829,911 cases.
The number of incidents per day is steadily increasing from 2022 (211,731) to a projected 242,740 in 2024.



Recommendations  
Optimize Resource Allocation:  Deploy more officers in high-call-density areas, particularly during peak hours.  
Enhance Training Programs: Provide specialized training for mental health crisis intervention to improve response outcomes.  
Leverage Predictive Analytics: Use historical call data to predict and prepare for peak periods and high-priority incidents.  
Community Engagement: Raise awareness about mental health resources to reduce 911 dependency for non-urgent incidents. 
Toheeb
To ensure effective case management, proper and accurate record-keeping is essential. Key fields such as call disposition description, initial problem description, initial and final problem categories should be reviewed and refined to categorize related crimes more effectively.  
Additionally, data standardization must be prioritized during logging. For instance, incident numbers should be unique for each record to eliminate duplicates and maintain data integrity.
Evalyn:
Mental health-related incidents (e.g., "Unable to Locate" and "Report Written MH") account for a substantial portion of calls. Investing in specialized crisis intervention teams trained in mental health de-escalation can:
Improve case resolution.
Reduce repeat calls and ensure effective support for affected individuals.
Officers in low-performing units should receive additional training or technological upgrades (e.g., better communication tools or GPS tracking).
Units with high workloads may benefit from automation in report generation or AI-based dispatch systems to reduce administrative strain.
Integrating a real-time alert system can dynamically notify officers of demand surges, ensuring appropriate action.



Add more based on your observation 
Challenges and Limitations
Data Gaps: Missing values in response times required imputation, potentially introducing bias.  
Scope Limitations: Analysis focused on historical data without accounting for real-time operational variables (e.g., geo ID).  
Mental Health Tags: Limited accuracy in identifying mental health incidents due to inconsistent tagging.  
Gabriel: Data types were not clear despite having the data dictionary
Rukayat: Data types included inside the data dictionary were inconsistent and they had to be changed while writing the queries.
Evalyn: The GeoID provided does not correspond to a recognizable location on the map. As a result, it was not possible to generate a map or identify the specific areas where incidents occurred or where units were dispatched.
Toheeb
The dataset showed inconsistencies with the provided data dictionary. Notably, it contained only one incident type, which contradicted the variety expected based on the supporting document. Additionally, the call categories included values that could be consolidated, suggesting opportunities for data refinement and standardization.
Some questions in the dataset couldn’t be answered for instance question three which have all the sectors mental health incidents percentages below 30%.
Add more challenges and limitations you observed during the analysis
Conclusion
The analysis of Nine Hundred and Fifty-Two Thousand, Eight Hundred and Thirty-Three (952,828) 911 calls revealed critical trends and resource gaps impacting response efficiency and community safety. Addressing the rise in mental health-related incidents and optimizing resource deployment are key steps toward improving public safety outcomes. Future work should incorporate real-time data and advanced predictive models for better operational planning.  
