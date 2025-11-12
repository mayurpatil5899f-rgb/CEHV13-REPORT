
Module 10 — Denial of Service (DoS) & Distributed Denial of Service (DDoS) (CEH v13)
Objective

Understand DoS and DDoS attack types, their mechanisms and impact, learn detection and mitigation techniques, and practise safe, authorized testing and simulation in controlled lab environments.

Description

Denial of Service (DoS) and Distributed Denial of Service (DDoS) attacks aim to disrupt the availability of systems, services, or networks by overwhelming resources (bandwidth, compute, memory, application limits) or exploiting protocol/implementation weaknesses. This module explains the attack vectors (volumetric, protocol, application), staging and orchestration methods, amplification/reflection techniques, botnet basics, and the operational and legal consequences of such attacks. Emphasis is on responsible handling — simulations only in isolated labs or with explicit authorization — and on designing resilient defenses and incident response plans.

Key Learning Outcomes

After completing this module you will be able to:

Differentiate DoS vs DDoS, and classify attacks by target layer (network, transport, application).

Identify common attack techniques: volumetric floods, protocol exploitation (SYN/ACK floods, UDP fragmentation), and application-layer floods (HTTP, slowloris).

Understand amplification/reflection attacks (DNS, NTP, memcached) and why misconfigured servers are dangerous.

Recognize botnet operation basics and command-and-control (C2) mechanisms used to run DDoS campaigns.

Detect early indicators of DoS/DDoS and tune monitoring to reduce false positives.

Design and apply mitigation strategies: traffic filtering, rate-limiting, scrubbing, CDN/WAF, and blackholing.

Prepare an incident response/playbook and recovery checklist for availability incidents.

Attack Types Covered

Volumetric attacks — saturate bandwidth (UDP floods, ICMP floods, greynoise).

Protocol attacks — exploit weaknesses in TCP/IP stack (SYN flood, TCP fragmentation, ACK flood).

Reflection & amplification — DNS amplification, NTP, Chargen, memcached amplification.

Application-layer attacks — slow POST/slowloris, HTTP floods, resource-exhaustion via expensive queries.

State-exhaustion attacks — connection table exhaustion on routers/firewalls/load balancers.

Multi-vector attacks — combinations to evade simple defenses.

Common Tools & Platforms (lab / defensive)
Purpose	Tools / Examples
Traffic generation / lab simulation	hping3, slowhttptest, LOIC (lab-only), httperf, Tsung
Protocol test	hping3, scapy (custom packets)
Load testing (simulated application flood)	siege, ab (ApacheBench), wrk
Monitoring & detection	ntop/ngrep, NetFlow/sFlow, Wireshark, Suricata, SIEM integration
Mitigation & protection	Cloud-based scrubbing services, CDN (Cloudflare/Akamai), WAF, load balancers
Reflection testing (lab-only, safe emulation)	Controlled DNS/NTP testbeds, local resolvers

Note: Tools that can be used for real-world DoS/DDoS must be used only in isolated labs or with explicit, written permission. Many of these tools are dual-use and illegal to run against third-party systems.

Example Lab Tasks (safe, controlled)

Understanding the baseline

Capture normal traffic metrics (bandwidth, connection counts, response times).

Simulate volumetric load in a lab

Use hping3 or wrk against an isolated test server to observe resource saturation effects.

Application-layer flood simulation

Use slowhttptest or wrk to simulate many slow or expensive HTTP requests and observe service behavior.

Protocol-level testing

Simulate SYN flood behavior in a closed network and watch TCP connection table exhaustion.

Reflection/amplification demo (emulated)

Demonstrate amplification concepts using a local resolver or controlled test servers — do not use public servers.

Monitoring & detection

Configure NetFlow/sFlow and SIEM rules to detect abnormal spikes; test alerting.

Mitigation exercise

Apply rate-limiting, ACLs, blackholing, or CDN-based protection in the lab and measure effectiveness.

Post-incident procedures

Run an IR runbook: containment, traffic reroute, notification, forensics (pcaps, logs) and recovery.

Indicators of Compromise / Detection Signals

Sudden, sustained spike in inbound traffic (bandwidth).

Rapid increase in new connections or half-open TCP sessions.

High CPU/memory usage on front-end servers or load balancers.

Increased SYN/ACK retransmissions and elevated packet loss.

Application errors (503/504), long response latencies, or resource timeouts.

NetFlow patterns showing many small sources to one destination (typical DDoS).

Mitigations & Defensive Strategies

Preparation & Architecture

Use geo-distributed infrastructure, CDNs, and scalable load balancers.

Harden internet-facing services and reduce attack surface (disable unused UDP services).

Network-level controls

BGP blackholing (as emergency), ACLs, rate-limiting at routers, Unicast RPF.

Application-level protections

WAF rules, CAPTCHA, connection throttling, caching, and efficient request handling.

Filtering & Scrubbing

Use ISP or cloud scrubbing centers to filter malicious traffic while preserving legitimate traffic.

Detection & Response

Baseline traffic, set thresholds/alerts, automate mitigation playbooks, and coordinate with upstream providers.

Post-attack remediation

Forensic capture (pcaps, flow logs), patch vulnerable reflectors, notify abused parties, and update runbooks.

Deliverables (for Module repo)

Module-10-DoS-DDoS/README.md — summary, objectives, safety rules, and TOC.

dos-lab-report.pdf — lab setup, scenarios, metrics, screenshots, and analysis.

pcaps/ — sanitized traffic captures demonstrating attack patterns (lab-only).

monitoring-rules.txt — example NetFlow/SNMP/SIEM detection rules or thresholds.

mitigation-playbook.md — sample incident response checklist and communication templates.

scripts/ — safe test scripts for lab load generation (annotated).

Legal, Safety & Ethical Notes

Launching DoS/DDoS attacks against third-party infrastructure is illegal and can cause severe harm — never perform outside an authorised lab or without written consent.

Use only isolated networks, VMs, or closed testbeds to simulate attacks.

Coordinate with your ISP, cloud provider, and legal/compliance teams when testing production resilience under approved conditions.

Maintain logs and evidence of authorization when conducting any resilience testing.
