Module 11: Evading IDS, Firewalls, and Honeypots

Overview

This module focuses on techniques attackers use to bypass network security defenses such as IDS (Intrusion Detection Systems), IPS (Intrusion Prevention Systems), firewalls, and honeypots. You will learn how evasion works, what weaknesses exist in detection systems, and how to defend networks from stealthy attacks.

🎯 Learning Objectives

Understand how IDS, IPS, firewalls, and honeypots work

Learn packet-level evasion techniques

Discover how attackers bypass filtering and detection rules

Study firewall architecture and weaknesses

Analyze honeypot behavior and detection methods

Learn defensive strategies and mitigation

🧱 Security Devices Covered
1. IDS (Intrusion Detection System)

Network IDS (NIDS)

Host-based IDS (HIDS)

Signature-based & anomaly-based detection

2. Firewalls

Packet filtering

Stateful inspection

Application-aware firewalls

NGFW (Next-Generation Firewall)

3. Honeypots

Low-interaction

High-interaction

Honeytokens

Honeynets

🚀 Evasion Techniques
1. Packet-Level Evasion

Fragmentation of payloads

Overlapping TCP segments

Manipulating TTL values

Source routing

Invalid checksums

Tools: Nmap, hping3, Scapy


3. Firewall Evasion Techniques

Source IP spoofing

Port hopping

MAC spoofing

Using proxy servers & VPNs

Reverse shells to bypass inbound rules

Application-layer manipulation

Outbound connection abuse using allowed ports (80/443)

4. IDS/IPS Evasion Techniques

Polymorphic shellcode

Encrypting payloads

Traffic padding

Inserting benign data in attack payload

Evasion using whitespace, URL encoding, Unicode encoding

Slow-rate attacks (Slowloris)

5. Honeypot Detection

Identifying low-interaction honeypots

Detecting virtualization/emulation

Fingerprinting honeyd or tarpits

Checking for unusual service responses

Timing analysis (delayed responses)

Tools: nmap, honeyd, kippo, cymothoa

🧰 Common Tools Used
Category	Tools
Scanning / Evasion	Nmap, Hping3, Scapy
Obfuscation	Veil, Hyperion, Shellter
Tunneling	DNSCat2, Iodine, ICMP tunnels
Firewall Testing	Firewalk, FOCA
Honeypots	Honeyd, Kippo, Dionaea, Cowrie
🛡️ Countermeasures
1. For IDS/IPS

Enable anomaly + signature-based rules

Use SSL inspection for encrypted traffic

Packet normalization (defragmentation, TTL fixes)

2. For Firewalls

Proper outbound filtering

Disable unused ports/services

Implement zone-based architecture

Enforce strong access control lists (ACLs)

3. For Honeypots

Integrate with SIEM

Use deception systems in layered defense

Place honeypots in DMZ or isolated subnets

4. General Hardening

Update signatures regularly

Use threat intel and behavioral monitoring

Log analysis and correlation

Block tunneling protocols unless required
