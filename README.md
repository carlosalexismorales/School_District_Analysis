# School_District_Analysis_Challenge

Using Pandas, Python and Jupyter notebook for school district analysis

## Project Overview

The school board has notified Maria and her supervisor that the students_complete.csv file shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. They have turned to Maria to help figure out the full extent of the academic dishonesty because they want to uphold state-testing standards. Thus, She has asked us to create a PythonData and use several of the resources at hand to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. Once the math and reading scores have been, Maria would like us to repeat the school district analysis that completed in this module and write up a report to describe how these changes affected the overall analysis.

## Challenge Overview

1. Opening Jupyter Notebook files from local directories using a development environment.
2. Reading an external CSV file into a DataFrame.
3. Formating a DataFrame column.
4. Determining data types of row values in a DataFrame.
5. Retrieving data from specific columns of a DataFrame.
6. Merging, filtering, slicing, and sorting a DataFrame.
7. Applying the Pandas groupby() function to a DataFrame.
8. Using the Pandas loc() method with conditional statements and comparison and logical operators
9. Using multiple methods to perform a function on a DataFrame.
10. Performing mathematical calculations on columns of a DataFrame or Series.

## Resources

- Anaconda version 1.10.0
- Conda version 4.13.3
- Python version 3.9.12
- Jupyter-Notebook version 6.4.11
- Pandas version 1.4.2
- ipykernal version 6.9.1
- Numpy version 1.21.5

## Results

### How is the district summary affected?

Original District Summary DataFrame:
<img width="921" alt="Screen Shot 2022-06-22 at 8 35 48 PM" src="https://user-images.githubusercontent.com/102444078/175203603-8836bb0a-24ae-4a97-b161-2715cd2e35f9.png">


Adjusted District Summary DataFrame:
<img width="922" alt="Screen Shot 2022-06-22 at 8 35 25 PM" src="https://user-images.githubusercontent.com/102444078/175203563-f4b4f970-364e-464c-a6e1-7244fd00a181.png">



The testing data for the 461 9th graders at Thomas High School was turned into null or NaN data. This subsequently recalculated the percentages of passing math, passing reading, and the overall passing. However, removing only 461 test scores did not have a huge impact of the vast data set. Reviewing these two district summaries, we can see that it was a marginal change at most with the differences being minimal. If we were to the round the data to the nearest whole number, they appear to be almost identical. We would have to scrutinize the data and look very closely to see any changes, but this wouldn't be very useful at all.

### How is the school summary affected?

Original Analysis:
<img width="990" alt="Screen Shot 2022-06-22 at 8 41 23 PM" src="https://user-images.githubusercontent.com/102444078/175204178-417e7daf-d538-4bde-bc9b-f43e062d1f59.png">


Adjusted Analysis:
<img width="994" alt="Screen Shot 2022-06-22 at 8 39 34 PM" src="https://user-images.githubusercontent.com/102444078/175203987-12cea3c2-5470-4f29-ac39-ae4e5aadf8cd.png">




After the data from Thomas High School was marked for review, we can adjusted the data to correctly reflect the alterations that were made. We replaced the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. As we can see from the screenshot above, there was a huge impact to the percentages when we removed the 9th grade students data. Passing math dropped to 66%, while passing reading dropped to 69%, and overall passing fell to 65%. As we can see in the original school summary, Thomas High School started with a 93% passing math score, a 97% passing reading score, and a 90% overall passing rate - this was marked by the school board for review since these numbers did not appear to be genuine.


### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?


Original Analysis:
<img width="1000" alt="Screen Shot 2022-06-22 at 8 47 48 PM" src="https://user-images.githubusercontent.com/102444078/175204803-22e17a20-c26d-4da5-9f19-af36e32d5ff3.png">


Adjusted Analysis:



- There are several things we must be attentive to when we replace the ninth graders' math and reading scores: 
 - When we listed the school relative to their performances in the original analysis, we can see that Thomas High School ranked 2nd in the district. This indicated that they were tested extremely well, but also marked an audit for grade alteration. 
 - After adjusting the 9th grade data with NaNs, Thomas High School fell in their rankings, respectively to the bottom 5 schools in passing percentages. 

- When the ninth graders' of Thomas High School had their scores omitted from the calculations, the following changes occured:
 - Thomas High School is still the second best performing school in the district with an overall passing rate of 90.63% among their tenth through twelfth graders.
 - The overall passing percentages of Thomas High School decreased by 0.11%

## How does replacing the ninth-grade scores affect the following:

### Adjusted Averages using the Math and Reading Scores

In the original data, Thomas High School had 83.6 math average and 83.7 reading average for the 9th grade, which matched, exceeded, or came close to the highest averages from every other school. It’s important that we realize that adding or removing an extreme value from the data set will affect the mean, but since these averages weren't too far off, there wasn't too drastic of a change. Since the scores were replaced with null values, which is considered missing data, it shows up in Python programming as NaN in the following charts.

Adjusted Average Math Scores ----------------------------------------------------- Adjusted Average Reading Scores:




### Scores by school spending

Thomas High School falls in the $630-$644/student spending range. However, the hundredths place was needed to see the nominal changes. It is found that Average Scores and Passing Percentages do not increase as spending per student increases. In fact, the top performing school in the entire school district (Cabera High School) received $68 less per student than the lowest performing school (Johnson High School). For the spending range of $630-644 per student, the overall passing percentage decreased by 0.1%

Original Analysis:


Adjusted Analysis:


There was very little spending impact by changing the 9th grade scores.

### Scores by school size

Thomas High School is defined as a medium sized school.
The hundredths place was needed to see the nominal changes.
When considering School Sizes, "Large" Schools (Over 2,000 Students) have the lowest average scores and passing percentages. The difference in performance between "Small" and "Medium" Size Schools is negligible (approximately 1%). Interestingly, all District schools in this dataset are characterized as "Large" schools.
This may be an indication that students in this district learn and perform better in smaller, more intimate settings.

Original Analysis:


Adjusted Analysis:


There was very little impact by campus size due to changing the 9th grade scores.

### Scores by school type

Thomas High School is a charter school type.
The hundredths place was needed to see the nominal changes.
Charter schools generally performed better than District schools in this analysis.
The top five schools with the highest overall passing percentages are all Charter schools, whereas the bottom five are all District Schools.
Charter schools in this dataset were typically characterized as "Small" and "Medium" size schools.
As seen in the DataFrame below, Charter schools have a 36% higher overall passing percentage than District schools.

Original Analysis:


Adjusted Analysis:


There was very little impact by school type by changing the 9th grade scores.

## Summary

1. The overall passing rate for Thomas High School changed dramatically from 91% to 65%.

2. Thomas High School's ranking dropped from 2nd to 8th in the district of 15 campuses.

3. Data at the grade level will now show as "NaN" in reports for the 9th grade students at Thomas High School

4. In addition to the overall passing rate, the campus math and reading averages and passing percentages all saw shifts.

The major changes will be seen at the lower views of the disaggregated data with minor impact to the larger data views.
