# HEALTHCARE ANALYSIS PROJECT

## PROJECT DESCRIPTION
   This project aims to analyze key healthcare metrics to gain insights into hospital operations, patient demographics and financial performance.
   By leveraging data on total billing, patients counts, average patient age and average lenght of stay(ALOS), this project seeks to identify trends, 
   optimize resource allocation and support data-driven decision-making for healthcare administrators and stakeholders.
<img width="1366" height="768" alt="Screenshot (83)" src="https://github.com/user-attachments/assets/ca406f9d-f688-4361-b62a-79beba53b1f6" />

### TECHNOLOGY & TOOLS USED
    - **Power BI Desktop** (data modeling, DAX, visuals)
    - **Power Query** (ETL / cleaning)
    - **Excel** (.xlsx source data)
    - DAX for measures and calculated tables


### STEPS FOLLOWED:
    * Step 1: Load data into power bi desktop, dataset is an xlsx file.
    * Step 2: Open the power query editor to check for duplicates, empty cells and missing values.
    * Step 3: Remove duplicates, empty cells and fill up missing values using the fill up & down option (fill with averages).
    * Step 4: Click on the close & apply button on the menu bar to close the power query editor window and apply any pending changes.

### ADD CALCULATED TABLE
    * Step 5: Using the Date column from the dataset to create a date table
               - DATE TABLE = CALENDARAUTO()

    * Step 6: Extracting the month and day from the Date Table
               - MONTH = FORMAT('DATE TABLE'[Date],"MMMM")
               - DAY = FORMAT('DATE TABLE'[Date],"DDDD")
               - YEAR = YEAR('DATE TABLE'[Date])

### KEY METRIC & DAX MEASURES
    * Step 7: TOTAL BILLING = SUM(Data[Billing Amount])

    * Step 8: TOTAL COUNT OF PATIENTS = COUNT(Data[Patient ID])

    * Step 9: AVERAGE AGE OF PATIENTS = AVERAGE(Data[Age])

    * Step 10: AVERAGE BILLING AMOUNT = AVERAGE(Data[Billing Amount])

    * Step 11: AVERAGE LENGHT OF STAY = AVERAGE(Data[Length of Stay])

    * Step 12: COUNT OF NORMAL TEXT RESULTS = COUNTROWS(FILTER('Data','Data'[Test Results]="Normal"))

    * Step 13: COUNT OF ABNORMAL TEXT RESULTS = COUNTROWS(FILTER('Data','Data'[Test Results]="ABNORMAL"))

### VISUALIZATION
    * Step 14: Count of Patient ID by Gender <Donut Chart>
                The analysis aggregates patients counts by gender to understand demographic distribution and its impact on hospital operations,
                resource allocation and care delivery.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/b099fb9e-0584-4b90-8b03-aac2482d7c17" />
![Patient Count by Gender - Donut Chart](Screenshot%20(71).png)
    * Step 15: Count of Patient ID by admission <Treemap Chart>
                The distribution of patients by admission type provide nsights into hospital operation, resource demands and patient care patterns.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/98306a6e-3490-4ca5-88af-cbb458ef883b" />

    * Step 16:  Condition distribution by Age,Gender and Blood type <Clustered Bar Chart>
                It analyzes the distribution of medical conditions across age groups, genders and blood type. Its goal is to identify patterns in
                condition prevalence, support clinical decision making and inform research allocation.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/21a9167a-9e0c-420a-b023-50f449133339" />

    * Step 17: Trend of Billing over month <Line Chart>
                It tracks monthly billing amount. Its goal is to support financial planning, resource allocation and cost optimization.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/107a00c9-bd5c-47f6-bf7e-e4cb923fa97d" />

    * Step 18: Correlation between blood types and specific conditions <Stacked Column Chart>
                It analyzes the distribution of medical conditions by blood type. The goal is to uncover patterns in condition prevalence across blood 
                types and support hypothesis generation for further study.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/30cddfbf-ca65-41c1-95f9-77cfa8458847" />

    * Step 19: Billing Amounts per Provider <Stacked Column Chart>
                It calculates total and average billing amounts per insurance providers. Its goal is to support hospital financial planning, insurance
                contract negotiations and equitable care delivery.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/7357864c-8efe-42a9-a771-600cc1f72191" />

    * Step 20: Patient Load per Hospital <Stacked Bar Chart>
                It refers to the volume of patients a hospital manages over a specific period.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/7651bb75-2757-4870-a0ac-591534373cbe" />

    * Step 21: Admission trend per year <Line Chart>
                Refers to changes in the number of patient admissions to hospitals over time. It provide insights into healthcare demands, resource 
                utilization and system performance.
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/04dbb1d4-aca7-4436-b548-f6f185cf019e" />

### ADD INTERACTIVITY WITH SLICER
    1. Select the slicer visual: In the visualizations pane (on the right), click the slicer icon. This adds a blank slicer to your report canvas.
    2. Add a field to the slicer: In the fields pane, locate the dataset and drag the field you want to filter(Year) into the 
       values area of the slicer.
    3. Resize and format the slicers to control user interactions.

### KEY INSIGHTS
    * The predominance of elective admissions may indicate strong patient access to preventive or specialized care, but it also underscores the need
      to maintain adequate resources for managing unpredictable urgent and emergency cases to ensure balanced care delivery.
    * Medicare reveals a higher percentage of total billing compared to other health providers indicating  a strong reliance on medicare within the
      healthcare system. This trend emphasizes the need for a balanced provider network to ensure equitable access to care across diverse patient
      demographics.
    * The visual for patient load by Hospital illustrates that Houston Methodist Hospital handled the highest patient loads in the region. This highlights
      potential challenges, such as strain on resources and staffing.
    * Test results and condition patterns vary noticeably by age, gender, and blood type → potential for targeted clinical protocols.

### 🚀 How to Use / Explore
    1. Clone the repoBashgit clone https://github.com/Josephine-analyst/Healthcare-Analysis-Project.git
    2. Open pbix/Healthcare-Analysis-Project.pbix in Power BI Desktop
    3. Place the original .xlsx in data/raw/ if you want to refresh

### CONCLUSION
    This healthcare analysis project examined patient data to uncover pattern and insights across multiple dimensions, including patient count by admission
    type, insurance provider,gender,distribution of medical conditions by age group, gender and blood type, billing. Using a hypothetical dataset of 55,501
    patients, the analysis provide actionable findings for hospital operations, financial planning and clinical research. Helping stakeholders plan capacity,
    allocate resources and address care delivery challenges.
     
    
        
    
