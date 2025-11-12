
Module 3 — Scanning Networks (CEH v13)
Objective

Learn methods and tools to discover live hosts, open ports, running services and OS details on a target network. This module teaches safe, effective scanning strategies and how to interpret scan results to plan further assessment steps.

Description

Network scanning is the active reconnaissance phase where you probe targets discovered during footprinting to build an accurate inventory of hosts, services and potential entry points. This module covers host discovery, port/service scanning, version and OS fingerprinting, scan tuning and basic vulnerability identification. It also explains ethics, legal considerations and techniques to avoid disrupting production systems.

Key Learning Outcomes

After completing this module you will be able to:

Distinguish host discovery vs port scanning vs service/OS fingerprinting.

Perform safe host discovery (ARP, ICMP, TCP) and large-scale discovery (Masscan).

Conduct detailed port and service scans (TCP/UDP), and interpret results.

Identify service versions and OS fingerprints to prioritise further testing.

Understand scan timing, throttling, and stealth/evasion tradeoffs.

Recognize false positives and scan artefacts.

Apply countermeasures and defensive controls to detect/mitigate scanning.

Techniques Covered

Host discovery: ICMP echo, TCP SYN ping, ARP scans, broadcast discovery.

Port scanning: TCP SYN (-sS), TCP connect (-sT), UDP (-sU), NULL/FIN/XMAS scans.

Service/version detection and banner grabbing.

OS fingerprinting and TTL/window analysis.

Stealth and timing: adjusting scan speed, fragmenting packets, use of decoys.

Large-scale scanning and rate-limited discovery.

Interpreting scan output and correlating with footprinting data.

Common Tools
PurposeToolsPort & service scansNmap, Masscan, NetcatGUI / visualZenmapUDP scanningNmap -sU, hping3Large-scale discoveryMasscanVulnerability probeNessus, OpenVAS, NiktoARP / local discoveryarp-scan, NetdiscoverBanner grabbingNetcat, Telnet, curlScan automationRustScan, AutoRecon, NSE scripts (Nmap Scripting Engine)

Example Lab Tasks (step-by-step flow)


Host discovery


Local network: arp-scan -l or nmap -sn 192.168.1.0/24


Remote: nmap -Pn -PS80,443 target.com (TCP SYN ping)




Basic TCP port scan


nmap -sS -p- -T4 10.10.10.5 (SYN scan, all ports, faster timing)




Service/version detection


nmap -sV -p22,80,443 --version-intensity 5 target.com




UDP scan (careful: slow)


nmap -sU -p53,123,161 -T3 target.com




OS fingerprinting


nmap -O target.com (requires privileges; may be inaccurate behind firewalls)




Run Nmap scripts for additional info


nmap -sV --script vuln 10.10.10.5




Large-scale scan (non-intrusive tuning)


masscan 10.0.0.0/8 -p80,443 --rate=1000 (rate tune to avoid DoS)




Correlate results with footprinting and prepare findings (open services, versions, suspicious banners).



Example Nmap Command Cheat-Sheet


nmap -sn 192.168.1.0/24 — ping/host discovery only.


nmap -sS -p- -T4 10.10.10.5 — SYN scan all ports with faster timing.


nmap -sV -oA scan-results 10.10.10.5 — service/version detection, save results.


nmap -sU -p- 10.10.10.5 — UDP full port scan (very slow).


nmap -O --osscan-guess 10.10.10.5 — OS detection with guesswork enabled.


nmap --script "default or safe" -p80,443 target.com — run selected NSE scripts.



Deliverables


Module-03 Report (PDF/Markdown): Goals, command list, screenshots, parsed output, analysis.


Raw scan outputs: .nmap, .xml, and .gnmap files exported from Nmap.


Evidence folder: screenshots of scans, logs, and timelines.


Risk summary: open services with version, potential vulnerabilities, exploitability rating.


Recommendations: immediate remediations (close unused ports, patch services, apply ACLs, IDS tuning).



Countermeasures & Defensive Notes


Implement ingress/egress firewall rules and host-based firewalls.


Use network segmentation and reduce exposed services.


Deploy IDS/IPS signatures for scanning patterns and anomalous rates.


Rate-limit connections, enable port knocking or VPN-only admin access.


Monitor logs for unusual port-scan behavior and tune alert thresholds.



Safety & Legal Reminder
Always obtain explicit authorization before scanning systems you do not own. Scanning without permission may be illegal and could cause service disruption.

Want this as a ready-to-drop README.md file for Module-03-Scanning/ (Markdown) so you can upload straight to GitHub? I can generate that now.


