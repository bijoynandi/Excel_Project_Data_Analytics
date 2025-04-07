# Excel Salary Dashboard

## Overview

Interactive Excel dashboard for data job salary insights. Empowering job seekers to explore compensation trends.

Dashboard: [Salary_Dashboard_Practice.xlsx](Salary_Dashboard_Practice.xlsx)

## Skills

*   Excel Charts
*   Excel Formulas & Functions
*   Data Validation

## Data

Real-world data science job info (2023): job titles, salaries, locations, skills.

## Dashboard Highlights

### Charts

#### Job Salaries

*   Horizontal bar chart compares median salaries across job titles.

#### Country Salaries

*   Color-coded map shows global salary variations.

### Formulas

*   `=MEDIAN(IF((jobs[job_title_short]=$A2)*(jobs[salary_year_avg]<>0)*(jobs[job_country]=country)*(ISNUMBER(SEARCH(type,jobs[job_schedule_type]))),jobs[salary_year_avg])))`

    *   Calculates median salary by job title, country, and job type.

*   `=FILTER(J2#,NOT(ISNUMBER(SEARCH("and",J2#)))*(J2#<>0))`

    *   Generates a list of unique job schedule types.

### Data Validation

*   Dropdown lists for Job Title, Country, and Type ensure data integrity.

## Reflection

Created this dashboard to empower data job seekers with salary insights and location factors, enabling informed career decisions.

## Acknowledgement

I would like to express my sincere gratitude to [Luke Barousse](https://github.com/lukebarousse) for providing the guidance and resources that made this project possible. The expertise was invaluable in helping me analyze the dataset and derive actionable insights. The guidance and support were instrumental in the success of this project. Thank you, Luke, for your invaluable contributions!

## Contact

If you have any questions or would like to connect, feel free to reach out to me at [bijoynandi31@gmail.com](mailto:bijoynandi31@gmail.com). I'm always open to discussions and collaborations.