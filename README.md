<h1>Apply Filters to SQL Queries</h1>

<h2>Description</h2>
My organization is working to make their system more secure. It is my job to ensure the system is safe, investigate all potential security issues, and update employee computers as needed. The following steps provide examples of how I used SQL with filters to perform security-related tasks
<br />
<br />
<h2>Retrieve after hours failed login attempts</h2>
There was a potential security incident that occurred after business hours (after 18:00). All after hours login attempts that failed need to be investigated.
The following code demonstrates how I created a SQL query to filter for failed login attempts that occurred after business hours.

<br />
<br />
  
<img src="https://imgur.com/AsS92Kp.png" height="80%" width="80%" alt= "SQL Steps"/>
<br />
The first part of the screenshot is my query, and the second part is a portion of the output. This query filters for failed login attempts that occurred after 18:00. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with an AND operator to filter my results to output only login attempts that occurred after 18:00 and were unsuccessful. The first condition is login_time > '18:00', which filters for the login attempts that occurred after 18:00. The second condition is success = FALSE, which filters for the failed login attempts. 
<br />
<h2>Retrieve login attempts on specific dates</h2>
A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09 or on the day before needs to be investigated.
The following code demonstrates how I created a SQL query to filter for login attempts that occurred on specific dates.
<br />
<br />
<img src="https://imgur.com/lXUr21V.png" height="80%" width="80%" alt="SQL Steps"/>
<br />
<br />
The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred on 2022-05-09 or 2022-05-08. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with an OR operator to filter my results to output only login attempts that occurred on either 2022-05-09 or 2022-05-08. The first condition is login_date = '2022-05-09', which filters for logins on 2022-05-09. The second condition is login_date = '2022-05-08', which filters for logins on 2022-05-08.
<br />
<br />

<h2> Retrieve login attempts outside of Mexico </h2>
After investigating the organization’s data on login attempts, I believe there is an issue with the login attempts that occurred outside of Mexico. These login attempts should be investigated.
Below, you will find the code that illustrates how I formulated an SQL query to filter and isolate the login attempts that took place outside of Mexico.
<br />
<br />
<img src="https://imgur.com/vs93YBn.png" height="80%" width="80%" alt="SQL Steps"/>
<br />
<br />
The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred in countries other than Mexico. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with NOT to filter for countries other than Mexico. I used LIKE with MEX% as the pattern to match because the dataset represents Mexico as MEX and MEXICO. The percentage sign (%) represents any number of unspecified characters when used with LIKE
<br/>
<br/>
<h2> Retrieve employees in Marketing </h2>
My team needs to upgrade Marketing department computers in the East building. Here's the SQL code I used to find which employee machines to update:
<br/>
<br/>
<img src="https://imgur.com/RZhlqSb.png" height="80%" width="80%" alt="SQL Steps"/>
<br />
<br />
The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all employees in the Marketing department in the East building. First, I started by selecting all data from the employees table. Then, I used a WHERE clause with AND to filter for employees who work in the Marketing department and in the East building. I used LIKE with East% as the pattern to match because the data in the office column represents the East building with the specific office number. The first condition is the department = 'Marketing' portion, which filters for employees in the Marketing department. The second condition is the office LIKE 'East%' portion, which filters for employees in the East building
<br/>
<br/>
<h2> Retrieve employees in Finance or Sales</h2>
We need to update computers for Finance and Sales department employees. I used SQL to filter and find info on employees in these two departments.
<br/>
<br/>
<img src="https://imgur.com/D1WnH29.png" height="80%" width="80%" alt="SQL Steps"/>
<br />
<br />
The query selects all Finance and Sales department employees by filtering with "OR" instead of "AND" to include employees from either department. It first filters for "Finance" department employees, and then for "Sales" department employees.
<br/>
<br/>
<h2> Retrieve all employees not in IT</h2>
We need to apply another security update for non-IT department employees. I used SQL to filter and gather information about these employees.
<br>
<br>
<img src="https://imgur.com/sxCQXfY.png" height="80%" width="80%" alt="SQL Steps"/>
<br>
<br>
The query returns all employees not in the Information Technology department. First, I started by selecting all data from the employees table. Then, I used a WHERE clause with NOT to filter for employees not in this department.
<br>
<br>
<h2> Summary </h2>
I used SQL query filters to extract specific details about login attempts and employee machines. I utilized two distinct tables: log_in_attempts and employees. For each task, I called on the AND, OR, and NOT operators to filter the requisite data. Additionally, I used the LIKE operator with the percentage sign (%) wildcard to identify patterns.


</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
