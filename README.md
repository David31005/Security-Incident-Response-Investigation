Security Incident Response Investigation

Project Overview

This cybersecurity portfolio project demonstrates a simulated Security Operations Center (SOC) investigation using Python, Pandas, Google Colab, and GitHub.

The investigation analyzes authentication logs, identifies suspicious login activity, reconstructs a security incident timeline, and generates an incident response report.

Project Type: SOC Analyst Training Lab
Incident ID: SOC-2026-001
Severity: High (Simulated)
Status: Investigation Required
Date: November 2, 2026

Project Objectives

* Analyze simulated authentication and security event logs.
* Identify patterns of potentially suspicious login activity.
* Detect repeated failed login attempts.
* Correlate successful logins with subsequent privilege changes.
* Reconstruct a chronological incident timeline.
* Document findings and recommended response actions.
* Demonstrate foundational SOC investigation and incident reporting skills.

Tools and Technologies

* Python: Security log processing and detection logic.
* Pandas: Filtering, grouping, and analyzing security events.
* Google Colab: Executing and documenting Python analysis.
* GitHub: Version control and cybersecurity portfolio documentation.
* CSV: Structured security event data.

Investigation Scenario

A simulated administrator account experienced multiple failed login attempts from the same source IP address.

Shortly afterward, the logs recorded a successful login and a privilege change associated with that IP address.

The sequence triggered a preliminary security investigation for possible brute-force activity and unauthorized access.

Investigated Indicators

Indicator	Finding
Source IP	203.0.113.45
Account	admin
Destination	Server-01
Failed login attempts	4
Successful logins	1
Privilege changes	1
Preliminary severity	High (Simulated)

The source IP belongs to a documentation-only address range. All activity is fictional.

Security Incident Timeline

Date and Time	Event
2026-11-02 09:05:00	Failed administrator login
2026-11-02 09:05:10	Failed administrator login
2026-11-02 09:05:20	Failed administrator login
2026-11-02 09:05:30	Failed administrator login
2026-11-02 09:06:00	Successful administrator login
2026-11-02 09:07:00	Privilege change recorded

Detection Methodology

The Python investigation used Pandas to load and analyze the simulated CSV security events.

The detection workflow:

1. Imported security logs from GitHub.
2. Filtered failed authentication events.
3. Counted failed logins by source IP address.
4. Flagged IP addresses with four or more failed login attempts.
5. Checked flagged IP addresses for successful login events.
6. Identified associated privilege change events.
7. Reconstructed a chronological incident timeline.
8. Generated a security incident report.

The detection threshold is a simplified training rule, not a validated production detection standard.

Investigation Findings

The analysis identified four failed administrator login attempts within 30 seconds from source IP 203.0.113.45.

A successful administrator login was recorded 30 seconds after the final failed attempt.

One minute later, a privilege change was recorded from the same source IP.

This sequence warrants further investigation because it may indicate attempted credential compromise followed by unauthorized activity.

However, the simulated evidence does not establish whether the successful login or privilege change was unauthorized.

Recommended Incident Response

Identification and Analysis

* Validate the security alerts against available authentication records.
* Determine whether the administrator login was authorized.
* Review additional endpoint, network, and privilege audit logs.
* Establish the scope of potentially affected systems and accounts.

Containment

* Preserve relevant evidence.
* If unauthorized access is confirmed, follow approved containment procedures.
* Revoke suspicious sessions or restrict account access when warranted.

Eradication and Recovery

* Reset affected credentials when appropriate.
* Review privileged access permissions.
* Remediate confirmed security weaknesses.
* Monitor systems for recurring suspicious activity.

Lessons Learned

* Review authentication monitoring and alert thresholds.
* Strengthen privileged account protection.
* Improve incident escalation and documentation procedures.

Project Files

* Incident_Response_Analysis.ipynb — Python investigation notebook.
* security_events.csv — Simulated security event dataset.
* incident_response_report.txt — Security incident report.
* README.md — Project documentation.

Skills Demonstrated

* SOC alert triage
* Security event log analysis
* Python scripting
* Pandas data analysis
* Authentication event correlation
* Potential brute-force activity detection
* Incident timeline reconstruction
* Preliminary severity assessment
* Incident response documentation
* GitHub project management

Project Limitations

This project uses a small, fictional dataset created for cybersecurity training.

The findings are based on simulated events rather than live network or endpoint telemetry. The detection logic demonstrates basic correlation but does not confirm an actual intrusion, account compromise, or privilege escalation.

Author

David Jeffries

Cybersecurity Portfolio | SOC Analyst Training Projects

GitHub: https://github.com/David31005

LinkedIn: https://www.linkedin.com/in/david-jeffries001

⸻

This project was developed for educational and cybersecurity portfolio purposes.
