# School_District_Analysis

## Overview of the School District Analysis
School and student data was analyzed to determine trends and insights for school districts. Data was taken from 2 CSV file datasets, [school data](https://github.com/MuddassirR/School_District_Analysis/blob/main/schools_complete.csv) and [student data](https://github.com/MuddassirR/School_District_Analysis/blob/main/students_complete.csv), and opened in Pandas Python using Jupyter Notebook. The data was merged and put into a dataframe. The dataframe consisted of columns such as student ID, student_name, gender, grade, school_name (school attended by student), reading_score, and math_score. Reading and math scores were the scores each student received in their reading and math courses. The merged dataset also included the size and budget of each school. Some students either jokingly put "DR" and other prefixes in their names or there was a data entry error, hence, prefixes ands suffices needed to be removed using the following commands: 

prefixes_suffixes = ["Dr. ", "Mr. ","Ms. ", "Mrs. ", "Miss ", " MD", " DDS", " DVM", " PhD"]
 # Iterate through the words in the "prefixes_suffixes" list and replace them with an empty space, "".
for word in prefixes_suffixes:
    student_data_df["student_name"] = student_data_df["student_name"].str.replace(word,"")

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





## Summary

