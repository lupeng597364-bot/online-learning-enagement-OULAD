# Readme file for online learning engagement and course outcomes

### HUDK4054 Individual assignment #2

## General Information

### Project title: 
Online Learning Engagement and Course Outcomes

### Creator: 
Peng Lu

### Principal investigator: 
Peng Lu

### Data Manager: 
Peng Lu

### Email: 
pl3017@tc.columbia.edu

### ORCID ID: 
0009-0009-7267-5051

### Affiliation: 
Teachers College, Columbia University

Date of data collection: Source dataset contains records from 2013 and 2014. Project focuses on AAA 2013J, which began in October 2013, and window covers days 0-27 relative to course start.

### Geographic location of data collection: 
Data originate from Open University’s online learning environment in the United Kingdom. Students' residential regions are recorded in region field of "studentInfo.cvs".

### Keywords: 
Learning analytics, online learning engagement, and OULAD

### Language information: 
This README and source dataset both use English

### REAME creation Date: 
09-30-2026


## Data and file overview

### File names and descriptions: 
This project uses 2 source files from OULAD.

| File Name | Description |
| --- | --- |
|studentInfo.csv| Student demographic information and final course outcomes. Each row represents a student enrolled in a particular module presentation. |
| studentVle.csv | Recorded interactions with online learning materials. Each row represents a student's interactions with a particular material on a particular day. |

The selected AAA/2013J subset contains 383 students' information.

### Relationships between Files: 
"sum_click" in studentVle.csv will be summed for each student over days 0-27 and then linked to the student's "final_result" in studentInfo.csv.

### File Creation Dates:

studentInfo.csv: 12-21-2015

studentVle.csv: 09-25-2015

### Related data not included:

The downloaded OULAD package also contains courses.csv, assessments.csv, studentAssessment.csv, studentRegistration.csv, and vle.csv.

## Sharing and Access Information

### Licenses and Restrictions:

The original OULAD dataset is  licensed under a Creative Commons Attribution 4.0 International (CC BY 4.0) license. This allows for the sharing and adaptation of the datasets for any purpose, provided that the appropriate credit is given.

### Publications:

Kuzilek, J., Hlosta, M., & Zdrahal, Z. (2017).
Open University Learning Analytics dataset.
Scientific Data, 4, 170171.
https://doi.org/10.1038/sdata.2017.171

### Accessible locations of the data

Kuzilek, J., Hlosta, M., & Zdrahal, Z. (2015). Open University Learning Analytics dataset [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5KK69.

### Recommended citation for the data

Kuzilek, J., Hlosta, M., & Zdrahal, Z. (2015). Open University Learning Analytics dataset [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5KK69.

## Methodological Information

### Methods for data collection: 

This project uses existing data from OULAD. No new data will be collected. The original collection and preparation procedures are described in the publication:

https://doi.org/10.1038/sdata.2017.171

### Methods used for data processing:
1. Filter both source files to module "AAA/2013J"
2. Selected interaction records with data values from 0-27.
3. Sum "sum_click" for each student to create the first 4 weeks' click counts.
4. Link the counts to studentInfo.csv using code_module, code_presentation, and id_student.
5. Assign zero recorded interactions to students with no interaction records in the selected window, and mark those cases separately.

## Data-specific information

### Number of Variables and records

| File | Number of Records | Number of Variables |
| --- | --- | --- |
| studentInfo.csv | 383 | 12 |
| studentVle.csv | 180,982 | 6 |

### Variable list

#### studentInfo.csv

|Name|Definition|
|---|---|
|code_module|Course module identifier|
|code_presentation| Course presentation identifier|
|id_student|student identifier|
|gender|F=female, M=Male|
|region|Student's residential region|
|highest_education|Highest education level|
|imd_band|Index of multiple deprivation band associated with student's residential area|
|age_band|Age band using label:0-35,35-55, and 55<=|
|num_of_prev_attempts|Number of previous attempts at module|
| studied_credits | Total credits the student was studying|
|disability|Whether student declared disability: Y=yes, N=no|
|final_result|Final course outcome: Pass, Distinction, Fail, or Withdrawn|

#### studentVle.csv

|Name|Definition|
|---|---|
|code_module|Course module identifier|
|code_presentation|Course presentation identifier|
|id_student|student identifier|
|id_site|identifier of online learning material|
|date|Number of days relative to course start|
|sum_click|Number of recorded interactions by student|

### Units of Measurement

Date: days relative to course start
Sum_click: recorded interaction counts
num_of_prev_attempts: number of attempts
studied_credits: academic credits

### Missing data symbol

In the imd_band list for studentInfo.csv, missing data is recorded as ?

In the sum_click list for studentVle.csv, missing data or no interaction record is recorded as 0.

### Specialized formats or abbreviations

|Name|Definition|
|---|---|
|OULAD|Open University Learning Analytics Dataset|
|VLE|Virtual learning environment|
|HE|Higher Education|
|A level|Advanced level|
|2013J|2013 course starting in October|




