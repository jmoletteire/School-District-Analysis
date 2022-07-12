# School District Analysis
## Overview
Following a case of academic dishonesty, altered grades for a ninth grade class and re-analyzed student performance among a set of high schools based on a variety of metrics such as school type, budget, and size using Jupyter Notebooks and Pandas.

## Results
The results below were collected from a fifteen-school district before and after nullifying grades for all 9th graders at Thomas High School.
### District Summary
* Before Removing Grades
  ![Module](/Resources/Screenshots/Summary.png)
* After Removing Grades
  ![Challenge](/Resources/Screenshots/Summary_Challenge.png)
##### Analysis
* The district-wide summary (displayed above) was largely unaffected by the nullification of Thomas High's ninth grade data, as no other schools had any student grades altered. Thus, only Thomas High School shows any difference between dataframes, and given this is a case of academic dishonesty, it makes sense that after removing the grades of the cheating students, most of Thomas's numbers fell.
* Curiously though, THS's Average Reading Score actually increased when the ninth grade was not counted. This could indicate that only a small number of freshman actually cheated, or that there was only cheating in math, since the class as a whole seems to be weighing the rest of the school down in reading.
  * Thomas did have a higher percentage of students passing reading before removing ninth graders, so perhaps the cheating brought student scores up to passing (>= 70), but still below average.

### School Summary
    
* Thomas High School's Performance
    * Top 5 Schools (Before)
    ![Module](/Resources/Screenshots/TopFiveSchools.png)
    * Top 5 Schools (After)
    ![Challenge](/Resources/Screenshots/TopFiveSchools_Challenge.png)
##### Analysis
* While Thomas High School saw a minor dip in its Overall Passing Percentage (from 90.95% to 90.63%) after excluding the freshman class, this decline did not have any effect on the top 5 schools in the district (by Overall Pass Percentage). Thomas High remains sandwiched between Cabrera and Griffin High Schools, placing second. 

### Breakdown
* Scores by School Spending
  * Before Removing Grades
  ![Module](/Resources/Screenshots/SpendingSummary.png)
  * After Removing Grades
  ![Challenge](/Resources/Screenshots/SpendingSummary_Challenge.png)


* Scores by School Size
  * Before
  ![Module](/Resources/Screenshots/SizeSummary.png)
  * After
  ![Challenge](/Resources/Screenshots/SizeSummary_Challenge.png)


* Scores by School Type
  * Before
  ![Module](/Resources/Screenshots/TypeSummary.png)
  * After
  ![Challenge](/Resources/Screenshots/TypeSummary_Challenge.png)

##### Analysis
* There is, noticeably, a lack of change in all three categories before and after removing the scores for Thomas High ninth graders. I postulate that the nullification of the scores (as opposed to setting them to zero), as well as the small size of the Thomas High freshman class relative to the total number of students in the district, can explain this observation.
* As far as the nullification of the scores, the explanation is fairly simple. Had we given Thomas High's ninth graders zeroes for math and reading it would have greatly skewed the data. Even in a set of roughly 37,000, a few hundred zeroes would cause a bit of a disturbance (in both math and reading) because of how greatly those scores would deviate from the mean. But, by removing the ninth graders from the calculation entirely, we've simply limited the population, and only slightly, as removing a few hundred data points is less consequential than creating a few hundred outliers. As such, we should expect the new data (from a pop. of ~36,000) to nearly mirror the old data (from a pop. of ~37,000), as it does.
* An additional explanation could be rounding. Had we not rounded to a single decimal place, or to the nearest whole number, there may have been a more observable difference in the data.

## Summary
In brief, the most notable observations here are:
1. Without the ninth grade, Thomas High School saw a decrease in its Avg. Math Score, and Percent Passing Math, Reading, and Overall.
2. Thomas High School's Average Reading Score increased without the ninth grade, suggesting that cheating may have been quite isolated among students, cheating may have only been in math, and/or that cheating brought students to passing grades but still left them below average.
3. The top 5 schools in the district (by Overall Pass %) are the same, even after a slight decrease in Thomas High's Overall Passing Percentage.
4. There was no change in any of the scores when grouping schools by spending, size, or type, before and after removing the THS freshman class. This may be because it was a small group who therefore had little impact on district-wide averages, especially when rounded to the nearest whole number.