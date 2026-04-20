# SQL-Query
Basic Query to Create and Insert Table with Values<br><br>

-- Create Department table<br><br>
CREATE TABLE Department (<br>
    dept_id INT PRIMARY KEY,<br>
    dept_name VARCHAR(100) NOT NULL,<br>
    location VARCHAR(100)<br>
);<br><br>

-- Create Employee table<br><br>
CREATE TABLE Employee (<br>
    emp_id INT PRIMARY KEY,<br>
    emp_name VARCHAR(100) NOT NULL,<br>
    job_title VARCHAR(100),<br>
    salary DECIMAL(10,2),<br>
    dept_id INT,<br>
    FOREIGN KEY (dept_id) REFERENCES Department(dept_id)<br>
);<br><br>

-- Insert into Department <br><br>
INSERT INTO Department (dept_id, dept_name, location)<br>
VALUES
(1, 'HR', 'Kathmandu'),<br>
(2, 'IT', 'Pokhara');<br><br>

-- Insert into Employee<br><br>
INSERT INTO Employee (emp_id, emp_name, job_title, salary, dept_id)<br>
VALUES
(101, 'Ram Sharma', 'Manager', 50000, 1),<br>
(102, 'Sita Karki', 'Developer', 60000, 2);<br><br>


--Using Join Statement<br><br>
SELECT e.emp_name, d.dept_name, e.salary<br>
FROM Employee e<br>
INNER JOIN Department d<br>
ON e.dept_id = d.dept_id<br>
WHERE e.salary > 50000;<br><br>

--Updating Statement<br><br>
UPDATE Employee<br>
SET salary = salary + 5000<br>
WHERE dept_id = 2;<br><br>

--Deletion Statement<br><br>
DELETE FROM Employee<br>
WHERE emp_id = 101;<br><br>


DELETE FROM Employee<br>
WHERE emp_name LIKE 'R%';<br><br>

--Display Statement<br><br>
SELECT *<br>
FROM Department<br>
WHERE dept_name = 'IT';<br><br>

--To delete table completely<br><br>
DROP TABLE Employee;<br>






















