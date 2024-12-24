# Excel Salary Dashboard

![Screenshot 2024-12-16 215811](https://github.com/user-attachments/assets/170e1040-151e-4fe8-a275-d113067b88e7)


## Introduction

This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated. 

The data is which provides a foundation in analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

### Dashboard File
My final dashboard is in [Salary_Dashboard_Practice.xlsx](Salary_Dashboard_Practice.xlsx).

### Excel Skills Used

The following Excel skills were utilized for analysis:

- **📉 Charts**
- **🧮 Formulas and Functions**
- **❎ Data Validation**

### Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023. The dataset provides a foundation for analyzing data using Excel. It includes detailed information on:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

## Dashboard Build

### 📉 Charts

#### 📊 Data Science Job Salaries - Bar Chart

![Screenshot 2024-12-24 200415](https://github.com/user-attachments/assets/e15c9cf3-4616-4af2-a756-dee184755d7c)


- 🛠️ **Excel Features:** Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 **Design Choice:** Horizontal bar chart for visual comparison of median salaries.
- 📉 **Data Organization:** Sorted job titles by descending salary for improved readability.
- 💡 **Insights Gained:** This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

#### 🗺️ Country Median Salaries - Map Chart

![Screenshot 2024-12-24 200537](https://github.com/user-attachments/assets/057bb978-d08d-4d1e-abfc-864bb2d9e2e1)

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
          (jobs[job_title_short]=$A2)*
          (jobs[salary_year_avg]<>0)*
          (jobs[job_country]=country)*
          (ISNUMBER(SEARCH(type,jobs[job_schedule_type]))),
          jobs[salary_year_avg]
     )
)
```

- 🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- 📊 **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
- **🔢 Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

🍽️ Background Table

![Screenshot 2024-12-24 201449](https://github.com/user-attachments/assets/5b84fcbb-3071-41c0-86cf-3b474b1811ab)


📉 Dashboard Implementation

![Screenshot 2024-12-24 201554](https://github.com/user-attachments/assets/67b06c78-a889-449a-bf65-17f9e88fece0)


#### ⏰ Count of Job Schedule Type

```
=FILTER(J2#,NOT(ISNUMBER(SEARCH("and",J2#)))*(J2#<>0))
```

- 🔍 **Unique List Generation:** This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
- **🔢 Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table

![Screenshot 2024-12-24 202119](https://github.com/user-attachments/assets/0c1dd555-6a42-41a2-ab53-13b4938f460e)


📉 Dashboard Implementation:

![Screenshot 2024-12-24 202247](https://github.com/user-attachments/assets/e115a589-8b08-48b5-84b4-ad78250504bc)


### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` option in the Data tab ensures:
    - 🎯 User input is restricted to predefined, validated schedule types
    - 🚫 Incorrect or inconsistent entries are prevented
    - 👥 Overall usability of the dashboard is enhanced

![Screenshot 2024-12-24 202449](https://github.com/user-attachments/assets/831d6eb8-243f-4526-b2bb-44e49ba5a3e3)


## Conclusion

I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from the provided dataset, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries. 

