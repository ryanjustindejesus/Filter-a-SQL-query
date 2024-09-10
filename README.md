<h1>Filtering a SQL query </h1>



<h2>Description</h2>
In this lab, I applied basic filters to SQL queries to retrieve information from a database. I used SQL to get specific information about employees, their machines, and the departments they’re in. I used the MariaDB shell to run SQL queries.
<br />


<h2>Practical experience gained in this Lab</h2>

- <b>Applying the WHERE clause to filter what a SQL query returns</b> 
- <b>Using the LIKE operator to filter for patterns</b>

<h2>Environments Used </h2>

- <b>Qwiklabs</b> 

<h2>Lab walk-through:</h2>

<h2>Task 1: List all organization machines </h2>
In this task, I got a list of all organization machines and their operating systems. The data is contained in the machines table.
 <br/> <br />
(1) I used the command "SELECT device_id, operating_system FROM machines;" to retrieve only the device_id and operating_system columns from the machines table. 
<br/> <br/> <p align="center">
<img src="https://imgur.com/QQxcJi9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br /> <br />

<h2>Task 2: Retrieve a list of the machines with OS 2 </h2>
In this task, I obtained a list of all machines with the 'OS 2' operating system because these machines need an update. 
<br/> <br />
(1) I used the command "SELECT device_id, operating_system FROM machines WHERE operating_system = 'OS 2';" to select all the records from the machines table with a value of 'OS 2' in the operating_system column.
<br /> <br /> <p align="center">
<img src="https://imgur.com/9kwiVGS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br /> <br />

<h2>Task 3: List employees in specific departments </h2>
In this task, I retrieved a list of all the employees in the Finance and Sales departments to obtain their office numbers. 
 <br/> <br/>
(1) First, I used the command "SELECT * FROM employees WHERE department = 'Finance';" to filter the rows returned from the department column in the employees table to include only employees from the 'Finance' department.  <br/>
<br/> <p align="center">
<img src="https://imgur.com/yGjLaKt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br /> <br />
(2) Finally, I used the command "SELECT * FROM employees WHERE department = 'Sales';" to return employees who are in the 'Sales' department.
<br/> <p align="center">
<img src="https://imgur.com/ywoX0Ii.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br /> <br />

<h2>Task 4: Identify employee machines </h2>
My team recently discovered that there are issues with machines in the South building. In this task, I obtained certain employee and computer information. A machine in 'South-109' has an issue. I need to determine which employee uses that computer so I can send them an alert.
 <br/> <br/> 
(1) First, I used the command "SELECT * FROM employees WHERE office = 'South-109';" to identify which employee uses the office in 'South-109'. 
<br/> <br/>  <p align="center">
<img src="https://imgur.com/gnplrQS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br /> <br />
My team determined that there was an issue with all the machines in the South building. Offices in the organization are named with the building name, a hyphen, and the office number in that building. 
<br /> <br />
(2) Next, I used the command "SELECT * FROM employees WHERE office LIKE 'South%';" to return information on all the employees in the 'South' building.
<br/> <p align="center">
<img src="https://imgur.com/33fHK6q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
