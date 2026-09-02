SQL Injection Assessment
Target: DVWA on Metasploitable2 Target IP: 192.168.196.129 Application: Damn Vulnerable Web Application Testing Environment: Authorized local lab environment
Objective
The objective of this assessment was to identify and demonstrate SQL Injection vulnerabilities in the DVWA application.
Testing Methodology
Tested the User ID parameter with normal input.
Tested SQL syntax manipulation.
Used ORDER BY testing to determine the number of columns.
Used UNION-based SQL Injection to confirm SQL query manipulation.
Identified the active database.
Enumerated database tables.
Enumerated columns from the users table.
Tested Blind SQL Injection using true and false conditions.
Key Results
The User ID parameter was confirmed to be vulnerable to SQL Injection.
ORDER BY testing showed that the query uses two columns.
UNION SELECT testing successfully returned attacker-controlled values.
The active database was identified as dvwa.
The MySQL version was identified as 5.0.51a-3ubuntu5.
The following tables were identified:
guestbook users
The users table exposed the following columns:
user_id first_name last_name user password avatar
Blind SQL Injection testing also produced different responses for true and false conditions.
Impact
An attacker could manipulate the application's SQL queries through the vulnerable parameter.
Depending on database permissions and application functionality, SQL Injection could allow unauthorized database access, information disclosure, authentication bypass, or modification of database data.
Remediation
Use prepared statements and parameterized queries.
Validate user input on the server side.
Do not build SQL queries by directly concatenating user input.
Use a database account with the minimum required privileges.
Disable detailed SQL error messages in production.
Perform regular application security testing.
Evidence
All testing was performed against the authorized local DVWA and Metasploitable2 lab environment.
Screenshots are stored in the screenshots directory.