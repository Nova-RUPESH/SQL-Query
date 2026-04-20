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
(102, 'Sita Karki', 'Developer', 60000, 2);<br>
