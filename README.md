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
![image](https://user-images.githubusercontent.com/72138103/169702417-8a47fcf2-0a96-4148-9087-f002790ffb35.png)
</br>

sol 2 )  
use upgrad;

select *
from employees
where officeCode between 2 and 4
order by firstName;

</br>

3 ) Employees with Odd-Numbered Office Codes
Write a query to retrieve the extensions and office codes of all the employees having an odd-numbered office code. Arrange them in the alphabetical order of their first names.
![image](https://user-images.githubusercontent.com/72138103/169702458-d03ee086-a45e-4c13-9124-1ec4fee19e7e.png)

</br>
sol 3 ) 
use upgrad;

select extension, officeCode
from employees
where officeCode % 2 = 1
order by firstName;

</br>

4 ) Employees with Even-Numbered Office Codes
Write a query to retrieve the extensions and office codes of all the employees having an even-numbered office code. Arrange them in the alphabetical order of their first names.
![image](https://user-images.githubusercontent.com/72138103/169702526-336424f2-ebfb-49de-9902-c152fd252ffa.png)
</br>
4 ) 
use upgrad;

select extension, officeCode from employees where MOD(officeCode , 2) = 0 order by firstName;

</br>

5 ) Lucky Employees
Write a query to retrieve all the details of employees who don't report to anyone. Arrange them in the increasing order of their employee numbers. Please click on the sample output to view it clearly.
![image](https://user-images.githubusercontent.com/72138103/169702583-a04363de-64b8-4ef6-8182-9a82b101e39f.png)

sol 5 ) use upgrad;

select *
from employees
where reportsTo is null
order by employeeNumber;

</br>

-------------------------------------------------------------------------------------------------------------------------------------
<h3> Timed Test - III </h3>

1 ) Non Sales Representatives
Write a query to retrieve the first names, last names and job titles of all those employees who are not sales representatives. Arrange them in the alphabetical order of their job titles. If two employees have the same job title, arrange them in the alphabetical order of their first names.
![image](https://user-images.githubusercontent.com/72138103/169702699-36ae46ff-1875-4c90-af63-74cc33a308ad.png)

</br>
sol 1 )
use upgrad;

select firstName, lastName, jobTitle
from employees
where jobTitle != 'Sales Rep'
order by jobTitle, firstName;

</br>

2 ) Selected Extensions
Write a query to retrieve the list of employee numbers and extensions of all the employees who have an extension ending with '1'. Arrange the list in the increasing order of the employee numbers.

![image](https://user-images.githubusercontent.com/72138103/169702943-34ab8bb5-6194-4338-b7ad-e3adb5d401fc.png)

sol 2 ) use upgrad;

select employeeNumber, extension
from employees
where extension like '%1'
order by employeeNumber;
</br>

3 ) Select Employees
Write a query to retrieve the first and last names of all employees who have the substring 'er' in their last names. List the output in the alphabetical order of the first names of the employees.
![image](https://user-images.githubusercontent.com/72138103/169702983-1593fc69-6406-44a7-85b5-75322cb881bf.png)
</br>

sol 3 ) use upgrad;

select firstName, lastName
from employees
where lastName like '%er%'
order by firstName;

</br>

4 ) Last Names
Write a query to retrieve the last names of all employees and arrange them in the alphabetical order.
</br>

sol 4 ) use upgrad;

select lastName
from employees
order by lastName;

---------------------------------------------------------------------------------------------------------------------------------------

<h3> Timed Test - IV </h3 >

1 ) Employees with Specific Employee Numbers
Write a query to retrieve the employee numbers, first and last names having employee numbers beginning with 1 and ending with 2. Arrange them in the alphabetical order of their first names.



Note that all employee numbers consist of 4 digits.
![image](https://user-images.githubusercontent.com/72138103/169703129-7469c571-624c-43ae-8798-697f6de15450.png)
</br>
sol 1 )
use upgrad;
select employeeNumber,firstName, lastName from employees
where employeeNumber like '1%2'
order by firstName;

2 ) Product Codes with Patterns
Write a query to retrieve the product codes and prices of all products having the pattern '_32' in their product codes. Arrange these products in the decreasing order of their prices.
![image](https://user-images.githubusercontent.com/72138103/169703164-be707189-2c5a-485a-9bf9-2d5e51ea30fb.png)

</br>

sol 2 )
use upgrad;
select productCode, priceEach from orderdetails where productcode like '____32__' order by priceEach desc;
</br>

3 ) First Names of Employees
Write a query to list the first names of the employees in the reverse alphabetical order.
</br>

sol 3 ) use upgrad;

select firstName
from employees
order by firstName desc;

</br>

4 ) Minimum and Maximum Order Amounts
Write a query to retrieve the minimum and maximum order amounts among the products.
![image](https://user-images.githubusercontent.com/72138103/169703233-421c634f-840f-47ea-9b08-c57eb909d817.png)
</br>
sol 4 )
use upgrad;

select min(priceEach * quantityOrdered) as minAmount, max(priceEach * quantityOrdered) as maxAmount
from orderdetails;
</br>
------------------------------------------------------------------------------------------------------------------------------------------------------------
</br>


<h3> Timed Test - V </h3>
</br>

1 ) Total and Average Order Amounts
Write a query to retrieve the total amount received from all orders, as well as the average amount.

![image](https://user-images.githubusercontent.com/72138103/169703404-57c34c45-45aa-4c64-8d65-bf550ea89dfc.png)

</br>

sol 1 ) use upgrad;

select sum(priceEach * quantityOrdered) as totalAmount, avg(priceEach * quantityOrdered) as avgAmount
from orderdetails;
</br>

2 ) Rounded Total and Average Order Amounts
Write a query to retrieve the total amount received from all orders, as well as the average amount and round the answers to the nearest integer.

![image](https://user-images.githubusercontent.com/72138103/169703441-4d22fb58-e674-44c9-a638-78a124757b02.png)

</br>
sol 2 )use upgrad;
select round(sum(quantityordered * priceeach)) as totalAmount, round(avg(quantityordered * priceeach)) as avgAmount
from orderdetails;

</br>
3 ) Employee Strength vs. Office Code
Write a query to retrieve the list of number of employees corresponding to each office code. Arrange the number of employees in the increasing order of the office codes.
![image](https://user-images.githubusercontent.com/72138103/169703492-cc38a0ad-74fb-4b29-9b41-3c3549e317b9.png)
</br>
sol 3 ) use upgrad;

select officeCode, count(*) as no_Of_Employees
from employees
group by officeCode
order by officeCode;

</br>

4 ) Rounded Total Order Amounts
Write a query to retrieve the rounded total order amounts for each order line number. Arrange these amounts in the decreasing order.

![image](https://user-images.githubusercontent.com/72138103/169703542-82f734a6-e651-47dc-8ac0-813f40dc9ba1.png)
</br>

sol 4 ) use upgrad;

select round(sum(priceEach * quantityOrdered)) as roundedAmount, orderLineNumber
from orderdetails
group by orderLineNumber
order by roundedAmount desc;

</br>

5 ) Orders of Less Than One Lakh
Write a query to retrieve order line numbers having rounded line-wise order amounts of less than 1,00,000. Arrange them in the decreasing order of their amounts.
![image](https://user-images.githubusercontent.com/72138103/169703591-4a34af7a-37ee-4139-aeab-44be03e9ffcf.png)
</br>
sol 5 ) 
use upgrad;

select round(sum(priceEach * quantityOrdered)) as roundedAmount, orderLineNumber
from orderdetails
group by orderLineNumber
having roundedAmount < 100000
order by roundedAmount desc;
</br>

