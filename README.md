
# Hospital Emergency Room Dashboard

## Project Summary

**Duration:** 19 Months

**Records Analysed:** 9,216 Patients

**Pages:** 4

**KPIs:** 4

**Dashboard Type:** Operational Analytics Dashboard
## Problem Statement

This dashboard enables hospital management to monitor Emergency Room operations and resource utilization through interactive visualizations. It provides insights into patient volume, consultation wait times, admission status, referral trends, patient demographics, and satisfaction scores, helping stakeholders identify operational bottlenecks and make data-driven decisions to improve patient care.



Since, the overall satisfaction score was 4.99, this gives them opportunities to improve the overall patient experience and they must work on improving their services. 

The average consultation wait time of 35.3 minutes indicates an opportunity to optimize patient flow and staffing during peak hours.



### Dashboard Features

### 📅 Monthly View

Monitor key metrics and trends on a monthly basis to identify patterns and areas for improvement


#### Purpose

Monitor monthly Emergency Room performance by analyzing patient volume, operational efficiency, referral trends, and demographic distribution.

#### Key Features
- Interactive Year and Month slicers for dynamic filtering.
- **KPI Cards**


                    Total Patients

                    Average Wait Time

                    Patient Satisfaction Score

                    Total Referrals

- Admission status analysis comparing admitted and discharged patients.
- Department referral analysis to identify the most frequently referred departments.
- Age group analysis to understand patient demographics.
- Gender distribution and patients treated within 30 minutes.
- Weekly and hourly patient arrival heatmap using a custom Wait  Time Interval calculated column.
- Calendar table for extracting the day name 

#### DAX Measures :
     
           Patients_count = DISTINCTCOUNT('Hospital ER_Data'[Patient Id])                       
#### Calculated Column : 

        Wait time interval = 
         SWITCH(TRUE(), 
        'Hospital ER_Data'[Admission Hour] < 2, "00-02",
        'Hospital ER_Data'[Admission Hour] < 4, "02-04",
        'Hospital ER_Data'[Admission Hour] < 6, "04-06",
        'Hospital ER_Data'[Admission Hour] < 8, "06-08",
        'Hospital ER_Data'[Admission Hour] < 10, "08-10",
        'Hospital ER_Data'[Admission Hour] < 12, "10-12",
        'Hospital ER_Data'[Admission Hour] < 14, "12-14",
        'Hospital ER_Data'[Admission Hour] < 16, "14-16",
        'Hospital ER_Data'[Admission Hour] < 18, "16-18",
        'Hospital ER_Data'[Admission Hour] < 20, "18-20",
        'Hospital ER_Data'[Admission Hour] < 22, "20-22",
        'Hospital ER_Data'[Admission Hour] < 24, "22-24")


        
#### Calendar table :
        
        Day = FORMAT(Calendar_date[Date] , "ddd")
        
&nbsp;
#### Dashboard snap :

&nbsp;

![Dashboard](https://github.com/Dhanashrilp/Hospital-Emergency-Room-Analytics-Dashboard/blob/main/images/ER_Monthly_view.png?raw=true)
        

### 📊 Consolidated View


##### The Consolidated View page allows users to analyse data across any selected date range.



  
    Allows users to analyse patient trends across any custom date range using an interactive date slicer.

&nbsp;

#### Dashboard snap :

&nbsp;
 ![Dashboard](https://github.com/Dhanashrilp/Hospital-Emergency-Room-Analytics-Dashboard/blob/main/images/ER_Consolidated_view.png?raw=true)

&nbsp;
### 👥 Patient Details


Displays detailed patient-level information for operational review 
| Field               |
| ------------------- |
| Patient ID          |
| Full Name           |
| Gender              |
| Age                 |
| Admission Date      |
| Wait Time           |
| Department Referral |
| Admission Status    |

&nbsp;
#### Dashboard snap :

&nbsp;


 ![Dashboard](https://github.com/Dhanashrilp/Hospital-Emergency-Room-Analytics-Dashboard/blob/main/images/ER_Patient_details.png?raw=true)





### 📈 Descriptive Analysis
Summarizes key findings and business recommendations.
 

## Key Insights

Following inferences can be drawn from the dashboard;

#### Total Number of Patients = 9216

   - Average wait time = 35.3 mins

   - Patient satisfaction score 4.99/10

   - Number of patients referred 3816

   - 4,612 patients (50.04%) were admitted for further treatment.
   
   - 4,604 patients (49.96%) were treated and discharged.

   - 4487(48.69%) patients were Female ,
     4705(51.05%) were male
     and 24(0.26%) preferred not to confirm their gender


        

  
## Business Recommendations

• Review staffing during Saturdays.

• Reduce consultation wait time.

• Monitor referral demand.

• Track patient satisfaction monthly.

• Continue analyzing patient flow.


## 🛠️ Tools Used

- Power BI
- Power Query
- DAX
- Excel

## 💼 Skills Demonstrated

- Data Cleaning & Transformation (Power Query)
- Data Modeling
- DAX Measures & Calculated Columns
- Interactive Dashboard Development
- KPI Design & Reporting
- Data Visualization
- Healthcare Data Analysis
- Business Insight Generation

  
