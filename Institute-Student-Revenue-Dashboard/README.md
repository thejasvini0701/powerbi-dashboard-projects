# Institute Student & Revenue Dashboard

An interactive Power BI dashboard that tracks **student enrolment, course-wise revenue and certificate issuance** for a training institute.

## Objective
- Track total students and total fees collected
- Compare enrolments and revenue across courses
- Monitor how many students have been issued certificates
- Understand student demographics by age group and city

## Tools Used
- Power BI Desktop
- Power Query (data cleaning and transformation)
- DAX

## Dataset
Two data sources were combined:

| Source | Type | Contents |
|---|---|---|
| Student Course Details | Folder of files | Student name, age, course, date of joining, fees |
| Student Personal Details | Excel file | Student name, age, contact, email, city, state, certificate issued (Yes/No) |

- Records: 772 students
- Courses: 8
- Cities: 6 (Tamil Nadu and Puducherry)
- Joining period: 2021–2023
- Note: This is a practice dataset (Power BI Basics Practice Pack).

## Data Preparation (Power Query)
- Combined multiple course files from a folder
- Split the combined text column into student name and age
- Capitalized student names and split the fees column
- Renamed columns, removed unwanted columns and set data types
- Removed duplicate students
- Loaded the personal details table from Excel

## DAX Used
```
CountYes = CALCULATE(COUNTROWS('Personal Details'), 'Personal Details'[Issued Certificate] = "Yes")

Countno = CALCULATE(COUNTROWS('Personal Details'), 'Personal Details'[Issued Certificate] = "No")
```
- **Age group** calculated column (`SWITCH`) to group students into Below 20, 20 to 29, 30 to 39 and 40 above

## Dashboard Features
- KPI cards: **Total Students** and **Total Amount (Fees)**
- Gauge: **Certificate Issued**
- Clustered column chart: students by course
- Clustered bar chart: fees by course
- Donut chart: age-wise distribution
- Slicers: City, Course and Student Name

## Key Insights
- Total of 772 students and ₹68.8 lakh in fees
- **Highest revenue:** Davinci Resolve (₹14.0 lakh), Adobe After Effects (₹11.9 lakh) and Autodesk 3ds Max (₹11.8 lakh)
- **Most enrolments:** MS Excel (223), DCA (141) and CCA (138)
- 65% of students (504) have been issued certificates
- About 52% of students are aged 20–29
- Pondicherry has the most students (214), followed by Madurai (161) and Tiruchirappalli (160)

## How to Use
1. Download the `.pbix` file from this repository
2. Open it in Power BI Desktop
3. Update the data source paths to your local files if needed (Home → Transform data → Data source settings)
4. Use the slicers to filter by city, course and student name
