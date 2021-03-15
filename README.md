# School_District_Analysis

## Project Overview
I am helping the head of data science at a school district analyze high school student's standardized test score data for analysis, reporting, and insights about performance trends and patterns. These insights are used to inform discussions and strategic decisions at the school and district level. In this analysis the variables we focused on were school budgets, size, and type (district vs charter) compared to student's standardized test scores in reading and math in order to explore if there is any apparent relationship between these variables and student performance.

Additionally, after running our intial district and school level analyses, the school board brought to our attention that the file with student test score data showed evidence of academic dishonesty. Specifically speaking, the affected data was that of the Thomas High School 9th graders. To ensure our district and school analyses are accurate, we decided to rerun the analysis without Thomas High School's 9th grade math and reading scores.

Github does not properly format the tables from jupyter notebooks. Go to the following link for proper formatting of our school analyses: https://nbviewer.jupyter.org/github/asliwinski23/School_District_Analysis/blob/main/PyCitySchools_Challenge.ipynb

## Resources
  * Data Source: schools_complete.csv, students_complete.csv
  * Software: Python 3.6.1, Jupyter Notebook, 1.0.0, Pandas, 1.1.3

## How does replacing Thomas High School's 9th grade scores affect the analysis?
Our results did vary from our first pass at the district and school analysis once we nullified Thomas High School's 9th grade math and reading scores, however not in a significant way. Highlighted below are the ways in which our analysis was or was not affected as well as some of the general patterns observed.

### District Summary
The district summary was not affectly greatly as 9th graders at Thomas High School only account for 1% of the student's in this study.

Below is the final district summary:
![District_Analysis](https://github.com/asliwinski23/School_District_Analysis/blob/main/Resources/District_Analysis.png)

### School Summary
Of course, in the school-level summary, the only difference was the row  for Thomas High School, as theirs was the only data that had invalid points of data. However, there was not a significant difference (<1%) in the percentage of students who passed the reading test, math test, and passed both the reading and math tests once 9th grade scores were omitted.

Below is the final school summary:
![Per_School_Analysis](https://github.com/asliwinski23/School_District_Analysis/blob/main/Resources/Per_School_Analysis.png)

### Performance Relative to Other Schools in the District
The first time we ran our analysis, Thomas High School was ranked 2nd of the 15 schools in terms of percentage of students who passed both the math and reading tests. Similar to the district and school summaries, not much changed when ommitting the 9th grade data for Thomas High School. In fact, they still remained ranked 2nd.

Below are the top 5 performing schools by % Overall Passing:
![top_five_schools](https://github.com/asliwinski23/School_District_Analysis/blob/main/Resources/top_five_schools.png)

### Math and Reading Scores by Grade
The math and reading scores were not affected aside from the fact that 9th grade data for Thomas High School reads as 'nan'.

### Scores by School Spending
As aforementioned, we analyzed how school budget would affect student performance in math and reading. After calculating each school's budget per student, we were able to categorize schools into four spending bins: <$584, $585-$629, $630-$644, and $645-$675. Thomas High School fell within the $630-$644 budget per student range. Again, there was no significant drop (<1%) change in the data. It is quite unintuitive, but we noticed that the schools with lower budgets per student had higher passing rates. 

Below is the table for Math and Reading Scores by School Budget per Student:
![scores_by_spending](https://github.com/asliwinski23/School_District_Analysis/blob/main/Resources/scores_by_spending.png)

### Scores by School Size
Another variable we wanted to inspect to see if there is any relation to test scores was school size (by student count). We created a 'small' (0-1000 students), 'medium' (1001-2000 students), and 'large' (2001-5000 students) category for schools. Thomas High School fell into the 'medium' category, where the results were not signifcantly affected in any category. One trend that can be noted is that smaller schools tend to perform better on the state reading and math tests.

Below is the table for Math and Reading Scores by School Size:
![scores_by_size](https://github.com/asliwinski23/School_District_Analysis/blob/main/Resources/scores_by_size.png)

### Scores by School Type
There are two types of schools: charter and district. Thomas High School is a charter school. While removing the 9th grade data did not make a significant difference in the table below, we can see that charter schools tend to perform considerably better than district schools on average, especially in math.

Below is the table for Math and Reading Scores by School Type:
![scores_by_type](https://github.com/asliwinski23/School_District_Analysis/blob/main/Resources/scores_by_type.png)

## Summary
There are minimal changes when we omit the Thomas High School 9th grader data because they only account for 1% of the student population we have data for. However, four changes between our first analysis vs second analysis without Thomas High School 9th grader scores are:
1. The number of total students we have data for dropped by ~1%
2. The number of students we have data for at Thomas High School dropped by ~28%
3. We no longer have data for Thomas High School 9th graders when trying to compare to other schools
4. % Overall Passing changed by <1%, but this column changed the most between our analyses
