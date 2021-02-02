# Employee Data Analysis

## Background
The purpose of this project is to perofrm Data Modeling, Data Engineering, and Data Analysis by designing tables from the given employee CSV datasets, import the CSV files in the SQL database, and write SQL to extract critical employee information.

The bel

## Requirements

#### **1.  Data Modeling**

* Determine the relationship of the given CSV datasets.

#### **2.  Data Engineering**

* Setup an employee database on PostgreSQL with the employee CSV dataset and link it based on the relationship found from Data Modeling.


#### **3.  Data Analysis**
 
 * Retreive the following employee information using SQL:
    * a.  List the following details of each employee: employee number, last name, first name, sex, and salary.
    * b.  List first name, last name, and hire date for employees who were hired in 1986.
    * c.  List the manager of each department with the following information: department number, department name, the manager's employee number, last name, first name.
    * d.  List the department of each employee with the following information: employee number, last name, first name, and department name.
    * e.  List first name, last name, and sex for employees whose first name is "Hercules" and last names begin with "B."
    * f.  List all employees in the Sales department, including their employee number, last name, first name, and department name.
    * g.  List all employees in the Sales and Development departments, including their employee number, last name, first name, and department name.
    * h.  In descending order, list the frequency count of employee last names, i.e., how many employees share each last name.
    
 * Retrive the following employee's salary information using SQL Alchemy and Matplotlib by:
    * a. Most Common Salary Ranges for Employees
    * b. Average Salary by Job Titles

![Image](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Output%20Files/ERD%20-%20Employee%20Database.png)

* The [Data Model](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Output%20Files/ERD%20-%20Employee%20Database.png) is saved in the output directory.
* Each box represents a table and its attributes (columns). 
* The data types are listed for each attribute.
* The key icon represents the primary keys uniquely identifies the records in each table.
* The line that connects to each table shows how the tables are related through common attirbutes.  
* The line also shows the type of relationship of the common attributes.  See the below image to determine the type relationship between the tables.

![Image](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Output%20Files/Relationship.png)

To conduct any data analysis, a data engineer must know what information the databases contain and how the attributes are related to one another. The perfect way is to map it out in a Entity Relationship Diagram (ERD) in  [http://www.quickdatabasediagrams.com]( http://www.quickdatabasediagrams.com).  See the below image to see how ERD of the Employee Databases.

    
## **2.  Data Engineering**

Based on the above Entity Relationship Diagram (ERD), a [table schema](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Table_Schema.sql) has been exported as a sql file to create the tables in PostgerSQL.

The table schema information is based on the six CSV files where all data types, primary keys, foreign keys, and other constraints are specified .

After running the table_schema.sql and creating the headings for each table for Postregres, we must import ach CSV file into the corresponding SQL table. 

**Note: Be sure to import the data in the same order that the tables were created and account for the headers when importing to avoid errors.**

The below table shows which table corresponds to which CSV file and the import should be run in the following order:

| SQL Table Name    | Corresponding CSV Table |
| ------------- | ------------- |
| "Departments"  | [departments.csv](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Resources/departments.csv)|
| "Titles"  | [titles.csv](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Resources/titles.csv)|
| "Employees"  | [employees.csv](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Resources/employees.csv)|
| "Salaries"  | [salaries.csv](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Resources/salaries.csv)|
| "Dept_Emp"  | [dept_emp.csv](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Resources/dept_emp.csv)|
| "Dept_Manager"  | [dept_manager.csv](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Resources/dept_manager.csv)|



## **3.  Data Analysis**

After completing the Data Modeling and Data Engineering steps, we have all the information to extract specific employee information from the databases. 

To conduct our Employee Data Analysis, a [queries file](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Queries.sql) has been created to retrieve the following employee information.

1.  List the following details of each employee: employee number, last name, first name, sex, and salary.

2.  List first name, last name, and hire date for employees who were hired in 1986.

3.  List the manager of each department with the following information: department number, department name, the manager's employee number, last name, first name.

4.  List the department of each employee with the following information: employee number, last name, first name, and department name.

5.  List first name, last name, and sex for employees whose first name is "Hercules" and last names begin with "B."

6.  List all employees in the Sales department, including their employee number, last name, first name, and department name.

7.  List all employees in the Sales and Development departments, including their employee number, last name, first name, and department name.

8.  In descending order, list the frequency count of employee last names, i.e., how many employees share each last name.

To see the results of the database, this can be run on PostgresSQL.

## **4.  Bonus**

Upon examining the data, I wanted to test the validity of the dataset to ensure it is accurate. To confirm this, the [Bonus file](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Bonus.ipynb) has been created to import the PostgreSQL database to Pandas Dataframes via SQL Alchemy.

Note: [gitignore](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/.gitignore) file has been created to ensure others do not have my personal access to my PostgreSQL.

The below visualizations are used to prove the validity of the employee data:

1.  [Historgram - Most Common Salary Ranges for Employees](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Output%20Files/Salary%20Ranges%20for%20Employees.png)

![Image](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Output%20Files/Salary%20Ranges%20for%20Employees.png)


2.  [Bar Chart - Average Salary by Title](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Output%20Files/Average%20Salary%20by%20Title.png)

![Image](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Output%20Files/Average%20Salary%20by%20Title.png)


## **5.  Folders and Directories**

The below folders have the following files:

| Folder Name    | File Name |
| ------------- | ------------- |
| Employee SQL  | [Table_Schema.sql](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Table_Schema.sql)  |
|               | [Queries.sql](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Queries.sql)  |
|               | [Bonus.ipynb](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Bonus.ipynb)  |
|               | [.gitignore](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/.gitignore)  |

Inside the Employee SQL Folder, there are the Ouput and Resources folders that stores the following files:

| Folder Name    | File Name |
| ------------- | ------------- |
| Output        | [ERD - Employee Database.png](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Output%20Files/ERD%20-%20Employee%20Database.png)  |
|               | [Salaries Ranges for Employees.png](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Output%20Files/Salary%20Ranges%20for%20Employees.png)  |
|               | [Average Salary by Title.png](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Output%20Files/Average%20Salary%20by%20Title.png)  |
|               | [Relationship.png](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Output%20Files/Relationship.png)  |
| Resources   | [departments.csv](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Resources/departments.csv)  |
|             | [dept_emp.csv](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Resources/dept_emp.csv)  |
|             | [dept_manager.csv](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Resources/dept_manager.csv)  |
|             | [employees.csv](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Resources/employees.csv)  |
|             | [salaries.csv](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Resources/salaries.csv)  |
|             | [titles.csv](https://github.com/cecileung1208/SQL-Employee-Data/blob/master/Employee_SQL/Resources/titles.csv)  |
