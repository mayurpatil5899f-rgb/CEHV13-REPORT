
Module 10: Denial of Service (DoS) & Distributed Denial of Service

Introduction to DoS/DDoS

DoS (Denial of Service) is an attack that aims to make a system, service, or network unavailable by overwhelming it with traffic or exploiting vulnerabilities.

DDoS (Distributed Denial of Service) uses multiple compromised machines (botnets) to perform the attack simultaneously.

The goal is to exhaust bandwidth, CPU, memory, or application resources.

2. Types of DoS Attacks
A. Volumetric Attacks

Flood the target with massive traffic.

Examples:

UDP Flood

ICMP Flood (Ping Flood)

DNS Amplification

NTP Amplification

B. Protocol Attacks

Exploit weaknesses in network protocols.

Examples:

SYN Flood

Ping of Death

Smurf Attack

Fragmentation Attacks (Teardrop)

C. Application Layer Attacks

Target the application or service directly.

Examples:

HTTP GET/POST Flood

Slowloris

Slow POST Attack

3. Botnets & DDoS Infrastructure

Attackers build botnets using:

Malware

Worms

Phishing

Botnets communicate through:

IRC

HTTP/S

P2P Command & Control

Used to launch large-scale DDoS attacks.

4. DoS/DDoS Attack Tools
DoS Tools

Hping3

LOIC (Low Orbit Ion Cannon)

HOIC (High Orbit Ion Cannon)

DDoS Tools

Botnet-based scripts

Trinoo

TFN/TFN2K

Stacheldraht

5. Defense Against DoS/DDoS
Network-Level Protection

Firewalls with rate limiting

IDS/IPS to detect abnormal traffic

Blackholing or sinkholing

Anycast network routing (used by Cloudflare)

Application-Level Protection

WAF (Web Application Firewall)

CAPTCHA / Request throttling

Load balancers

Cloud-Based DDoS Protection Services

Cloudflare

Akamai

AWS Shield

Google Cloud Armor

6. Incident Response for DoS/DDoS

Identify attack type and traffic pattern

Block malicious IPs or ranges

Inform ISP or upstream provider

Redirect traffic to scrubbing centers

Apply long-term rate limits and filtering rules

7. Key Concepts

Amplification: Attackers use vulnerable services to multiply attack volume.

Reflection: Spoofed source IP makes third-party servers flood the victim.

Spoofing: Faking IP addresses to hide attacker identity.

Slow-rate attacks: Consume resources with very slow requests (Slowloris).
