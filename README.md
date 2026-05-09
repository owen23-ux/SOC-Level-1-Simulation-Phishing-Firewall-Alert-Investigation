# SOC Level 1 Simulation – Phishing & Firewall Alert Investigation

## Overview
This project documents my investigation of multiple SOC alerts from TryHackMe's SOC Immersive Simulation. The scenario involved phishing emails and a firewall block of a malicious URL.

## Key Findings
- Alert 8816: Firewall blocked connection to malicious bit.ly URL – No escalation needed
- Alert 8817: User clicked phishing link and firewall allowed connection – Escalated

## Tools Used
- TryHackMe SOC Simulator
- Splunk SIEM
- VirusTotal
- Firewall logs

## Skills Demonstrated
- Alert triage
- Log analysis
- Phishing investigation
- Threat intelligence
- Incident documentation

## Files
- `Alerts/` – Individual alert details
- `Evidence/` – Screenshots of logs and VirusTotal results
- `Reports/` – Complete case reports
- `Findings/` – Investigation summary

## Status
- 8816: ✅ Complete (True Positive – No Escalation)
- 8817: ✅ Complete (True Positive – Escalated)
- 8814, 8815, 8818: ⏳ Pending

## Author
Owen Maake – SOC L1 Candidate
