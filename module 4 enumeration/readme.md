Module 04 — Enumeration (CEH v13)
Objective

Collect detailed information about systems and services discovered during scanning to identify user accounts, shares, services, and configuration details that can be used to plan privilege escalation or exploitation.

Description

Enumeration is the active process of probing a target to enumerate resources and extract detailed information (usernames, groups, shares, services, software versions, policies, etc.). Whereas scanning tells you what is alive and what ports are open, enumeration tells you what those services expose. This module covers techniques for enumerating network services (SMB, NetBIOS, RPC, LDAP, SNMP, SMTP, etc.), application-level enumeration (databases, web apps), authentication mechanisms, and weaknesses that lead to privilege escalation or lateral movement.

Key Learning Outcomes

After completing this module you will be able to:

Explain the role of enumeration within the penetration testing lifecycle.

Enumerate network services and extract actionable information (usernames, shares, ACLs).

Use protocol-specific enumeration techniques for SMB, LDAP, SNMP, RPC, and more.

Identify misconfigurations and exposed data that could be leveraged for exploitation.

Gather evidence and document findings with repeatable commands and outputs.

Recommend practical mitigations to reduce enumeration exposure.

Techniques Covered

NetBIOS and SMB enumeration (shares, sessions, user lists).

LDAP and Active Directory enumeration (users, groups, GPOs, trusts).

SNMP enumeration (community strings, device info).

RPC and DCE/RPC enumeration (services, endpoints).

SMTP/POP/IMAP enumeration (valid users, open relays).

Database enumeration (identifying DBMS, schemas, users).

Service banner grabbing and configuration inspection.

Brute-forcing / probing for valid usernames (responsibly, only with permission).

Correlating enumeration data with prior footprinting and scanning results.

Common Tools & Commands (examples)
Purpose	Tool	Example
SMB enumeration	enum4linux, smbclient, rpcclient	enum4linux -a 10.10.10.5
NetBIOS info	nbtscan, nmblookup	nbtscan 192.168.1.0/24
LDAP / AD	ldapsearch, BloodHound, Impacket	ldapsearch -x -h dc.example.com -b "dc=example,dc=com"
SNMP	snmpwalk, onesixtyone	snmpwalk -v2c -c public 10.10.10.20
RPC	rpcclient	rpcclient -U "" 10.10.10.5
SMTP user check	smtp-user-enum, swaks	smtp-user-enum -M VRFY -U users.txt -t mail.example.com
Web app enumeration	dirb, gobuster, nikto	gobuster dir -u http://target -w /usr/share/wordlists/dirb/common.txt
AD mapping/analysis	BloodHound (neo4j), SharpHound	Invoke-BloodHound -CollectionMethod All
General scripting	curl, python scripts	curl -I http://target
Example Lab Tasks (step-by-step)

Re-run targeted Nmap against live hosts with service/version detection.

Use enum4linux -a to gather SMB shares, local users, and password policy.

Query LDAP (if exposed) to enumerate users, groups, and OU structure.

Execute snmpwalk against devices to extract system info and community strings.

Use rpcclient to list shares and users via MS-RPC.

Test SMTP for valid usernames using safe enumeration techniques.

Run web-app content discovery and map endpoints for potential sensitive files.

Import collected AD data into BloodHound to visualise attack paths (in lab environment).

Correlate results, prioritise findings, and prepare report entries.

Deliverables

Module-04-Enumeration/README.md — summary, objectives, and commands used.

enumeration-report.pdf or enumeration-report.md — narrative of findings, screenshots, parsed outputs.

commands.txt — exact commands used during the engagement.

evidence/ — raw outputs, screenshots (enum4linux, ldapsearch, snmpwalk, rpcclient, etc.).

risk-summary.csv — enumerated items mapped to risk and recommended mitigation.

Common Findings & Examples of Impact

Exposed SMB shares containing sensitive files or credentials.

LDAP allowing anonymous binds or returning user lists.

SNMP using default or public community strings revealing network maps.

Misconfigured services exposing admin interfaces or user lists.

AD misconfigurations enabling escalation or lateral movement via weak trusts.

Countermeasures & Hardening

Disable unnecessary services and close unused ports.

Enforce strong ACLs on SMB shares; remove anonymous access.

Harden LDAP/AD: disable anonymous binds, restrict queries, enable audit logging.

Change default SNMP community strings; use SNMPv3 with authentication and encryption.

Harden mail servers to prevent user enumeration (throttle responses, uniform error messaging).

Implement monitoring/alerting for unusual enumeration patterns and rate-limits.

Periodic external OSINT/enum audits to detect accidental exposure.

Legal & Safety Reminder

Only perform enumeration with explicit written authorization. Enumeration can be noisy and may trigger alarms or cause service disruption—always use controlled lab environments or authorized targets.
