Cross Site Scripting Assessment
Target: DVWA on Metasploitable2
Target IP: 192.168.196.129
Application: Damn Vulnerable Web Application
Testing Environment: Authorized Local Lab Environment
Objective
The objective of this assessment was to identify and demonstrate Cross Site Scripting vulnerabilities in the DVWA application.
Testing Methodology
Tested Reflected XSS functionality.
Tested JavaScript injection through user input.
Confirmed JavaScript execution using a browser alert.
Tested Stored XSS functionality.
Tested the application under different DVWA security levels.
Documented successful and unsuccessful payload execution.
Reflected XSS
The Reflected XSS functionality was tested using the following payload:
�
alert('XSS-Nadim')
The payload was successfully reflected by the application and executed as JavaScript in the browser.
Result:
Reflected XSS: Confirmed
Stored XSS
The Stored XSS functionality was tested through the comment form.
The JavaScript payload was submitted as user-controlled content and the stored comment was subsequently viewed again.
Result:
Stored XSS: Confirmed if the payload executed when the stored comment was displayed.
Security Level Testing
At Low security level, the basic JavaScript payload successfully executed.
At High security level, the same payload did not execute because the application applied stronger input filtering.
Impact
An attacker could potentially execute malicious JavaScript in a victim's browser.
Depending on the application, successful XSS could lead to session-related attacks, unauthorized actions, phishing, page manipulation, or exposure of sensitive information.
Remediation
Use proper output encoding for user-controlled data.
Validate and sanitize user input.
Use a strong Content Security Policy.
Avoid inserting untrusted input directly into HTML.
Use secure cookie attributes such as HttpOnly and SameSite.
Evidence
All testing was performed against the authorized local DVWA and Metasploitable2 lab environment.
Screenshots are stored in the screenshots directory.