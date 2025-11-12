Module 08 — Sniffing (CEH v13)
Objective

Understand network sniffing techniques and tools to capture, analyze, and interpret network traffic for reconnaissance and incident investigation — and learn how to harden networks to detect and prevent sniffing attacks.

Description

Sniffing (packet capturing) is the process of intercepting and logging traffic that passes over a network. This module covers both passive and active sniffing techniques, how attackers harvest sensitive data (credentials, session tokens, clear-text traffic), and how defenders can detect and mitigate these threats. Hands-on labs show how to capture packets, analyze protocols, and extract useful intelligence while emphasising safe, authorised testing in isolated environments.

Key Learning Outcomes

After completing this module you will be able to:

Explain how sniffing works at different layers (link, network, transport).

Differentiate passive sniffing (promiscuous mode) from active attacks (ARP spoofing, MAC flooding, MitM).

Use packet capture tools to collect and analyze traffic, extract credentials, and identify suspicious communications.

Understand protocol-specific risks (HTTP, FTP, SMTP, Telnet) and how encryption (TLS, SSH) mitigates them.

Perform LAN-based sniffing techniques (ARP poisoning, DHCP spoofing) in lab environments.

Implement network defenses: encryption, port security, 802.1X, monitoring, and segmentation.

Techniques Covered

Promiscuous mode and packet capture basics.

Passive capture from span/mirror ports and network taps.

Active sniffing: ARP poisoning/ARP spoofing, MITM via Ettercap/Responder, DHCP spoofing.

SSL/TLS interception concepts (transparent proxies, explicit proxying) — theory and defensive considerations.

Extracting credentials and session tokens from clear-text protocols.

Packet filtering and pattern matching to locate IOCs.

Traffic reassembly for files, HTTP streams, and protocol analysis.

Common Tools
Purpose	Tools / Examples
Packet capture & analysis	Wireshark, tcpdump
ARP spoofing / MITM	Ettercap, Bettercap, mitmproxy
Credential capture & hash harvesting	Responder, Wireshark filters, dsniff
Network taps / mirroring	tcpdump on SPAN port, network TAP devices
SSL/TLS inspection	mitmproxy, corporate TLS proxies (lab only, with consent)
Automation / scripting	tshark, scapy, Python for parsing pcaps
Example Lab Tasks (step-by-step)

Setup — Use an isolated lab switch or virtual network with a span/mirror port or network tap.

Passive capture — Run tcpdump/Wireshark on a mirror port and capture baseline traffic.

Filter & analyze — Use Wireshark display filters to find HTTP credentials, DNS queries, and suspicious connections.

ARP poisoning (lab-only, authorised) — Launch ARP spoofing with Ettercap/Bettercap to intercept traffic between two VMs (document risks).

Extract clear-text secrets — Locate HTTP POSTs, FTP credentials, or basic-auth headers in captures (redact real secrets in reports).

DNS / SMB poisoning with Responder — Identify LLMNR/NetBIOS-name service weaknesses that leak credentials (lab-only).

TLS/HTTPS observation — Demonstrate why encryption prevents credential disclosure; show SNI, certificate inspection.

Capture analysis — Reassemble HTTP streams or files from pcap; export artifacts for reporting.

Cleanup — Revert ARP table changes and remove any lab artifacts.

Deliverables

Module-08-Sniffing/README.md — module summary, objectives, and safe lab rules.

sniffing-lab-report.pdf — findings, screenshots from Wireshark, filters used, parsed outputs, and lessons learned.

captures/ — sample pcaps (sanitised/anonymised).

commands.txt — exact commands and Wireshark filters.

evidence/ — screenshots, extracted artifacts (redacted), and timelines.

mitigations.md — short checklist for defenders.

Countermeasures & Hardening

Use end-to-end encryption (HTTPS, SSH, TLS) to protect sensitive data in transit.

Disable insecure clear-text protocols (Telnet, FTP) or tunnel them through secure channels.

Implement 802.1X, port security, MAC filtering and dynamic ARP inspection on switches.

Use VLAN segmentation and avoid flat networks that allow easy sniffing.

Monitor for ARP anomalies and unusual traffic patterns (IDS/IPS signatures).

Use network TAPs/SPAN for monitoring instead of relying on host-based promiscuous captures.

Enforce HSTS, secure cookies, and session management to reduce session theft risk.

Legal & Safety Reminder

Only perform sniffing and any active MITM attacks with explicit written authorization. Sniffing is privacy-sensitive — treat captured data as confidential, redact or anonymize personal data in reports, and follow organisational policies and legal requiremen
