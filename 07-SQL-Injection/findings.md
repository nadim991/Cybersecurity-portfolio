SQL Injection Finding
Finding ID: SQLI-01
Title: SQL Injection in User ID Parameter
Severity: High
Status: Confirmed
Affected Application: DVWA
Affected Parameter: User ID
Description
The User ID parameter accepts SQL syntax as part of the input. Testing demonstrated that user-controlled input is processed by the backend SQL query without adequate input protection.
Evidence
Normal input:
1
returned:
ID: 1 First name: admin Surname: admin
ORDER BY testing showed:
ORDER BY 1
worked successfully.
ORDER BY 3
returned:
Unknown column '3' in 'order clause'
This indicates that the query exposes two columns.
UNION-based SQL Injection was successfully demonstrated with two output columns.
Database enumeration identified:
Database: dvwa
MySQL version:
5.0.51a-3ubuntu5
Table enumeration identified:
guestbook users
Column enumeration of the users table identified:
user_id first_name last_name user password avatar
Blind SQL Injection
The Blind SQL Injection functionality was tested using different SQL conditions.
A true condition returned the expected user information.
A false condition returned no matching user information.
The difference in application behavior demonstrates that the injected SQL condition is being evaluated by the backend database.
Impact
Successful SQL Injection may allow an attacker to manipulate database queries.
Potential impact includes unauthorized data access, information disclosure, authentication bypass, and modification of database information.
Risk
The vulnerability is significant because the application exposes database information through a user-controlled parameter.
Recommendation
Use parameterized queries or prepared statements.
Implement strict server-side input validation.
Apply least-privilege permissions to the database account.
Prevent detailed database errors from being displayed to users.
Conduct regular vulnerability assessments and secure code reviews.
Testing Environment
Target: 192.168.196.129
Application: DVWA
Platform: Metasploitable2
Scope: Authorized local virtual lab
Conclusion
SQL Injection and Blind SQL Injection were successfully demonstrated against the DVWA lab application. The testing confirmed that the User ID parameter can influence backend SQL query behavior and expose database information.