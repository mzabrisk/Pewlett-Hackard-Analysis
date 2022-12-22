# Pewlett-Hackard-Analysis

## Overview:
Pewlett-Hackard is in aging company with an aging workforce. Management wants a better idea of which employees, and positions, within the company can be expected to retire in the near future. We have been tasked with moving their current excel file system to a SQL database and performing a few queries to give management a better idea of retiring employess by title and employees who are eligible for a proposed mentorship program.

## Results:

- The expected retirees are disproportionately senior level, as can be seen in the retiring titles table:
![](https://github.com/mzabrisk/Pewlett-Hackard-Analysis/blob/0fc160fd8618055a4e1a218e872e2f0cea6537ba/Data/figures/retiring_titles.png)
- Also from the table above, only two managerial level employees are retiring.
- Further analysis of the mentorship_eligibility table shows that the proportions of the different titles present in this population is similar to that in the retiring employees table. Table details are below, and query details are in the summary section.
- Despite similar proportions when comparing titles, there are significantly more employees preparing for retirement than there are eligible for the mentorship program. There are 72,458 employees preparing for retirment, while there are only 1,549 employees eligible for the mentorship program. The queries:
![](https://github.com/mzabrisk/Pewlett-Hackard-Analysis/blob/0fc160fd8618055a4e1a218e872e2f0cea6537ba/Data/figures/sum_queries.png)

## Summary

- 

- Our analysis showed that >25,000 senior engineers and nearly 25,000 senior staff are expected to retire, but the impact of these numbers isn't clear without a better picture of the Pewlett-Hackard workforce. A query showing the employees who are expected to have another 10+ years in the workforce, and their titles, would be very useful.  Unfortunately, it isn't clear what year this data is from:
    - The most recent hires are from 2002-08-01, however we are gating our birthdates for 1952-1955. If the year is 2002, an emloyee born in 1952 would still be far from retirement. Most recent hire dates is evident from this simple query:
    ![](https://github.com/mzabrisk/Pewlett-Hackard-Analysis/blob/0fc160fd8618055a4e1a218e872e2f0cea6537ba/Data/figures/titles_query.png)
    
    - Digging further into the employees table, it appears that the oldest employees were born in 1952, and the youngest born in 1965. The dataset clearly isn't real-world data, or was highly curated before we received it, making a true analysis of the companies future difficult. The queries used to find this information are here:
    ![](https://github.com/mzabrisk/Pewlett-Hackard-Analysis/blob/0fc160fd8618055a4e1a218e872e2f0cea6537ba/Data/figures/employees_query.png)


- A query similar to the retiring titles table should be performed, but on those placed on the mentorship_eligibility table, to give a better idea of the titles present within the cohort. Here is the query used for this analysis:

![](https://github.com/mzabrisk/Pewlett-Hackard-Analysis/blob/0fc160fd8618055a4e1a218e872e2f0cea6537ba/Data/figures/mentorship_count_query.png)