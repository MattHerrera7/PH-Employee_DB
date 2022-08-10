# Detailed Instructions From Your Instructor Team

The objective of this challenge is for you to create (additional) two intermediate tables and a final table that contains the total number of employees by title that will be retiring based on your birth date. You'll also create a table that of employees who are still employed and born withing a certain year that are eligible to participate in a mentorship program. Finally, you will write a report on the results of the analysis.

## Deliverable 1: The number of retiring employees by title

For the first deliverable, we are asking you to create three tables.

* For the first table, you'll need to retrieve the `emp_no`, `first_name` and `last_name` columns from the employees table employees, and the the `title`, `from_date` and `to_date` columns from the titles table. you'll need to join the two tables on the primary key and then filter the data for those employees born between January 1, 1952 and December 31, 1955. The data should be saved as a new table, and exported as `retirement_titles.csv` into the Data folder of your Pewlett-Hackard-Analysis folder.

* The retirement titles table will have duplicate entries for some employees because you have switched titles over the years. These duplicate entries will be handled in the next table.

![The retirement table with employee number, first name, last name, title, the title from and to dates, and ordered by employee number.](retirement_titles.png)

* For the second table, we have provided [starter code](Employee_Challenge_starter_code.sql) that you should download, copy and paste into your `Employee_Challenge_starter_code.sql` file. Using this starter code, you will need to retrieve the `emp_no`, `first_name`, `last_name` and `title` columns from the retirement titles table you just created.

* Using the the `DISTINCT ON` statement you should get the first occurrence of the employee number in the `ON ()` clause for each set of rows.  We have provided a hint that links to documentation on how to use the `DISTINCT ON` statement.

* The data should be filtered on `to_date` to keep only those dates that are equal to `'9999-01-01'`, then sorted in ascending order by the employee number. Lastly, data should be saved as a new table, and exported as `unique_titles.csv` into the Data folder of your Pewlett-Hackard-Analysis folder.

![The unique titles table sorted by employee number and the recent title date in descending order.](unique_titles.png)

* For the final table, you will have to retrieve the number of employees by recent job title who are about to retire.

* To get the number of employees by job title you will need to retrieve the number of titles from unique titles table. Then the data should be grouped by titles and sorted by the number of titles in descending order, and added to a new table, then exported as `retiring_titles.csv` into the Data folder of your Pewlett-Hackard-Analysis folder.

![The retiring title table ordered by title and sorted by count in descending order.](retiring_titles.png)

## Deliverable 2: The eligible employees for the mentorship program

For the second deliverable, you will need to create a mentorship eligibility table that holds the employees who are currently employed and born between January 1, 1965 and December 31, 1965.

* For this table, you'll need to retrieve the `emp_no`, `first_name`, `last_name`, and `birth_date` columns from the employees table, the `from_date` and `to_date` columns from the department employee table, and the `title` column from the titles table. you'll also have to use the the `DISTINCT ON` statement to get the first occurrence of the employee number in the `ON ()` clause for each set of rows.

* Next, you'll need to perform two `INNER JOIN` statements. The first will join the employees and the department employee tables on the primary key, and the second will join the employees and the titles tables on the primary key. Then, you'll need to filter the data on the `to_date` column to get current employees, and where your birth dates are between January 1, 1965 and December 31, 1965. Finally, you'll need to order the table by the employee number, and add the data to a new table, export the table as `mentorship_eligibilty.csv` into the Data folder of your Pewlett-Hackard-Analysis folder.

![The mentorship table with the employee number, first and last name, birth date, from and to date for the current title, ordered by employee number.](mentoring_titles.png)

## Deliverable 3: A written report for the employee database analysis

Again, the goal of the writing assignment is for you to present your findings in a logical manner. As a reminder, you should use appropriate grammar and structure when writing.

For the written analysis, you should use the repository README.md to write your report. The report will contain three sections: an overview of the analysis, results, and summary.

**Overview of the analysis:** Explain the purpose of this analysis.

**Results:** Provide a bulleted list with four major points from the retirement titles and the mentorship eligibility tables. Use images if necessary to support your evidence.

**Summary:** Provide a high-level summary that addresses the following questions, and then provide two additional queries or tables that can be created that will provide more insight for the upcoming "silver tsunami".
  * How many roles will need to be filled as the "silver tsunami" begins to make an impact?
  * Are there enough retirement-ready employees in the departments that are qualified to mentor the next generation of Pewlett Hackard employees?

The README.md document should be in the home directory of your repository. All links should be working, and images and code should be formatted and displayed where appropriate.

## Grading Rubric

The [Employee Database Grading Rubric](Module_7_Challenge_Grading_Rubric.pdf) is provided for you to use when grading you' submissions.
