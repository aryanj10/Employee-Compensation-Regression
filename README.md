# Employee Compensation Estimator


Employee compensation involves all the ways your organization gives back to team members for their hard work. The obvious form of compensation is pay, whether it’s salaried, hourly, or sales-based. It’s important that how much an organization financially compensates an employee is fair, especially in terms of balancing the job role itself and the organization’s budget.

 

The salary or compensation to be paid to an employee of an organization depends on various factors like the organization group, department, job, salaries, etc. of the employee.

 

 

## Problem Statement
Imagine you are working as a data scientist in a big organization which has thousands of employees. The HR department is planning to provide some additional compensation to each working employee which needs to be calculated by looking at the profile of each employee and the benefits they are getting.

 

The HR department asks your help if you can use your data science and machine learning skills and calculate an estimated ‘Total Compensation’ for each employee.

## Objective
To build a machine learning model to estimate the total compensation to be provided to an employee.

## Code and Resources Used 
**Python Version:** 3.7  
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn, xgboost, lightgbm  
**Data Source:** City and County of San Francisco  
**Data Link:** https://data.sfgov.org/City-Management-and-Ethics/Employee-Compensation/88g8-5mnd


## Data Dictionary

<b>OGC</b>: Organization Group Code - Org Group is a group of Departments. For example, the Public Protection Org Group includes departments such as the Police, Fire, Adult Probation, District Attorney, and Sheriff.


<b>OG</b>: Organization Group names


<b>DC</b>: Department Code - Departments are the primary organizational unit used by the City and County of San Francisco. Examples include Recreation and Parks, Public Works, and the Police Department.


<b>Dept</b>: Department name


<b>UC</b>: Union Code - Unions represent employees in collective bargaining agreements. A job belongs to one union, although some jobs are unrepresented (usually temporarily).


<b>Union</b>: Union names


<b>JF</b>: Job Family - Job Family combines similar Jobs into meaningful groups.


<b>Job</b>: Job name


<b>EI</b>: Employee Identifier


<b>Salaries</b>: Salary of the employee


<b>Overtime</b>: Amounts paid to City employees working in excess of 40 hours per week. 


<b>H/D</b>: Health/Dental - City-paid premiums to health and dental insurance plans covering City 
employees. To protect confidentiality as legally required, pro-rated citywide averages are presented in lieu of employee-specific health and dental benefits. 


<b>YT</b>: Year Type - Fiscal (July through June) or Calendar (January through December)


<b>Total_Compensation</b>: The final compensation i.e. the sum of all salaries and benefits paid to City employees.

## EDA
I looked at the distributions of the data and the value counts for the various categorical variables. Below are a few highlights.

Dataset Shape: (287836, 15)  
|    | Name               | dtypes  | Missing | Uniques |
|----|--------------------|---------|---------|---------|
| 0  | Year               | int64   | 0       | 4       |
| 1  | OGC                | int64   | 0       | 7       |
| 2  | OG                 | object  | 0       | 7       |
| 3  | DC                 | object  | 0       | 54      |
| 4  | Dept               | object  | 0       | 54      |
| 5  | UC                 | int64   | 0       | 789     |
| 6  | Union              | object  | 36      | 73      |
| 7  | JF                 | object  | 38      | 55      |
| 8  | Job                | object  | 0       | 1136    |
| 9  | EI                 | int64   | 0       | 52403   |
| 10 | Salaries           | int64   | 0       | 104444  |
| 11 | Overtime           | int64   | 0       | 33632   |
| 12 | H/D                | float64 | 0       | 113669  |
| 13 | YT                 | object  | 0       | 2       |
| 14 | Total_Compensation | int64   | 0       | 155965  |



