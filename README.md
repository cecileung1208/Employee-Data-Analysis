# Employee Data Analysis

![Image](https://s27389.pcdn.co/wp-content/uploads/employee%20data-1000x440.jpg)

## Background
The purpose of this project is to perofrm Data Modeling, Data Engineering, and Data Analysis by designing tables from the given employee CSV datasets, import the CSV files in the SQL database, and write SQL to extract critical employee information.

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
    * d.  List the department of each employee with the following information: employee number, last name, first name, and depatment name.
    * e.  List first name, last name, and sex for employees whose first name is "Hercules" and last names begin with "B."
    * f.  List all employees in the Sales department, including their employee number, last name, first name, and department name.
    * g.  List all employees in the Sales and Development departments, including their employee number, last name, first name, and department name.
    * h.  In descending order, list the frequency count of employee last names, i.e., how many employees share each last name.
    
 * Retrive the following employee's salary information using SQL Alchemy and Matplotlib by:
    * a. Most Common Salary Ranges for Employees
    * b. Average Salary by Job Titles
    
## Datasets

* [departments.csv](https://github.com/cecileung1208/Employee-Data-Analysis/blob/master/Employee%20Data/departments.csv)
* [dept_emp.csv](https://github.com/cecileung1208/Employee-Data-Analysis/blob/master/Employee%20Data/dept_emp.csv)
* [dept_manager.csv](https://github.com/cecileung1208/Employee-Data-Analysis/blob/master/Employee%20Data/dept_manager.csv)
* [employees.csv](https://github.com/cecileung1208/Employee-Data-Analysis/blob/master/Employee%20Data/employees.csv)  
* [salaries.csv](https://github.com/cecileung1208/Employee-Data-Analysis/blob/master/Employee%20Data/salaries.csv)
* [titles.csv](https://github.com/cecileung1208/Employee-Data-Analysis/blob/master/Employee%20Data/titles.csv) 

    
    
## Method

#### **1.  Data Modeling**
* Create an Entity Relationship Diagram (ERD) using the online software ((http://www.quickdatabasediagrams.com/).
* Inspect the headings to determine comon attributes between each table.
* Determine the data types for each column.
* Determine parameters for primary and foreign keys.
* Link the relationship betwee tables with primary keys.
* Export to table schema for Data Engineering.

#### **2. Data Engineering**
* Create PostgreSQL database for employee data.
* Import the table schema on the database.
* Create tables and heading labels as per the ERD.
* Import employee CSV datasets in the respective tables created.


#### **3. Data Analysis** 
* Employee SQL:
  * Using SQL, query for the required information across the tables in the PostgreSQL database.
 
* Salary Information:
  * Establish connection between PostgreSQL database and Jupyter Notebook file.
  * Write SQL to extract relevant employee, job title and salary data and display the information into a Dataframe.
  * View dataframes to ensure common headings have the same name to perform the merge function.
  * Use the salary data to plot employee salary ranges in a Histogram.
  * Merge salary_data, title_data, and employee data.
  * Calculate the average salary by title.
  * Plot the averagy salary by title in a Bar Graph.
 
## Scripts
[Table Schema SQL](https://github.com/cecileung1208/Employee-Data-Analysis/tree/master/Data%20Engineering)
[SQL Queries](https://github.com/cecileung1208/Employee-Data-Analysis/blob/master/Data%20Analysis/Employee%20SQL/Queries.sql)
[Salary Analysis](https://github.com/cecileung1208/Employee-Data-Analysis/blob/master/Data%20Analysis/Salary%20Analysis/Salary_Analysis.ipynb)
 
  
## Results

#### **1.  Data Modeling**

![Image](https://github.com/cecileung1208/Employee-Data-Analysis/blob/master/Data%20Modeling/ERD%20-%20Employee%20Database.png)

#### **2.  Data Engineering**

![Image](https://github.com/cecileung1208/Employee-Data-Analysis/blob/master/Data%20Engineering/Table_Schema_Script.png)

Employee Database on PostgreSQL
![Image](https://github.com/cecileung1208/Employee-Data-Analysis/tree/master/Data%20Engineering)
![Image](https://github.com/cecileung1208/Employee-Data-Analysis/blob/master/Data%20Engineering/Table_Schema_PostgreSQL_Dependents.png)

#### **3.  Data Analysis**

The Employee SQL provided the following information about the company:
    * a.  There are 300,024 employees in the company.
    * b.  There are 36,150 employees hired during 1986.
    * c.  There are 24 managers across 9 departments.
    * d.  The companies have almost 65% of them employees, in the Development, Production and Sales department.
    * e.  There are 20 employees where their first name is "Hercules" and their last name begins with "B".
    * f.  There are 52,245 employees in the Sales Department.
    * g.  There are 137,952 employees in the Sales and Development Departments.
    * h.  Many employees share the same last name with 226 employees having the last name "Baba".
 CSV Outputs can be retrieved in this [folder](https://github.com/cecileung1208/Employee-Data-Analysis/tree/master/Data%20Analysis/Employee%20SQL).
    
The Salary Analysis provided the following information about the company:
    * The average salary for the employees is $52,970.73
    
    ![Image](https://github.com/cecileung1208/Employee-Data-Analysis/blob/master/Data%20Analysis/Salary%20Analysis/Salary%20Ranges%20for%20Employees.png)
    
    * The staff and the senior staff have the highest salaries in the company.
    
    ![Image](https://github.com/cecileung1208/Employee-Data-Analysis/blob/master/Data%20Analysis/Salary%20Analysis/Average%20Salary%20by%20Title.png)
    
