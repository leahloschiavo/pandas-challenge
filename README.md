 In this assignment I successfully created code to achieve the following results:

Total number of unique schools
Total students
Total budget
Average math score
Average reading score
% passing math 
% passing reading 
% overall passing 

School Summary
DataFrame that summarizes key metrics about each school.
School name
School type
Total students
Total school budget
Per student budget
Average math score
Average reading score
% passing math (the percentage of students who passed math)
% passing reading (the percentage of students who passed reading)
% overall passing (the percentage of students who passed math AND reading)
Highest-Performing Schools (by % Overall Passing)

Sort the schools by % Overall Passing in descending order and display the top 5 rows.
Save the results in a DataFrame called "top_schools".
Lowest-Performing Schools (by % Overall Passing)
Sort the schools by % Overall Passing in ascending order and display the top 5 rows.
Save the results in a DataFrame called "bottom_schools".

Math Scores by Grade:
Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.
Reading Scores by Grade:
Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

Scores by School Spending:
Create a table that breaks down school performance based on average spending ranges (per student).
Use the code provided below to create four bins with reasonable cutoff values to group school spending.
spending_bins = [0, 585, 630, 645, 680]
labels = ["<$585", "$585-630", "$630-645", "$645-680"]
Use pd.cut to categorize spending based on the bins.
Use the following code to then calculate mean scores per spending range.
spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Math Score"].mean()
spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Reading Score"].mean()
spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Math"].mean()
spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Reading"].mean()
overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Overall Passing"].mean()
Use the scores above to create a DataFrame called spending_summary.


Metrics-- put in table and sorted in bins:
Average math score/Average reading score
% passing math 
% passing reading 
% overall passing
Scores by School Size:
Use the following code to bin the per_school_summary.
size_bins = [0, 1000, 2000, 5000]
labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]
Use pd.cut on the "Total Students" column of the per_school_summary DataFrame.
Create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).
Scores by School Type
Use the per_school_summary DataFrame from the previous step to create a new DataFrame called type_summary.
This new DataFrame should show school performance based on the "School Type".


District Summary:
Calculate the total number of unique schools 
Calculate the total number of students
Calculate the total budget
Calculate the average math score
Calculate the average reading score 
Use the code provided to calculate the percentage of students who passed math 
Calculate the percentage of students who passed reading
Use the code provided to calculate the percentage of students that passed both math and reading 
Create a new DataFrame for the above calculations called district_summary 

School Summary:
Use the code provided to calculate the averages
Create the spending_summary DataFrame using the binned and averaged spending data
Scores by School Size 
Use pd.cut with the provided code to bin the data by the school sizes 
Use the code provided to calculate the averages 
Create the size_summary DataFrame using the binned and averaged size data 
Scores by School Type 
Group the per_school_summary DataFrame by "School Type" and average the results 
Use the code provided to select the new column data 
Create a new DataFrame called type_summary that uses the new column data 



Analysis:
One of the things I recognized with the data is that the budget for charter schools is much lower than district schools. In addition, the math and reading scores between the two differed as well. The charter schools had students who scored higher in reading and math. The charter schools were labled as smaller and the district schools were large for the most part.

Resources:
I used a Tutor (Jesse Wright) who helped me figure out the codes in the second section of the assignment. 
I used asked BCS for error questions
