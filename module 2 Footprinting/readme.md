🧭 Module 2 – Footprinting and Reconnaissance
Objective

The objective of this module is to gather preliminary information about a target organization or system using both passive and active reconnaissance techniques. This phase helps ethical hackers identify potential entry points and understand the target’s digital footprint before conducting active assessments.

Description

Footprinting, also known as reconnaissance, is the first phase of ethical hacking. In this phase, the attacker or security professional collects as much information as possible about a target to understand its network, systems, and security posture.

This module focuses on the methods, tools, and strategies used to collect intelligence from publicly available sources (OSINT) and how to perform active probing safely. It also covers how to analyze and document the information gathered for future attack phases.

Key Learning Outcomes

After completing this module, learners will be able to:

Understand the importance and scope of footprinting in ethical hacking.

Differentiate between passive and active information-gathering techniques.

Perform OSINT (Open Source Intelligence) using various online tools and databases.

Conduct WHOIS lookups, DNS enumeration, and email footprinting.

Identify target infrastructure using search engines, social media, and public repositories.

Map network ranges, domains, and subdomains.

Recognize countermeasures to prevent or minimize footprinting activities.

Techniques Covered

WHOIS and DNS information gathering

Subdomain enumeration

Email footprinting and tracking

Website mirroring and metadata analysis

Google hacking / dorking

Social media reconnaissance

Network range and IP identification

Shodan, Censys, and Recon-NG scanning

Footprinting through job postings and public documents

Common Tools Used
Category	Tool Name	Purpose
OSINT Search	Maltego, Recon-NG, theHarvester	Information aggregation
Domain Info	whois, dnsenum, nslookup, dig	Domain and DNS record enumeration
Web Info	Wappalyzer, BuiltWith, HTTrack	Technology profiling and website cloning
Network Footprinting	Nmap, Shodan, Censys	Port scanning and asset discovery
Social Media	Social-Searcher, SpiderFoot, Sherlock	Username and profile intelligence

Lab Tasks (Example Flow)

Perform WHOIS lookup to identify domain registration details.

Use dnsenum or dig to collect DNS records and subdomains.

Conduct Google dorking to find sensitive information exposed online.

Extract metadata from publicly available documents (e.g., PDF, DOCX).

Perform email footprinting using theHarvester and hunter.io.

Analyze gathered data to map target infrastructure.

Document findings and identify possible attack vectors.

Deliverables

Footprinting Report (PDF or Markdown): Includes collected data, analysis, screenshots, and tools used.

Screenshots Folder: Evidence of OSINT and reconnaissance activities.

Tool Commands File: Command syntax used during the lab.

Summary Section: Observations and possible mitigation strategies.

Countermeasures

Use of privacy protection services for domain registration.

Limiting public exposure of system details and sensitive metadata.

Implementing banner-grabbing prevention and rate-limiting.

Monitoring search engine indexing for leaked data.

Regular OSINT audits to identify unintentional data exposure.

Conclusion

Footprinting is the foundation of every penetration test and ethical hacking engagement. A detailed understanding of reconnaissance enables professionals to anticipate attacker behavior, identify weaknesses early, and strengthen an organization’s external defense posture.
