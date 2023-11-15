# Example of work

The main task is to write a function get_classification() to find out every LSE student's classification of an award based on the records of 3 years of study of a given student. 


Resit rule:

Students can have three attempts to pass the courses they take in their first year and two attempts to pass the courses they take in their second and third year
If a course is failed and re-taken, while the original fail mark and the new mark achieved will be recorded, a maximum mark of 40 and the grade will be capped at "Pass" when calculating the classification
Given the mark of a course, the corresponding "grade" can be determined based on the table below:

Grade	Mark
First Class Honours	70-100
Upper Second Class Honours	60-69
Lower Second Class Honours	50-59
Third Class Honours	40-49
Fail	0-39
And if it is a retake, the grade is capped as "Pass".

The course mark of a half-unit course is considered as one mark. The course mark of a full-unit course is counted as two marks

"First year average" is calculated as the average of the best 6 out of 9 first-year marks (including LSE100)

If a course is failed and re-taken, a maximum mark of 40 is capped when calculating the average
A full-unit mark will be counted twice
The classification of each student is based on 18 classification marks, comprised of:

"First year average" as 2 marks
8 marks from the second year
8 marks from the third year
The mark from the last attempt should be used

"Aggregate" of each student is the sum of the 18 classification marks

Degree classification rule (before the penalty rule):

First class honours:
At least 10 first class marks, or
8-9 first class marks and an aggregate of at least 1180
Upper second class honours:
At least 10 upper second class marks or above, or
8-9 upper second class marks or above, and an aggregate of at least 1030
Lower second class honours:
At least 10 lower second class marks or above, or
8-9 lower second class marks or above, and an aggregate of at least 880
Third class honours:
16 third class marks (or above)
Fail
None of the above fulfilled

Instructions
1. Write the function definition for the function get_course_grade(). It takes the mark of a course (int, between 0 and 100) as the first argument and an int (1, 2 or 3) as the second argument representing whether the mark is for attempts 1, 2 or 3. The function returns the corresponding grade of the course (str. Possible values: 'First Class Honours', 'Upper Second Class Honours', 'Lower Second Class Honours', 'Third Class Honours', 'Pass', 'Fail') based on the rules above

2. Ensure the function get_course_grade() works as intended by testing the function in src/test_lse_classification.py

3. In src/lse_classification.py, write the function definition get_first_year_average_simplified(). It takes 9 first-year marks (list of int with length 9, each integer between 0 and 100) as the argument and it returns the corresponding rounded "first-year average" (int between 0 and 100), which is the average of the highest 6 first year marks.

4. Ensure the function get_first_year_average_simplified() works as intended by testing the function in src/test_lse_classification.py

5. In src/lse_classification.py, write the function definition get_classification_simple(). It takes 2 arguments, with the first argument is for all classification marks (list of int with length 18, each integer between 0 and 100) and the second argument is for all classification grades (list of str with length 18. Possible values of the strings: 'First Class Honours', 'Upper Second Class Honours', 'Lower Second Class Honours', 'Third Class Honours', 'Pass', 'Fail'). It returns the corresponding final classification of the student ('First Class Honours', 'Upper Second Class Honours', 'Lower Second Class Honours', 'Third Class Honours', 'Fail')

6. Ensure the function get_classification_simple() works as intended by testing the function in src/test_lse_classification.py
