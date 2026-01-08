# excel_project2_using_DAX
## advanced analysis using DAX  

## Introduction
As getting into data as a job seeker, I always have a doubt what are the most demanding skills to get into data job and what skills do employers adore and willing to pay more. In this project I did analyze the top skills and what kind of roles do we get into with those particular skills.

## Questions that I answer with my analysis

### To get to know more about data jobs, I analysed the following:

  1. Does more skills equals to better pay?
  2. What's the salary for data jobs in different regions?
  3. What are the top skills required for a data job?
  4. What is the pay for the top 10 skills?

## Skills that I used for this project

  1. Pivot Tables
  2. Pivot Charts
  3. DAX: Data analysis expressions
  4. Power query
  5. Power Pivot

## Dataset

The dataset that I used in the project contains real-world data science job information. The dataset is available from luke barousse excel for data analysis course, which gave me the foundation for analyzing data in excel.

### In this data =set we have information about

  1. Job titles
  2. salaries
  3. locations
  4. skills

## 1. Does more skills equal to better pay?

### skill used: Power Query (ETL)

### Extract

Used power query to extract the original data (data_salary_all.xlsx) and created 2 queries
  1. 1st one with all data jobs
  2. 2nd listing the skills for each job ID

### Transform

Transformed each query by changing column types, removing unnecessary columns, cleaning text to eliminate specific words, and trimming excess white space

### Load 

Finally, I loaded both transformed queries into the workbook, setting the foundation for my subsequent analysis.

## Analysis Insights

  1. There is a positive correlation between the number of skills requested in job postings and the median salary, particularly in roles like Senior Data Engineer and Data Scientist.
  2. Roles that require fewer skills, like business analyst, tend to offer lower salaries, suggesting that more specilized skill sets command higher market value.
  
  <img width="564" height="351" alt="08 01 2026_02 12 17_REC" src="https://github.com/user-attachments/assets/fa6afd47-3e41-43d3-87fb-b83a8a1a9481" />

## 2. What is the salary for data jobs in different regions?

### skill used: PivotTables & DAX

Pivot tables:

  1. Created a pivot table using the Data Model with Power Pivot
  2. Moved the job_title_short to rows and salary_year_avg to values
  3. Added new measure to calculate the median salary for US jobs.

      =CALCULATE(
         MEDIAN(data_jobs_all[salary_year_avg])
         data_jobs_all(job_country] = "United States")

DAX:

To calculate the median year salary I used DAX.

  Median Salary := MEDIAN(data_jobs_all[salary_year_avg])

<img width="509" height="242" alt="08 01 2026_02 25 23_REC" src="https://github.com/user-attachments/assets/491d3315-f7cd-4abd-b930-40d01a188663" />

##   3. What are the top skills required for a data job?

### Skills used: Pivot charts, DAX and pivot table.

  1. moved job_skills tab to rows and values
  2. sorted and filted skill count to top 10, and ascending order.


<img width="677" height="335" alt="08 01 2026_02 36 46_REC" src="https://github.com/user-attachments/assets/c0844e44-8ac2-4789-8193-0983f0934cf4" />

##  4. What is the pay for the top 10 skills?

### Skills used: Pivot charts, DAX, pivot table

  1. moved job_skills to rows, calculated median salary for each skills using DAX and moved it to values, job_skills to values.
  2. Sorted it to ascending order and filtered it to top 10.
  3. Used pivot chart to analyze skill count and median salary for each skill.


<img width="1374" height="411" alt="08 01 2026_02 44 25_REC" src="https://github.com/user-attachments/assets/afb63235-87e9-4947-b0b8-4ac2802ee11e" />

🔍 Project Conclusion

This project demonstrates how Excel, Power Query, Power Pivot, and DAX can be leveraged together to answer real-world career questions in the data job market. By transforming raw job posting data into a structured data model and applying DAX measures, I uncovered meaningful relationships between skills, roles, geography, and compensation.

The analysis clearly shows that roles requiring broader and more specialized skill sets tend to command higher salaries, especially in senior and engineering-focused positions. Additionally, geographic comparisons revealed noticeable salary differences across regions, reinforcing the importance of location in compensation strategy. Finally, identifying the most in-demand and highest-paying skills provides practical guidance for aspiring data professionals on where to focus their learning efforts.

Beyond the insights, this project strengthened my ability to:

Design efficient ETL workflows using Power Query

Build scalable data models with Power Pivot

Write meaningful DAX measures for advanced analysis

Translate complex data into clear, decision-driven visuals

This project reinforced a key takeaway for me as a data professional:
👉 data skills are not just about tools—they’re about asking the right questions and delivering insights that drive smarter career and business decisions.

📊🚀





  
