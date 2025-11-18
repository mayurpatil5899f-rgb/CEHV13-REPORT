Module 15 – SQL Injection (Summary)
📌 Overview

SQL Injection (SQLi) is a web application attack where an attacker inserts malicious SQL queries into input fields to manipulate the database. It occurs when user input is not properly validated or sanitized.

🎯 Learning Objectives

Understand how SQL injection works

Identify vulnerable parameters

Perform manual and automated SQL injection testing

Extract sensitive information from databases

Understand SQLi prevention techniques

🔍 Types of SQL Injection
1. In-Band SQL Injection

Error-Based SQLi: Uses database error messages to gather information

Union-Based SQLi: Combines multiple queries to extract data

2. Blind SQL Injection

Boolean-Based SQLi: Observes page responses (True/False)

Time-Based SQLi: Uses delays to infer database behavior

3. Out-of-Band SQL Injection

Uses external channels (DNS/HTTP requests) to extract data

🧪 SQL Injection Testing Steps

Identify input fields (login form, search box, URL parameters)

Inject basic payloads like ' OR '1'='1 or "

Confirm database errors or unusual responses

Use advanced payloads to enumerate database tables

Dump data using tools

Report findings with proof-of-concept

🛠 Tools Used

sqlmap

Burp Suite Intruder

Havij (legacy)

Nmap NSE scripts

Browser developer tools

💥 Common SQL Injection Payloads
' OR '1'='1 --
" OR 1=1 --
admin' --
1' OR '1'='1' #

📂 Attack Scenarios

Bypassing authentication

Extracting usernames/passwords

Listing databases and tables

Modifying or deleting database records

Impersonating users

Taking full control of the web application

🛡 Prevention & Mitigation

Use prepared statements & parameterized queries

Validate and sanitize all user inputs

Apply least privilege principle

Use Web Application Firewalls (WAFs)

Regular security testing and patching

Disable detailed error messages

📝 Conclusion

SQL Injection remains one of the most dangerous web application vulnerabilities. Understanding and testing for SQLi is essential for securing web applications and databases. Proper input validation and secure coding practices are the most effective defenses.
