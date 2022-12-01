# HET Case Study 
## Instructions 
"This is an unstructured exercise that will be used to evaluate your critical thinking, problem solving, analytic, and data mining skills. 

The data housed in this workbook is 12 months of Member-level (read: Patient level) cost/utilization/diagnosis metrics for one of BCBSILs clients. 

The ultimate goal is to use the 'Client Membership', 'Client Data', & 'Benchmark Data' Tabs to craft a deliverable to your client. 

How you choose to structure that presentation is entirely up to you. There are no wrong answers and any findings you conclude are perfectly acceptable. 

The expectation is that you will leverage any/all resources available to you to help analyze the data and organize your findings in such a way that is presentation friendly. 

You will have 48 hours to complete this exercise. All materials used are due by 9am on the 2nd day post receipt (if received on Friday, 9am -- submission is expected to be Sunday, 9am) to Todd_Peden@bcbsil.com. At which point, a 30 minute conference call will be scheduled with the Health Economics Team in order for you to present your material and walk through your approach. 

Below you will find a data dictionary and a metric 'cheat sheet' designed to aid you in the process. Feel free to email Todd Peden, Director of the Health Economics Team, at the above email address with any questions that you may have throughout this exercise. "		

<br>
<br>

## Data Dictionary

| Field      | Description |
| ----------- | ----------- |
dw_mbr_key      | Unique member identifier       
gender| Character value : M for male and F for female								
age|Age of member at the time of reporting								
zip_cd|Zip code for member's home address								
relationship|Descriptor of the Member's Relationship to the Subscriber (aka - Employee) --  Subscriber ||  Spouse ||  Dependent								
enrollment_month|Number of months during the 12-month period that the member was actively enrolled in the insurance plan								
MSA|Metropolitan statistical area (MSA) is the formal definition of a region that consists of a city and surrounding communities that are linked by social and economic factors								
state|State for member's home address								
area_id|Geographical region identifier of member, related to MSA areas								
risk_score|Concurrent medical risk score								
sdoh_percentile|Percentile score of social determinate of health factors (0.01 = best and 0.99 = worst)								
urban_percentile|Percentile of urbanicity based on member's zip code (0.01 = most rural and 0.99 = most urban)								
hypertension_ind|Indicator for hypertension diagnosis								
depression_ind|Indicator for depression diagnosis								
hyperlipidemia_ind|Indicator for hyperlipidemia diagnosis								
cad_ind|Indicator for coronary artery disease diagnosis								
diabetes_ind|Indicator for diabetes diagnosis								
alcohol_ind|Indicator for alcohol dependency diagnosis								
sud_ind|Indicator for substance use disorder diagnosis								
copd_ind|Indicator for COPD diagnosis								
psychotic_ind|Indicator for psychotic condition diagnosis								
hypothyroidism_ind|Indicator for hypothyroidism diagnosis								
anxiety_ind|Indicator for anxiety diagnosis								
cancer_ind|Indicator for cancer diagnosis								
pregnancy_ind|Indicator for pregnancy diagnosis								
annual_wellness_visit|Indicator showing whether or not the member sought an annual wellness visit during the period								
mbr_months_ccs|Enrollment_month divided by each member's number of records in the table (e.g. for a member who was actively enrolled for 12 months and had 6 rows of data in the table, each row for this member would show mbr_months_ccs = 12/6 or 2.000)								
Primary_CCS_Dx_Level_1|First Level of the Disease Group Hierarchy								
Primary_CCS_Dx_Level_2|Second Level of the Disease Group Hierarchy								
Total_Allowed|Total Expense (Plan paid + Member Responsibility)												
Total_Paid|Total Expense (Plan paid)								
Allowed_Inpatient|Allowed Amount in an Inpatient Setting								
Allowed_Outpatient|Allowed Amount in an Outpatient Setting								
Allowed_Professional|Allowed Amount in a Professional Setting								
Paid_Inpatient|Plan Paid Amount in an Inpatient Setting								
Paid_Outpatient|Plan Paid Amount in an Outpatient Setting								
Paid_Professional|Plan Paid Amount in a Professional Setting								
Adm_cnt_Inpatient|Count of Admissions into an Inpatient Facility								
Day_cnt_Inpatient|Number of Days stayed at an Inpatient Facility								
Visit_cnt_Outpatient|Count of Admissions into an Inpatient Facility								
Visit_cnt_Professional|Count of Visits to a Professional Setting								
Proc_cnt_Professional|Count of Procedures in a Professional Setting								
Svc_unit_cnt_Professional|Count of Services in a Professional Setting								
non_utilizer|Indicator showing whether or not the member sought ANY health care service during the period, 1 means member did not incur any claims during the period								
uniq_mbr_cnt| Unique count of member indentifier
									
<br>

## Cheat Sheet 
| Typical Metric      | Definition | Calculation |
| ----------- | ----------- | ----------|
Paid PMPM | 'Paid Per Member Per Month' - Primary Metric used to evaluate performance. Often used to score year over year increases/declines. | =(Total Paid/member months)
Admissions/1000 |Number of IP Admissions for each 1000 Members within a given time| =(Admissions/Members)*1000			
Visits/1000 |Number of OP/ER/Prof Visits for each 1000 Members within a given time| =(Visits/Members)*1000
Paid per Claimant | Amount of Medical expense per Individual| =Paid/Unique Member

