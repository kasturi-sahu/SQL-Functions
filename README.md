# SQL
JDA Programme at Npower

## SQL Activity (Book Table)
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# SQL Functions
## Aggregate Functions
Query A1: Enter a function that calculates the total cost of all animal rescues in the PETRESCUE table.

Query A2: Enter a function that displays the total cost of all animal rescues in the PETRESCUE table in a column called SUM_OF_COST.

Query A3: Enter a function that displays the maximum quantity of animals rescued.

Query A4: Enter a function that displays the average cost of animals rescued.

Query A5: Enter a function that displays the average cost of rescuing a dog.

## Scalar and String Functions
Query B1: Enter a function that displays the rounded cost of each rescue.

Query B2: Enter a function that displays the length of each animal name.

Query B3: Enter a function that displays the animal name in each rescue in uppercase.

Query B4: Enter a function that displays the animal name in each rescue in uppercase without duplications.

Query B5: Enter a query that displays all the columns from the PETRESCUE table, where the animal(s) rescued are cats. Use cat in lower case in the query.

## Date and Time Functions
Query C1: Enter a function that displays the day of the month when cats have been rescued.

Query C2: Enter a function that displays the number of rescues on the 5th month.

Query C3: Enter a function that displays the number of rescues on the 14th day of the month.

Query C4: Animals rescued should see the vet within three days of arrivals. Enter a function that displays the third day from each rescue.

Query C5: Enter a function that displays the length of time the animals have been rescued; the difference between today’s date and the rescue date.

# Sub-Queries and Nested Select

1. Execute a failing query (i.e. one which gives an error) to retrieve all employees records whose salary is lower than the average salary.
2. Execute a working query using a sub-select to retrieve all employees records whose salary is lower than the average salary.
3. Execute a failing query (i.e. one which gives an error) to retrieve all employees records with EMP_ID, SALARY and maximum salary as MAX_SALARY in every row.
4. Execute a Column Expression that retrieves all employees records with EMP_ID, SALARY and maximum salary as MAX_SALARY in every row.
5. Execute a Table Expression for the EMPLOYEES table that excludes columns with sensitive employee data (i.e. does not include columns: SSN, B_DATE, SEX, ADDRESS, SALARY).
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Working with Multiple Tables
How does an Implicit version of CROSS JOIN (also known as Cartesian Join) statement syntax look?
SELECT column_name(s)
FROM table1, table2;

How does an Implicit version of INNER JOIN statement syntax look?
SELECT column_name(s)
FROM table1, table2
WHERE table1.column_name = table2.column_name;

# Accessing Multiple Tables with Implicit Joins
1. Perform an implicit cartesian/cross join between EMPLOYEES and JOBS tables.

select * from EMPLOYEES, JOBS;
2. Retrieve only the EMPLOYEES records that correspond to jobs in the JOBS table.

select * from EMPLOYEES, JOBS where EMPLOYEES.JOB_ID = JOBS.JOB_IDENT;
3. Redo the previous query, using shorter aliases for table names.

select * from EMPLOYEES E, JOBS J where E.JOB_ID = J.JOB_IDENT;
4. Redo the previous query, but retrieve only the Employee ID, Employee Name and Job Title.

select EMP_ID,F_NAME,L_NAME, JOB_TITLE from EMPLOYEES E, JOBS J where E.JOB_ID = J.JOB_IDENT;
5. Redo the previous query, but specify the fully qualified column names with aliases in the SELECT clause.

select E.EMP_ID,E.F_NAME,E.L_NAME, J.JOB_TITLE from EMPLOYEES E, JOBS  J where 

# Accessing Multiple Tables with Sub-Queries
1. Retrieve only the EMPLOYEES records that correspond to jobs in the JOBS table.

select * from EMPLOYEES where JOB_ID IN (select JOB_IDENT from JOBS);
2. Retrieve only the list of employees whose JOB_TITLE is Jr. Designer.

select * from EMPLOYEES where JOB_ID IN (select JOB_IDENT from JOBS where JOB_TITLE= 'Jr. Designer');
3. Retrieve JOB information and who earn more than $70,000.

select JOB_TITLE, MIN_SALARY,MAX_SALARY,JOB_IDENT from JOBS where JOB_IDENT IN (select JOB_ID from EMPLOYEES where SALARY > 70000 );
4. Retrieve JOB information and list of employees whose birth year is after 1976.

select JOB_TITLE, MIN_SALARY,MAX_SALARY,JOB_IDENT from JOBS where JOB_IDENT IN (select JOB_ID from EMPLOYEES where YEAR(B_DATE)>1976 );
5. Retrieve JOB information and list of female employees whose birth year is after 1976.

select JOB_TITLE, MIN_SALARY,MAX_SALARY,JOB_IDENT from JOBS  where JOB_I

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Create & Access SQLite database using Python

## Objectives

After completing this lab you will be able to:

*   Create a database
*   Create a table
*   Insert data into the table
*   Query data from the table
*   Retrieve the result set into a pandas dataframe
*   Close the database connection
  
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Connect to Db2 database on Cloud using Python

## Objectives

After completing this lab you will be able to:

* Import the ibm_db Python library
* Enter the database connection credentials
* Create the database connection
* Close the database connection

