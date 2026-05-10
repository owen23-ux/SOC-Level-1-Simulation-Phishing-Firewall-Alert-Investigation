# SOC Analyst Phishing Investigation – TryHackMe Simulation

## Overview
This project documents my investigation of two security alerts from the TryHackMe SOC Immersive Simulation - Introduction to Phishing.

## Alerts Investigated

| Alert ID | Type | Severity | Classification |
|----------|------|----------|----------------|
| 8816 | Firewall Block | High | True Positive |
| 8817 | Phishing Email | Medium | True Positive |

## Key Findings

### Alert 8816
- User at 10.20.2.17 attempted to access a malicious bit.ly link
- Firewall BLOCKED the connection
- VirusTotal: 1/93 vendors flagged as phishing
- **No escalation needed** – firewall did its job

### Alert 8817
- User C. Allen received phishing email from fake Microsoft domain
- User CLICKED the link at 19:35:10
- Firewall ALLOWED the connection to fake login page
- **Escalation REQUIRED** – potential credential theft

## Tools Used
- Splunk (SIEM) for firewall log analysis
- VirusTotal for URL and domain reputation checks
- TryHackMe SOC Simulator

## Lessons Learned
1. A blocked connection (Alert 8816) is less urgent than an allowed connection to a malicious site (Alert 8817)
2. Always check firewall logs to confirm if a user clicked a phishing link
3. Different source IPs may indicate different users – investigate each separately
4. Document everything – screenshots, timestamps, and rationale

## Author
Owen Maake – Aspiring SOC L1 Analyst

## Date
May 2026
