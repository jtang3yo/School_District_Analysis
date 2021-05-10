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
** 1. Merge the school_data_df and student_data_df into school_data_complete_df with replaced math and reading scores of Thomas High School 9th grade as NaNs. 

** 2. Repeat the school district analysis you did in this module, and recreate the following metrics

*** 1). The district summary: 
a. declare variables for school_count, student_count, total_budget, average_math_scores, average_reading_scores, and egt the number of students that are in ninth grade at Thomas High School. These students have no grades. Subtract the number of students that are in ninth grade at Thomas High School from the total student count to get the new total student count. 
  THS 9th Grade student count![image](https://user-images.githubusercontent.com/82353749/117671659-08b16480-b177-11eb-870e-8658b1369c81.png)
b. Get passing math, reading and overall passing rate based on the new total student count. 
  calculation based on new total student count ![image](https://user-images.githubusercontent.com/82353749/117671880-46ae8880-b177-11eb-8613-48edc8f965f2.png)
c. Create a new district_summary_df 
  District_summary_df![image](https://user-images.githubusercontent.com/82353749/117672424-d6eccd80-b177-11eb-9bf8-6cc9c5568a80.png)
  
*** 2) The school summary: 
a. Declare variables by using school_data_complete_df, student_data_df, and school_data_df to calculate per school data. 
b. Create a new per_school_summary_df 
  Create per_school_summary and format ![image](https://user-images.githubusercontent.com/82353749/117673183-8d50b280-b178-11eb-9aff-4bf8222015c4.png)
c. Final output of per_school_summary_df with updated passing rate of THS 
  Per_school_summary_df ![image](https://user-images.githubusercontent.com/82353749/117673481-d4d73e80-b178-11eb-9264-ede9aa201b43.png)
  
*** 3) The top 5 and bottom 5 performing schools, based on the overall passing rate 
a. In order to compare the impact of dishonest grades of THS 9th grade, need to recalculate the passing rate of THS using 10-12th grade student count. 
  THS 10-12TH grade count ![image](https://user-images.githubusercontent.com/82353749/117674309-8f674100-b179-11eb-9245-a83a0fe92d75.png)
  THS 10-12TH grade passing rate.jpg![image](https://user-images.githubusercontent.com/82353749/117677529-89bf2a80-b17c-11eb-84d3-1441582126cb.png)
  Replace the passing rate of THS with new THS 10-12th grade via loc() method: 
  Replace THS passing rate ![image](https://user-images.githubusercontent.com/82353749/117675418-89259480-b17a-11eb-9165-abd221963e5d.png)
b. Get top 5 schools with updated data of THS: Top five school_new ![image](https://user-images.githubusercontent.com/82353749/117675684-c9851280-b17a-11eb-9950-5bd4cbb2053c.png)

*** 4) The average math score for each grade level from each school
a. Create Series of each grader and use groupby() to calculate the average passing math rate of each grader 
b. Average passing math by grader ![image](https://user-images.githubusercontent.com/82353749/117676109-3f897980-b17b-11eb-9f01-fe702a298d99.png)

*** 5) The average reading score for each grade level from each school
a. Refactor the code to get average passing reading rate of each grader 
b. Average passing reading by grader![image](https://user-images.githubusercontent.com/82353749/117676433-8a0af600-b17b-11eb-897a-e672f20768f0.png)
c. Output of average passing reading by grader ![image](https://user-images.githubusercontent.com/82353749/117676621-b6267700-b17b-11eb-9cc0-df43174a93ff.png)

*** 6) The scores by school spending per student
a. Establish spending bins 
  Establish the spending bins ![image](https://user-images.githubusercontent.com/82353749/117683112-bde91a00-b181-11eb-853b-f2eec0f415d0.png)
b. Groupby the spending ranges and calculate the average of math and reading scores 
  Scores by school spending per student: Per student![image](https://user-images.githubusercontent.com/82353749/117683319-f4269980-b181-11eb-9f2a-7ed38c4aff0f.png)
c. Spending range per student output![image](https://user-images.githubusercontent.com/82353749/117683768-64351f80-b182-11eb-8368-c3bcc0a9960c.png)

*** 7) The scores by school spending by school size
a. Establish the bins on school size 
  School size bins ![image](https://user-images.githubusercontent.com/82353749/117684061-a199ad00-b182-11eb-9d47-99d3345e6233.png)
b. Groupby the school size and calculate the average math and reading scores 
  School size average scores ![image](https://user-images.githubusercontent.com/82353749/117684608-27b5f380-b183-11eb-8658-519fc7f2c8b8.png)
c. Final output of size_summary_df: size_summary_df output ![image](https://user-images.githubusercontent.com/82353749/117684832-5e8c0980-b183-11eb-8ca5-fb3e02303d6d.png)

*** 8) The scores by school spending by school type
a. Groupby school type for average scores Calculate averages for the math and reading score columns via mean()
  school type average scores ![image](https://user-images.githubusercontent.com/82353749/117685517-00abf180-b184-11eb-98f0-95c4cb0c38b7.png)
b. Type_summary_df output: Type_summary_df output ![image](https://user-images.githubusercontent.com/82353749/117685716-2cc77280-b184-11eb-99ee-ab336c13f425.png)

## Summary 
### How is the district summary affected? 
1. Compare with the original district_summary_df, the average math and reading did not change much, and there is slightly drop from 65% to 64.9% on overall passing rate in the updated district_summary_df. 
2. Original district_summary_df![image](https://user-images.githubusercontent.com/82353749/117687701-07d3ff00-b186-11eb-9178-80bac04e4f3f.png)
   Updated district_summary_df![image](https://user-images.githubusercontent.com/82353749/117687201-8da37a80-b185-11eb-8982-ecff871a0735.png)

### How is the school summary affected? How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
1. Compare with the original top five shcools, the overall passing rate has dropped slightly from 90.95% to 90.63% after subtract 9th grade scores. Thomas High School still ranks No.2. 
2. Original top 5 schools![image](https://user-images.githubusercontent.com/82353749/117689241-8bdab680-b187-11eb-89aa-92dfc2ee3230.png)
   Top five school_new ![image](https://user-images.githubusercontent.com/82353749/117689335-9eed8680-b187-11eb-87d0-65e276ebb373.png)
3. However, prior to replace THS's overall passing with only 10-12th grades, THS's overall passing rate was 65.08%. 
   THS 9th NaNs ![image](https://user-images.githubusercontent.com/82353749/117689797-1de2bf00-b188-11eb-8e7c-9d6e0535fe7f.png)
   
### How does replacing the ninth-grade scores affect the following: Since the 9th Grade's scores have been replaced with NaN, but later on, THS's math and reading scores have been replaced with only taking consideration into 10th - 12th grades, so the passing rates of THS renders slight difference compare to the original THS passing rates data. Accordingly, with the insignificant change on THS passing rates, the results remain the same for the following. 
  1) Original THS ![image](https://user-images.githubusercontent.com/82353749/117693554-263cf900-b18c-11eb-94e5-5e14c8e98c1e.png)
  2) Updated THS ![image](https://user-images.githubusercontent.com/82353749/117693588-2f2dca80-b18c-11eb-9288-3e74bfe20fb5.png)
1. Math and reading scores by grade: 
  1) Original math and reading by grades ![image](https://user-images.githubusercontent.com/82353749/117694477-30abc280-b18d-11eb-96c2-b11824aeef4b.png)
  2) Updated math and reading by grades ![image](https://user-images.githubusercontent.com/82353749/117694690-6cdf2300-b18d-11eb-8688-c2c04597a342.png)
2. Scores by school spending
  1) Original by spending![image](https://user-images.githubusercontent.com/82353749/117695291-145c5580-b18e-11eb-8e20-59daf8ab8967.png)
  2) Updated by spending![image](https://user-images.githubusercontent.com/82353749/117695324-1d4d2700-b18e-11eb-8bac-8911a75c0427.png)
3. Scores by school size
  1) Original by size ![image](https://user-images.githubusercontent.com/82353749/117695482-466db780-b18e-11eb-8573-256f160e7968.png)
  2) Updated by size ![image](https://user-images.githubusercontent.com/82353749/117695870-b2502000-b18e-11eb-856c-edc9ec616d28.png)
4. Scores by school type
  1) Original by type ![image](https://user-images.githubusercontent.com/82353749/117696131-f93e1580-b18e-11eb-81a3-d246cf5f8119.png)
  2) Updated by type ![image](https://user-images.githubusercontent.com/82353749/117696017-d90e5680-b18e-11eb-92bc-21253a2c1df7.png)




  
   



