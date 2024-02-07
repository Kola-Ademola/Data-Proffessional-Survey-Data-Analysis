# Data-Proffessional-Survey-Data-Analysis
## by Kola Ademola
___
![](images/survey.jpg)
___
## INTRODUCTION
___
Inspiration for this project is gotten from Alex Freberg big thanks to him.!!!! For this project I used the survey data Alex Freberg collected from a survey of Data professionals.. 

## PROBLEM STATEMENT
The purpose of this analysis is just to get an insight of what data roles/jobs are like. I am interested in finding out the following from this analysis:
* Which Data role earns the most salary?
* What are satisfaction levels like in terms of, Management, Work/Life balance and Salary.
* Which country can I get the most salary as a data Professional?
* Which Industry do Data professionals work in the most & what programming language is most common?
* What do these data professionals look out for when they're searching for their next role?
* How difficult is it to break into data?

___
## DATA SOURCING
___
This is a real dataset from a survey conducted by [Alex Freberg](https://www.youtube.com/@AlexTheAnalyst).  
Here's a link to his [Youtube](https://www.youtube.com/@AlexTheAnalyst)  
Link to [Dataset](https://github.com/AlexTheAnalyst/Power-BI/blob/main/Power%20BI%20-%20Final%20Project.xlsx)
___
## SKILLS DEMONSTRATED
___
For this project I used the following tools;
* **Python -->** For Data Cleaning
* **Power BI -->** For Data transformation, Data Modelling & Visualization
  
### DATA CLEANING
The survey raw data was very dirty with many data quality issues. I first imported the dataset into a Jupyter notebook where I used Python to clean the data.  
![](images/python_import.png)  
I did a lot of cleaning with Python but I will just walkthrough the important parts.  
> I dropped some columns that I would'nt use in my analysis first.
![](images/drop_col.png)
___
> The salary was in a range ie (10-20k, 30-40k etc..) so I had to extract the salary values and then calculated the average salary for each response from the range given by the respondent.  
![](images/get_salary.png)
___
> The last important cleaning step was to replace all the free responses, where respondents could type anything to just **"Others"**
![](images/other_cleaning.png)
___
> After cleaning, I exported the cleaned data for further transformation and visualizations in Power BI.
![](images/export_clean_data.png)
___
### DATA TRANSFORMATION & MODELLING
___
The dataset was still in a single table, so I had to do some extra transformation in Power BI to create dimension tables out of the data. The dimension tables created were;
* **ROLES** table: This hold info on all the job roles.
* **INDUSTRIES** table: This holds info on all the job industries.
* **COUNTRIES** table: This holds info on all the countries of the participants.
* **PROGRAMMING LANGUAGES** table: This holds info on all the languages used by participants for their jobs.

I then used these to create a simple **STAR SCHEMA** with the main survey data table as the *Fact* table.  
![](images/model.png)
___
## ANALYSIS & VISUALIZATIONS
___ 
This dashboard has a single report page
![](images/dashboard.png)
### [LINK TO DASHBOARD](https://app.powerbi.com/view?r=eyJrIjoiODVmMGFiM2EtYjBhNS00NzBhLThjODMtMDYyYjlkZDVhMGQwIiwidCI6ImQyMzQyMjIxLWJiM2ItNGQ1ZS04NWRmLTkyYzFlOTg0YTNlZCJ9)
___
I am interested in finding out the following from this analysis:
But first, a quick insight about the participants;  
![](images/summary.png)  
> There's a **565** participants in total, with **$55k** average salary & an average age of 30.
___
* Which Data role earns the most salary?  
![](images/avg_salary.png)  
> Based on this survey, it's clear that **Data Scientists** earn the most, with an average salary of **$97k**..  
* Gender Breakdown  
![](images/avg_salary.png)
> ..and **Women** earn more than Men with **$58k** to **$55k**.
___
* What do these data professionals look out for when they're searching for their next role?
![](images/job_factor.png)
> Most of the participants were looking for **Better Salary**
___
* and How difficult is it to break into any data role?
![](images/difficulty.png)
> According to this survey the participants are neutral on how difficult it is to break into data, as most of them said it's **Neither easy nor difficult**
___
* What are satisfaction levels like in terms of, Management, Work/Life balance and Salary.
### SATISFACTION LEVELS
|Management|Work/Life balance|Salary|
|----------|-----------------|------|
|![](images/mgt_sat.png)|![](images/work_sat.png)|![](images/salary_sat.png)|
> We can still see that most are generally not satisfied with their salary as *Salary satisfaction is the lowest at 43%*. Although the *Management: 54% & Work/Life Balance: 58%* are not so great as well.
___
___
* Which country can I get the most salary as a data Professional?  
|Ireland|Denmark|USA|
|--------------------------------|--------------------------------|--------------------------------|
|![](images/part_by_country1.png)|![](images/part_by_country2.png)|![](images/part_by_country3.png)|  
> The salary in **Ireland: $95k** & **Denmark: $84k** is very high when compared to **USA: $78k**, but we should also notice that *Ireland & Denmark* have less than 3 participants in this survey and this might not be a good representation of that country while **USA** has the most participants with an average salary of **$78k** so that would be a better choice to pick as the country that pay the most for data roles.
___
* Which Industry do Data professionals work in the most & what programming language is most common?
![](images/roles_by_in.png)
> Most participants work in different industries which were just grouped as **Others**, but we can also see that **Python** is the most used Programming language.
___
## CONCLUSION
After this analysis, based on this survey data only:
* Most data professionals are really not happy with their salary and coupled with the fact that *better salary* is what most were looking for in their next job. Also the HR department should also do well in terms of management while the work/life balance is upto both the participant and management to attain a great balance.

* Most professionals prefer to use Python and me personally I love Python as well. 😂
* The United States seems to do better in terms of Salary as compared to other countries.
* In as much as I love **Data Analytics & Data Engineering** they don't pay as much as **Data Science**.
