# Advanced SQL Functions and Formulas

============================================================================
# Module 2 Advanced SQL: Functions and Formulas </br>

<h3> Practice Questions </h3> </br>

<h3> Timed Test-1 </h3>

1 ) Write a query to return the employee number, first name and last name of all the employees. Order the employees in the alphabetical order of their first names. </br>
![image](https://user-images.githubusercontent.com/82382478/169697144-ac939879-a8f8-49e4-93a6-cc1d3ea57100.png)

sol 1 )  
use upgrad;

# Write your code below
select employeeNumber, firstName, lastName from employees order by firstName;

</br>

2 ) Write a query to return the email ids of all the employees in the increasing order of their employee numbers. </br>
sol 2 )
use upgrad;

select email as emailID
from employees
order by employeeNumber;
 
 </br>
 
 3 ) Employees with a Specific Office Code
Write a query to retrieve the first names and last names of all the employees having an office code of 4. Arrange them in the alphabetical order of their last names.
</br>
![image](https://user-images.githubusercontent.com/82382478/169697199-022e84a3-7c08-44eb-9b0c-5485edd44422.png)

sol 3 ) 
use upgrad;

select firstName, lastName
from employees
where officeCode = 4
order by lastName;

</br>

4 ) All Employee Details
Write a query to retrieve the entire data of all the employees from the employees table. Arrange them in the alphabetical order of their first names. Please click on the sample output to view it clearly.
![image](https://user-images.githubusercontent.com/82382478/169697231-2bd251c3-62b3-48c6-a89c-b20ed4598896.png)
</br>

sol 4 ) 
use upgrad;

select *
from employees
order by firstName;

5 ) Filtered Employees
Write a query to retrieve the email addresses of all the employees who have an office code of 6 and report to employees with code '1088'. Arrange these employees in the increasing order of their employee numbers.
</br>

sol 5 ) 
use upgrad;

select email
from employees
where officeCode = 6 and reportsTo = 1088
order by employeeNumber;

</br>
--------------------------------------------------------------------------------------------------------------------------------------------
<h3> Timed Test-2 </h3>

1 ) More Filtered Employees
Write a query to retrieve the email addresses of all the employees who have an office code of 6 or report to employees with employee number '1088'. Arrange them in the reverse alphabetical order of their first names.
</br>

sol 1) 
use upgrad;

select email
from employees
where officeCode = 6 or reportsTo = 1088
order by firstName desc;

</br>

2 ) Employees from Specific Office Codes
Write a query to retrieve all the details of all the employees who have an office code from 2 to 4. Arrange them in the alphabetical order of their first names. Please click on the sample output to view it clearly.
