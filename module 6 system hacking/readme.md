Module 06 — System Hacking (CEH v13)
Objective

Develop practical skills to identify, exploit, and remediate system-level weaknesses on target hosts. Focus is on understanding attack chains (recon → exploit → escalate → maintain → cover tracks) and applying defensive controls to reduce risk.

Description

System Hacking covers attacks against individual machines (servers, workstations) to gain unauthorized access, escalate privileges, maintain persistence, and extract data — all within an authorized, controlled environment. This module explains common exploitation vectors (weak credentials, misconfigurations, vulnerable services, unpatched software), post-exploitation techniques, and how defenders can detect and mitigate these activities. Emphasis is placed on safe, non-destructive verification and thorough documentation.

Key Learning Outcomes

After completing this module you will be able to:

Understand the full system-level attack lifecycle: access → privilege escalation → persistence → data exfiltration → cleanup.

Identify common local and remote exploitation vectors (default creds, buffer overflows, insecure services).

Execute and validate exploitation techniques in lab environments without causing lasting damage.

Perform privilege escalation on Windows and Linux hosts (local/remote).

Implement persistence mechanisms and know how to detect and remediate them.

Use post-exploitation tools to enumerate system data, user activity, configurations, and credentials.

Recommend hardening controls and detection strategies to reduce system-level risk.

Techniques Covered

Gaining initial access: password guessing/brute force, exploit chaining, vulnerable services.

Password attacks: local passwd/hash extraction, crack workflows, pass-the-hash, pass-the-ticket basics.

Privilege escalation: SUID/SGID misconfigs, weak service permissions, kernel exploits, DLL hijacking.

Post-exploitation: system discovery, credential harvesting (Mimikatz, /etc/shadow), keylogging (lab-only), pivoting.

Persistence techniques: scheduled tasks/cron jobs, startup scripts, services/registry autoruns, web shells.

Anti-forensics & cover tracks (theory only): log tampering, timestomping; discussing why this is unethical/illegal in real tests.

Safe exploitation practices: proof-of-concept verification without destructive payloads.

Common Tools & Commands
Purpose	Tools / Examples
Exploitation framework	Metasploit (msfconsole, exploit modules)
Credential harvesting	Mimikatz, hashcat, john
Post-exploitation	Meterpreter, PowerShell Empire (lab env), Impacket
Linux escalation & enumeration	LinPEAS, Linux Exploit Suggester, sudo -l, id, ps
Windows enumeration	Windows-exploit-suggester, whoami /priv, query user
Pivoting & tunneling	ssh -L/-R, proxychains, socks proxy via Meterpreter
File & process analysis	lsof, netstat, ss, tasklist, procmon (Windows)
Memory / dump	volatility (analysis), procdump
Example Lab Tasks (step-by-step)

Initial Access

Use credential list (authorized lab) to attempt SSH/RDP login; document successful/failed attempts.

Exploit a vulnerable service

Safe PoC exploit (e.g., known service with non-destructive payload) within lab VM.

Local Enumeration

Run LinPEAS / PowerUp to find privilege escalation vectors; inspect SUID files, weak sudo rules.

Privilege Escalation

Demonstrate a safe escalation (e.g., exploit misconfigured sudo rule).

Credential Harvesting

Extract hashed passwords (e.g., /etc/shadow or SAM via authorized approach) and demonstrate cracking workflow (lab-only).

Persistence

Create a benign scheduled task or cron job (clearly documented) to show persistence mechanics (remove after test).

Post-exploitation Recon

Enumerate connected hosts, saved credentials, configuration files, and sensitive data locations.

Cleanup & Reporting

Remove any artifacts, restore changed settings in the lab, and document steps, outputs, and remediation steps.

Deliverables

Module-06 Report (PDF/Markdown): Attack chain narrative, commands, screenshots, outputs, proof-of-concept (non-destructive).

Raw outputs: Meterpreter sessions logs, exploit output, enumeration tool results.

Commands.txt: Exact commands and parameters used.

Evidence folder: Screenshots, hashes, logs (redacted if needed).

Remediation Recommendations: Patching, account hardening, privilege restriction, EDR/monitoring rules.

Countermeasures & Hardening

Enforce strong password policies and MFA for privileged accounts.

Apply timely OS and application patches; maintain a vulnerability management program.

Restrict sudo and administrative privileges to least privilege.

Disable or harden legacy/unused services; close unnecessary ports.

Deploy Endpoint Detection and Response (EDR) and centralized logging with alerting for suspicious behavior (Lateral movement, credential dumping).

Regularly audit SUID/SetUID files, scheduled tasks, and startup items.

Use process integrity checks and application allow-listing.

Legal & Safety Reminder

All system hacking activities must be performed only on systems for which you have explicit written authorization (laboratory VMs, sanctioned pentest engagements). Techniques such as credential dumping, persistence, and anti-forensics are destructive or illegal if used without permission — in reports, include proof of authorization and ensure all changes are reverted in lab environments.
