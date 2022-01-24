# School District Analysis
## Overview
The purpose of this project is to analyse School District information on standardized testing scores, student performance, school type, size and budget, in order to present data analysis to the School Board, which may help take decisions that may improve the overall school performances.
After a thorough analysis, the school board notified us evidence of academic dishonesty in the testing scores for the Thomas High School ninth grade students, so the original script code was modified in order to replace the supposedly altered grades, and the determine the impact on the final analysis.

The analysis presented here was made using Python v. 3.7.6, Pandas Lybrary and Jupyter Notebook interface.

## Results
After importing de csv files containing the information pertaining to the school information and student information, the same data cleaning was applied in order to have standardized values across the Data Frames.

Then, in the student data DataFrame, by using de loc method, all the grades for both math and reading tests, from the ninth grade students of the Thomas High School were replaced with NaN values, in order to be able to calculate again average grades and then passing percentages without taking into account the 9th grade students. An example of the corrected Dataframe is shown below.

![Dataframe Nan](https://user-images.githubusercontent.com/95982833/150715844-6225f762-cf17-486a-ace5-539be95f45a3.png)

Then the school district analysis was repeated, by modifying the previous code script, but with the new DataFrame merged into the school summary.
After this step, the 9th grade students from Thomas High School had to be substracted from the total student count, in order to calculate new averages and percentages. This was accomplished by repeating counts on the corrected student dataframe, in which the 9th grade students had no values in their grading scores. Then a simple substraction was made using ordinary arithmetic operators, as is shown in the image below.

![new student count](https://user-images.githubusercontent.com/95982833/150715868-05480fc0-fa50-48f9-8b89-a21fc14f36d5.png)



After comparing both district summaries, some changes must be noted:

 - The total schools, students and budget, obviously were unaltered.
 - A slight decrease in the average math score, from 79 to 78.9 was noted, translating into a 74.8% of students passing math (previous was 75%.
 - The average reading score remained unaltered (81.9), but the percentage of students passing the reading test decreased to 85.7% from 86%.
 - The overall passing percentage decreased from 65% to 64.9%.

![previous district summary](https://user-images.githubusercontent.com/95982833/150715893-28c2c461-2f38-49ee-a783-cf8002e0f806.png)

![new district summary](https://user-images.githubusercontent.com/95982833/150715905-c74b9351-481f-4a34-8b0a-8843a6aef8d6.png)

The most notable changes, afther replacing the 9th grade scores, were noted in the School Summary:

 - The average math score increased from 83.35 to 83.896.
 - The average reading score increased from 83.90 to 93.186.
 - The percentage of students passing the math test practically remained the same (93.1% to 93.19%).
 - The percentage of students passing the reading test dramatically increased from 69.66% to 97.3%.
 - The increase in the percentage of students passing the reading test impacted on the overall passing percentage of students, increasing from 65.08% to 90.63%.
 
![previous school summary](https://user-images.githubusercontent.com/95982833/150715923-8a813721-bb3d-40c5-ac83-5ed855f0b134.png)

![new school summary](https://user-images.githubusercontent.com/95982833/150715946-4a82282f-b50c-47ec-84e0-be677388128a.png)

The changes mentioned above, put Thomas High School among the top five schools in the district.

![new top five schools](https://user-images.githubusercontent.com/95982833/150715966-69bc5492-4085-4bb8-96aa-fdce69f99a5e.png)


The scores by grade analysis was not affected, as the 9th grade scores from Thomas High School were considered invalid, and do not impact the average per grade by school.

When the analysis of performance by spending, there was a minimal increase in the average scores of both math and reading, and their respective percentaged including the overall passing, however this increase is noted in the hundreths decimal position, which makes no significant change in the analysis after rounding up the numbers.

The same can be said about the analysis of performance vs. school size and school type.
## Summary
After repeating the analysis, updating the 9th grade scores, we can conclude that there was a notable impact on the average and percentage of students passing the reading test, which in turn dramatically increased the overall school performance, placing it in the top five schools of the district.
