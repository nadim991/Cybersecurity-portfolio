# Cross-Site Scripting (XSS) Assessment

## Assessment Overview

This project documents the security assessment of Cross-Site Scripting (XSS) vulnerabilities within Damn Vulnerable Web Application (DVWA).

The assessment was conducted in an authorized and isolated local laboratory environment using Metasploitable2.

| Category | Details |
|---|---|
| Target Application | Damn Vulnerable Web Application (DVWA) |
| Target Host | Metasploitable2 |
| Target IP | `192.168.196.129` |
| Vulnerability | Cross-Site Scripting (XSS) |
| Testing Environment | Authorized Local Lab |
| Testing Type | Web Application Security Assessment |

---

## Objective

The objective of this assessment was to identify, validate, and demonstrate Cross-Site Scripting vulnerabilities within DVWA.

The assessment focused on determining whether user-controlled input could be interpreted and executed as JavaScript by the application.

---

## Testing Methodology

The assessment followed a structured web application security testing approach:

1. Identify XSS testing functionality within DVWA.
2. Submit controlled JavaScript payloads through user-controlled input fields.
3. Observe how the application processes and reflects the supplied input.
4. Validate JavaScript execution in the browser.
5. Test both Reflected XSS and Stored XSS functionality.
6. Repeat testing under different DVWA security levels.
7. Record successful and unsuccessful payload execution.
8. Document the security impact and recommended remediation.

---

## Reflected XSS

### Test Description

The Reflected XSS functionality was tested by submitting a controlled JavaScript payload through the application's user input.

### Payload

```html
<script>alert('XSS-Nadim')</script>