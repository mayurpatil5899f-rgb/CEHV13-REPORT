Module 09 — Social Engineering (CEH v13)
Objective

Understand the human element of security: learn how attackers manipulate people to disclose information or perform actions, and learn practical defensive strategies to detect, prevent, and respond to social engineering attacks.

Description

Social engineering is the art of exploiting human psychology rather than technical flaws to breach security. This module covers social-engineering methodologies (pretexting, impersonation, phishing, baiting, quid pro quo, tailgating), how to design and conduct ethical social-engineering assessments, how to capture evidence, and how to build awareness and technical controls to reduce human risk. Emphasis is on legal/ethical constraints, safe lab simulations, and measurable awareness metrics.

Key Learning Outcomes

After completing this module, learners will be able to:

Define social engineering and explain why humans are often the weakest link.

Distinguish social-engineering techniques (phishing, vishing, smishing, pretexting, baiting, physical social engineering).

Perform controlled, ethical social-engineering assessments (scoping, approvals, safe templates).

Design and run phishing simulations and awareness campaigns safely and legally.

Recognize psychological principles attackers use (authority, urgency, reciprocity, social proof, scarcity).

Identify detection, response, and mitigation measures — both technical and behavioural.

Produce reports with metrics (click rates, credential submission rates, improvement over time).

Techniques Covered

Pretexting and vishing (voice-based social engineering).

Phishing (spear-phishing, whaling), smishing (SMS phishing) and clone-phishing.

Baiting (physical media like USB drops) and quid pro quo.

Tailgating and piggybacking for physical access.

Authority & urgency exploitation in messaging.

Information harvesting from social media and OSINT to craft convincing pretexts.

Social-engineering automation tools and safe simulation platforms.

Measuring effectiveness: KPIs and awareness improvement plans.

Common Tools & Platforms
Purpose	Tools / Examples
Phishing simulation	GoPhish, PhishTool, King Phisher
Awareness & training	KnowBe4, Cofense Triage (lab exercises)
OSINT for pretexting	LinkedIn, Twitter, Google, Pipl, Hunter.io
Telephony & vishing	SIP test setups, controlled call scripts (lab-only)
Physical test kits	Badge printing (simulated), USB test files (lab)
Tracking & metrics	Campaign dashboards, CSV exports, ticketing for remediation
Example Lab Tasks (ethical, scoped, and authorized)

Scope & Approval

Obtain written authorization, define allowed targets, exclusions, and success metrics.

OSINT & Pretext Creation

Gather public information to craft believable emails or phone scripts (no harvesting of private data).

Phishing Simulation (lab)

Build a GoPhish campaign with a safe landing page that captures only simulated credentials or a click metric.

Vishing Exercise (lab)

Use scripted calls to request non-sensitive verification (e.g., confirm a meeting time) to measure susceptibility.

Physical Social Test (lab)

Controlled tailgating test at an office entrance using escorts and consented observers.

Baiting Simulation (lab)

Leave clearly labelled inert USB sticks and measure pickup/reporting rates (do NOT use real malware).

Awareness Campaign

Deliver training, then re-run simulations to measure improvement and produce KPIs.

Reporting & Remediation

Produce executive and technical reports, recommend targeted training and policy changes.

Deliverables

Module-09 Report (PDF/Markdown): campaign plan, approvals, scripts, metrics, and remediation roadmap.

Campaign artifacts: email templates, call scripts, landing pages (sanitised).

Metrics dashboard: click rates, credential-submission rates (simulated), report-to-phish ratios.

Recommendations: awareness training plan, policy changes, technical controls.

Evidence folder: anonymised screenshots and logs showing campaign behaviour (respect privacy).

Countermeasures & Hardening

Security awareness training tailored to real threats and role-specific risks.

Phishing-resistant MFA (push, hardware tokens) to reduce credential compromise risk.

Email controls: DMARC/DKIM/SPF, anti-phishing filters, URL rewriting/sandboxing.

Phone-based protections: verification processes, call-back policies for sensitive requests.

Physical access controls: visitor escorts, badge checks, turnstiles, tailgating detection.

Incident playbooks and easy reporting mechanisms (single-click “Report Phish” buttons).

Regular, measured simulations with follow-up training and positive reinforcement.

Legal, Ethical & Safety Notes

Never conduct social-engineering tests without explicit written authorization from appropriate stakeholders.

Protect participant privacy — anonymise results and avoid real credential capture or exposure of personal data.

Use non-malicious artifacts (inert USBs, simulated credential pages) and document cleanup procedures.

Coordinate with HR, legal, and physical security teams before any exercise.

Focus on education and remediation, not punishment
