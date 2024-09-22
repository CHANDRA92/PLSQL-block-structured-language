## For Table Demo use In this code 
```plsql
-- Create the employees table
CREATE TABLE employees (
    employee_id NUMBER(5) PRIMARY KEY,
    first_name VARCHAR2(50),
    last_name VARCHAR2(50),
    salary NUMBER(8, 2),
    department_id NUMBER(5)
);

-- Insert some dummy data into the employees table
INSERT INTO employees (employee_id, first_name, last_name, salary, department_id) VALUES (100, 'John', 'Doe', 5000, 10);
INSERT INTO employees (employee_id, first_name, last_name, salary, department_id) VALUES (101, 'Jane', 'Smith', 6000, 20);
INSERT INTO employees (employee_id, first_name, last_name, salary, department_id) VALUES (102, 'Alice', 'Johnson', 5500, 30);
INSERT INTO employees (employee_id, first_name, last_name, salary, department_id) VALUES (103, 'Bob', 'Williams', 7000, 10);
INSERT INTO employees (employee_id, first_name, last_name, salary, department_id) VALUES (104, 'Michael', 'Brown', 8000, 20);

-- Commit the changes
COMMIT;

```

```plsql
SET SERVEROUTPUT ON;
DECLARE 
	v_salary NUMBER(8);
BEGIN 
	SELECT salary INTO v_salary FROM employees
    WHERE employee_id = 100;
    DBMS_OUTPUT.PUT_LINE(v_salary);
END;
/

DECLARE 
	v_salary NUMBER(8);
    v_fname VARCHAR2(20);
BEGIN
	SELECT salary,first_name INTO v_salary, v_fname FROM employees
    WHERE employee_id = 100;
    DBMS_output.PUT_LINE(v_fname ||' Has Salary ' || v_salary);
END;
```
