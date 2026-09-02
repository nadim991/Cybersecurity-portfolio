XSS Findings
Finding ID: XSS-01
Title: Reflected Cross Site Scripting
Severity: Medium
Status: Confirmed
Affected Component: DVWA XSS Reflected
Description
The Reflected XSS functionality allows user-controlled input to be reflected into the application response without sufficient output encoding.
A JavaScript payload was successfully executed through the vulnerable input.
Payload:
�
alert('XSS-Nadim')
Evidence
The payload was submitted through the Reflected XSS input.
A browser popup displaying:
XSS-Nadim
was successfully triggered.
This confirms that attacker-controlled JavaScript can execute in the application's browser context.
Impact
Successful exploitation could allow an attacker to execute JavaScript in a victim's browser.
Potential impacts include session-related attacks, unauthorized actions, phishing, page manipulation, and information exposure.
Recommendation
Implement context-aware output encoding.
Validate user input on the server side.
Sanitize user-controlled HTML where necessary.
Implement a Content Security Policy.
Use secure cookie attributes.
Finding ID: XSS-02
Title: Stored Cross Site Scripting
Severity: High
Status: Confirmed
Affected Component: DVWA XSS Stored
Description
The Stored XSS functionality allows user-controlled content to be stored by the application and subsequently rendered to users without sufficient sanitization or output encoding.
Payload:
�
alert('XSS-Nadim')
Evidence
The payload was submitted through the comment functionality.
When the stored comment was displayed again, the JavaScript payload executed and triggered the browser alert.
This confirms Stored XSS.
Impact
Stored XSS can affect users who view the malicious stored content.
Because the payload remains stored in the application, multiple users may be exposed to the attack.
Recommendation
Sanitize user-generated content before storage or rendering.
Apply context-aware output encoding.
Implement a Content Security Policy.
Validate input on the server side.
Avoid rendering untrusted HTML directly.
Security Level Observation
The basic XSS payload successfully executed when DVWA Security was set to Low.
The same type of payload did not execute at High security level due to stronger filtering.
Testing Environment
Target: 192.168.196.129
Application: DVWA
Platform: Metasploitable2
Security Level: Low
Scope: Authorized Local Virtual Lab
Conclusion
Reflected XSS was successfully confirmed in DVWA.
Stored XSS was successfully confirmed if the stored payload executed when the comment was displayed again.
The assessment demonstrates how insufficient input handling and output encoding can allow attacker-controlled JavaScript to execute in a web application.