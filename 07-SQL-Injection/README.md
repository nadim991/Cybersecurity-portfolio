# SQL Injection Assessment

## Assessment Overview

This project documents the security assessment of SQL Injection vulnerabilities within the Damn Vulnerable Web Application (DVWA).

The assessment was conducted in an authorized and isolated local laboratory environment using Metasploitable2.

| Category | Details |
|---|---|
| Target Application | Damn Vulnerable Web Application (DVWA) |
| Target Host | Metasploitable2 |
| Target IP | `192.168.196.129` |
| Vulnerability | SQL Injection |
| Database | MySQL |
| Testing Environment | Authorized Local Lab |
| Testing Type | Web Application Security Assessment |

## Objective

The objective of this assessment was to identify, validate, and demonstrate SQL Injection vulnerabilities within the DVWA application.

The assessment focused on determining whether user-controlled input could manipulate the application's underlying SQL queries and allow unauthorized interaction with the database.

## Testing Methodology

The assessment followed a structured SQL Injection testing process:

1. Tested the User ID parameter using normal input.
2. Tested SQL syntax manipulation.
3. Performed `ORDER BY` testing to determine the number of columns.
4. Used `UNION SELECT` techniques to confirm SQL query manipulation.
5. Identified the active database.
6. Enumerated database tables.
7. Enumerated columns from the `users` table.
8. Tested Blind SQL Injection using true and false conditions.
9. Documented the observed responses and results.

## SQL Injection Validation

The User ID parameter was tested with controlled SQL input.

The application was found to process the supplied input in a way that allowed manipulation of the underlying SQL query.

**Result:** SQL Injection confirmed.

## Column Enumeration

`ORDER BY` testing was performed to determine the number of columns returned by the underlying query.

**Result:** The query was determined to use **two columns**.

## UNION-Based SQL Injection

`UNION SELECT` testing was performed after identifying the column count.

The test successfully returned attacker-controlled values through the application's response.

**Result:** UNION-based SQL Injection confirmed.

## Database Enumeration

Further testing was performed to identify the active database and enumerate database structures.

### Database Information

| Property | Result |
|---|---|
| Database | `dvwa` |
| Database Server | MySQL |
| MySQL Version | `5.0.51a-3ubuntu5` |

### Identified Tables

The following tables were identified:

- `guestbook`
- `users`

### `users` Table Columns

The following columns were identified in the `users` table:

- `user_id`
- `first_name`
- `last_name`
- `user`
- `password`
- `avatar`

## Blind SQL Injection

Blind SQL Injection testing was performed using conditions designed to produce different responses based on whether the supplied condition evaluated as true or false.

The application produced different responses for true and false conditions.

**Result:** Blind SQL Injection behavior confirmed.

## Key Findings

The assessment identified the following:

- The User ID parameter was vulnerable to SQL Injection.
- The underlying query was determined to use two columns.
- `UNION SELECT` testing successfully returned attacker-controlled values.
- The active database was identified as `dvwa`.
- The MySQL version was identified as `5.0.51a-3ubuntu5`.
- The `guestbook` and `users` tables were identified.
- Multiple columns within the `users` table were enumerated.
- Different responses were observed during Blind SQL Injection testing.

## Impact

SQL Injection can allow an attacker to manipulate application-generated SQL queries through vulnerable input parameters.

Depending on database privileges, application architecture, and available functionality, successful SQL Injection may result in:

- Unauthorized database access
- Sensitive information disclosure
- Authentication bypass
- Modification or deletion of database records
- Further compromise of the application or underlying system

## Remediation

The following security controls are recommended:

- Use prepared statements and parameterized queries.
- Validate user input on the server side.
- Never construct SQL queries by directly concatenating user-controlled input.
- Apply the principle of least privilege to database accounts.
- Disable detailed database error messages in production environments.
- Use secure database access controls.
- Perform regular application security testing.
- Conduct code review to identify unsafe SQL query construction.

## Evidence

All testing was performed against the authorized local DVWA application running on Metasploitable2.

The assessment evidence includes:

- SQL Injection input testing
- `ORDER BY` column enumeration
- `UNION SELECT` testing
- Database identification
- Table enumeration
- Column enumeration
- Blind SQL Injection true/false testing
- Application responses demonstrating the identified behavior

Supporting screenshots are maintained in the project's `screenshots` directory.

## Tools & Technologies

- Kali Linux
- Metasploitable2
- Damn Vulnerable Web Application (DVWA)
- MySQL
- Web Browser
- SQL Injection techniques
- UNION-based SQL Injection
- Blind SQL Injection

## Key Skills Demonstrated

- Web Application Security Testing
- SQL Injection Identification
- SQL Query Manipulation Analysis
- UNION-Based SQL Injection
- Blind SQL Injection Testing
- Database Enumeration
- Table Enumeration
- Column Enumeration
- Vulnerability Validation
- Risk Assessment
- Security Documentation
- Remediation Planning

## Ethical Scope

All testing was performed against a deliberately vulnerable application inside an authorized and isolated local laboratory environment.

No unauthorized systems, applications, or third-party services were targeted.

This project is intended for cybersecurity education, authorized security testing, and professional portfolio demonstration.