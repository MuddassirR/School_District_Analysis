# School_District_Analysis

## Overview of the School District Analysis
School and student data was analyzed to determine trends and insights for school districts. Data was taken from 2 CSV file datasets, [school data](https://github.com/MuddassirR/School_District_Analysis/blob/main/schools_complete.csv) and [student data](https://github.com/MuddassirR/School_District_Analysis/blob/main/students_complete.csv), and opened in Pandas Python using Jupyter Notebook. The data was merged and put into a dataframe. The dataframe consisted of columns such as student ID, student_name, gender, grade, school_name (school attended by student), reading_score, and math_score. Reading and math scores were the scores each student received in their reading and math courses. The merged dataset also included the size and budget of each school. Some students either jokingly put "DR" and other prefixes in their names or there was a data entry error, hence, prefixes ands suffices needed to be removed.

The merged dataset was necessary in helping the school district make important decisisons pertaining to school performance, enabling school districts to make better decisions regarding to budget and performance. However, it was suspected that grades for 9th grades students in Thomas High School were altered. To combat this, the grades for grade 9 students in Thomas High School were converted to NaNs and the analysis was done again.
  
## Results
Before accounting for the altered grades, we see from the [district summary dataframe](https://github.com/MuddassirR/School_District_Analysis/blob/main/district_summary.png):
- that there were a total of 15 schools
- 39,170 total students
- the total budget was $24,649,428
- the average math score per student was around 79
- the average reading score per student was 81.9
- the percentage of students who passed math (passing grade is 70 or higher) is 75%
- the percentage of students who passed reading (passing grade is 70 or higher) is 85.8%
- and the percentage of students that passed both math and reading was 65.2%

To clarify, the dataframe was formatted to include dollar sign for total budget and only go to 1 decimal place for percentages.

When accounting for the altered grades, we frrom the [district summary dataframe (acounted for altered grades)](https://github.com/MuddassirR/School_District_Analysis/blob/main/district_summary_accounted.png)
- that the total number of schools is still 15 as expected
- total students is still 39170
- average math score is 78.9
- average reading score is 81.9
- % passing math is 74.8
- %passingh reading 85.7
- overall passing Percent is 64.9, which is a notable difference. 

When looking at [school summaries](https://github.com/MuddassirR/School_District_Analysis/blob/main/school_summary.png), we see that in Thomas High School:
- the average math score is 83.42
- the average reading score is 83.85
- the number of students passing math is 93.27%
- the number of students passing reading is 97.31%
- and the number of students passing both is 90.95%

When accounting for altered grades, we see from the [updated school summary](https://github.com/MuddassirR/School_District_Analysis/blob/main/school_summary_accounted.png), we see that in Thomas High School:
- the average math score is 83.36
- the average reading score is 83.90
- the number of students passing math is 66.91%
- the number of students passing reading is 69.66%
- and the number of students passing both is 65.08%

Thus, we see a significant difference in the percentage of students passing in Thomas High School when only including grades 10-12, implying that grade 9 percentages are far above the normal.

We also see from the [scores by grade](https://github.com/MuddassirR/School_District_Analysis/blob/main/scores_by_grade.png), before not inlcuding grade 9 students in Thomas High school, that:
- the math score for students in grade 9 in Thomas High School is on average 83.6
- the math score for students in grade 10 in Thomas High School is on average 83.1
- the math score for students in grade 11 in Thomas High School is on average 83.5
- the math score for students in grade 12 in Thomas High School is on average 83.5
- the reading score for students in grade 9 in Thomas High School is on average 83.7
- the reading score for students in grade 10 in Thomas High School is on average 84.3
- the reading score for students in grade 11 in Thomas High School is on average 83.6
- the reading score for students in grade 12 in Thomas High School is on average 83.8
- our results with the adjusted dataframe for excluding grade 9 students will have the exact same numbers, except grade 9 average scores for math and reading will be a NaN value.
- scores by school spending did not change
- scores by school size did not change 
- scores by school typee did not change as well.


## Summary
4 major differences can be highlighted when excluding grade 9 students in Thomas High School. First, we see that the percentage of total students in the dataframe that passed both math and reading was 65.2% before exclusion. When excluding, the overall passing Percent was 64.9, implying that excluding grade 9 students in Thomas High School(THS) had a signficant impact in reducing the total percetange of overall passing students in the district. Second, we see before exluding, the % of students in THS passing math was 93.27%, which decreased to 66.91% after exclusion, implying grade 9 students signficantly boosted the average and likely had averages higher than 100, which is impossible. Third, the % of students in THS that passed reading was 97.31% pre exclusion, which dropped to 69.66% after exclusion, implying the same thing. Finally, using the statements just mentioned, the % of students in THS passing both math and reading was 90.95% before exclusion which decreased to 65.08%, overall implying that grade 9 math and reading grades were altered. 


