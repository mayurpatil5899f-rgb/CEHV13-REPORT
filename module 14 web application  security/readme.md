Module 14: Web Application Security
Overview

Module 14 focuses on identifying, exploiting, and mitigating vulnerabilities in web applications.
It covers secure coding practices, common attack vectors, web application testing techniques, and industry standards such as OWASP.

🧩 Key Learning Objectives

Understand web application architecture

Identify security flaws in web applications

Analyze and exploit common web vulnerabilities

Implement secure coding practices

Learn OWASP Top 10 methodologies

Perform web application penetration testing

🕸️ Common Web Application Vulnerabilities
🔹 1. Injection Attacks

SQL Injection

Command Injection

LDAP Injection

XML Injection

🔹 2. Authentication & Authorization Flaws

Broken Authentication

Broken Access Control

Credential stuffing

Weak session management

🔹 3. Cross-Site Attacks

XSS (Stored, Reflected, DOM-based)

CSRF (Cross-Site Request Forgery)

🔹 4. Security Misconfigurations

Default credentials

Directory listing enabled

Debug mode active

Missing security headers

🔹 5. Insecure Deserialization

Code execution

Replay attacks

Privilege escalation

🛠️ Tools Used in Web App Security Testing
Category	Tools
Scanning	OWASP ZAP, Nikto, Wapiti
Interception/Exploitation	Burp Suite, Postman, Fiddler
Automation	WFuzz, Gobuster, Dirb
Reporting	Dradis, Faraday, Serpico
🔍 OWASP Top 10 (Latest Highlights)

A01: Broken Access Control

A02: Cryptographic Failures

A03: Injection

A04: Insecure Design

A05: Security Misconfiguration

A06: Vulnerable and Outdated Components

A07: Identification and Authentication Failures

A08: Software and Data Integrity Failures

A09: Security Logging & Monitoring Failures

A10: Server-Side Request Forgery (SSRF)

🧪 Web Application Pentesting Methodology

Information Gathering

WhoIs, robots.txt, URL structure, sub-domains

Mapping the Application

Parameter discovery, directories, endpoints

Vulnerability Identification

Fuzzing inputs, testing auth flows

Exploitation

Using Burp Suite, ZAP, and manual payloads

Post-Exploitation

Privilege escalation, data extraction

Reporting

Document all findings with PoC

🛡️ Secure Coding & Defense Techniques

Input validation (whitelisting)

Parameterized queries (Prepared Statements)

Encoding and escaping user data

Implementing MFA & secure session handling

Enforcing least privilege

Regular vulnerability scanning

Using WAF (Web Application Firewall)
