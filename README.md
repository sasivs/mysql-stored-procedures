# mysql-stored-procedures
-- create schema
CREATE SCHEMA stored_proc_tutorial;
 
-- table creation
CREATE TABLE studentMarks (stud_id SMALLINT(5) NOT NULL AUTO_INCREMENT PRIMARY KEY, total_marks INT, grade VARCHAR(5));
 
 
-- insert sample data
INSERT INTO studentMarks(total_marks, grade) VALUES(450, 'A'), (480, 'A+'), (490, 'A++'), (440, 'B+'),(400, 'C+'),(380,'C')
,(250, 'D'),(200,'E'),(100,'F'),(150,'F'),(220, 'E');

1.create a stored procedure to fetch the details of students with the student ID being passed as an input parameter.

2. create a stored procedure to fetch the details of students having certain grade with the grade being passed as an input parameter.

3. create a stored procedure to calculate the average marks of all the students from the studentMarks table and return the average as an OUT field.

4. create a stored procedure to fetch the minimum mark corresponding to a grade with the grade being passed as an input parameter and return the minimum mark as an OUT field.

5. Create a stored procedure that takes an initial value of the counter and increment it with a given number.

6. create a stored procedure that takes a studentID as a input parameter and increments  the marks of the student by a given number as INOUT parameter.The final marks of the student must be stored in the INOUT paramaeter.

7. create a stored procedure  to find the count of students who is having marks below the average marks of all the students.

8. Write a nested stored procedure to find If a student marks are above average – then the result would be PASS else – FAIL.

9. Write a stored procedure to take studentId and depending on the studentMarks you 
need to return the class according to the below criteria.
Marks >= 400 : Class – First Class
Marks >= 300 and Marks < 400 – Second Class
Marks < 300 – Failed

10. Create a procedure that would insert a record in the studentMarks table and have IN parameters as studentId, total_marks, and grade. Also add an OUT parameter named rowCount which would return the total count of records in the studentMarks table.
Add the Error Handler for Duplicate Key record i.e. if someone invokes it for inserting a record with an existing studentID, then the Error handler would be invoked and will return an appropriate error.(Try both the “action” options namely: “CONTINUE” and “EXIT”)

Note : syntax for declaring error handler is:
             DECLARE {action} HANDLER FOR {condition} {statement}
