# School_District_Analysis
## Overview of the School District Analysis project 
### Background 
The school board has notified Maria and her supervisor that the students_complete.csv file shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. Although the school board does not know the full extent of the academic dishonesty, they want to uphold state-testing standards and have turned to Maria for help. She has asked you to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. Once you’ve replaced the math and reading scores, Maria would like you to repeat the school district analysis that you did in this module and write up a report to describe how these changes affected the overall analysis.
### Purpose 
Refactoring the the code to get the new district and school summary, and compare with the original dataframe to see how much it has impacted the summaries without dishonest math and reading scores. 
## Analysis 
* Deliverable 1 
** 1. Use the loc method on the student_data_df to select all the reading scores from the 9th grade at Thomas High School and replace 
In order to exclude dishonest scores of questionable grade at Thomas High School, applied the loc() method within student_data_df to replace the scores with NaN. 
Replacing reading score with NaN![image](https://user-images.githubusercontent.com/82353749/117590993-0fe95b80-b100-11eb-88c2-3a84c119d93a.png)
** 2. Refactor the code to replace all 9th Grade math scores with NaN 
Math scores replaced with NaN![image](https://user-images.githubusercontent.com/82353749/117591040-6b1b4e00-b100-11eb-838f-95c443f7e0e0.png)
** 3. The student_data_df has been refactored and checked the student data for NaNs 
Check for NaNs in student_data_df![image](https://user-images.githubusercontent.com/82353749/117591290-e0d3e980-b101-11eb-99de-af061e08903b.png)

* Deliverable 2 
** 1. 
