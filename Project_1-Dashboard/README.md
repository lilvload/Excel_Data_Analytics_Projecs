# Excel Salary Dashboard

<img width="1200" height="520" alt="1_Salary_Dasboard" src="https://github.com/user-attachments/assets/6948f2ce-fe2a-4b60-8885-78de5422868b" />

## Introduction

This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated. 

The data is from [Luke Barousse Excel course](https://youtu.be/pCJ15nGFgVg?si=Ql6toJxpcgihLxgS), which provides a foundation in analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

### Dashboard File
My final dashboard is in [Salary_Dashboard_Project.xlsx](Salary_Dashboard_Project.xlsx).

### Excel Skills Used

The following Excel skills were utilized for analysis:

- **📉 Charts**
- **🧮 Formulas and Functions**
- **❎ Data Validation**

### Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023. The dataset is available via Luke Barousse Excel course. It includes detailed information on:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

## Dashboard Build

### 📉 Charts

#### 📊 Data Professionals Job Salaries - Bar Chart

<img width="790" height="500" alt="2_Chart1" src="https://github.com/user-attachments/assets/d201eb01-5cfa-46b2-8053-97e5f0bb513e" />  

- 🛠️ **Excel Features:** Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 **Design Choice:** Horizontal bar chart for visual comparison of median salaries.
- 📉 **Data Organization:** Sorted job titles by descending salary for improved readability.
- 💡 **Insights Gained:** This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

#### 🗺️ Country Median Salaries - Map Chart

<img width="800" height="470" alt="3_Country_Map" src="https://github.com/user-attachments/assets/950f80a8-fee5-4a9d-a2b3-bd98c9ea3e25" />  

- 🛠️ **Excel Features:** Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 **Design Choice:** Color-coded map to visually differentiate salary levels across regions.
- 📊 **Data Representation:** Plotted median salary for each country with available data.
- 👁️ **Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.
- 💡 **Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.

### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles

```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- 🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- 📊 **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
- **🔢 Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

🍽️ Background Table

<img width="295" height="266" alt="4_Background_Table1" src="https://github.com/user-attachments/assets/f79ff632-784b-4c63-808d-3d44aefe0e36" />

📉 Dashboard Implementation

<img width="493" height="576" alt="5_Dashboard_Implementation" src="https://github.com/user-attachments/assets/a7a3a401-0b56-473e-a1b6-86c938363946" />

#### ⏰ Count of Job Schedule Type

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- 🔍 **Unique List Generation:** This Excel formula above employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
- **🔢 Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table

<img width="366" height="145" alt="6_Background_Table2" src="https://github.com/user-attachments/assets/74f99c95-6380-49a3-81f2-16e2fe0c7012" />

📉 Dashboard Implementation:

<img width="491" height="567" alt="7_Dasboard_Implementation2" src="https://github.com/user-attachments/assets/996c75b6-a62e-4c74-aa7e-8b81033fa723" />

### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` option in the Data tab ensures:
    - 🎯 User input is restricted to predefined, validated schedule types
    - 🚫 Incorrect or inconsistent entries are prevented
    - 👥 Overall usability of the dashboard is enhanced

<img width="480" height="425" alt="8_Data_Validation" src="https://github.com/user-attachments/assets/bae5f53b-1609-4cac-894f-9f6dcc70e050" />

## Conclusion

I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from Luke Barousse Excel course, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries. 
