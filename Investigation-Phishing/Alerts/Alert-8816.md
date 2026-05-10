# Alert 8816 – Access to Blacklisted External URL Blocked by Firewall

## Basic Information

| Field | Value |
|-------|-------|
| Alert ID | 8816 |
| Alert Rule | Access to Blacklisted External URL Blocked by Firewall |
| Severity | High |
| Type | Firewall |
| Date and Time Detected | May 3rd 2026 at 19:33 |
| Status | Complete – Closed |

## Investigation Details

| Field | Value |
|-------|-------|
| Datasource | firewall |
| Timestamp | 05/03/2026 19:31:20.173 |
| Action | blocked |
| Source IP | 10.20.2.17 |
| Source Port | 34257 |
| Destination IP | 67.199.248.11 |
| Destination Port | 80 |
| URL | http://bit.ly/3sHkX3da12340 |
| Application | web-browsing |
| Protocol | TCP |
| Rule | Blocked Websites |

## Threat Intelligence

| Check | Result |
|-------|--------|
| VirusTotal | 1/93 security vendors flagged as malicious |
| Category | Phishing |

## Classification

| Field | Answer |
|-------|--------|
| True Positive or False Positive? | True Positive |
| Does this alert require escalation? | NO |

## Reason for Classification

The destination URL (http://bit.ly/3sHkX3da12340) triggered a firewall block rule because it is listed in the organization's threat intelligence blacklist. Bit.ly links are commonly used in phishing attacks to disguise malicious destinations. The firewall successfully blocked the connection, preventing any damage.

## Remediation Actions

1. Block the full bit.ly redirect domain at the proxy level
2. Scan source workstation (10.20.2.17) for malware or other infections
3. Educate the user about phishing risks and not clicking unknown links
4. Check if the user entered any credentials on any suspicious pages
5. Monitor the source IP for additional suspicious outbound attempts

## Attack Indicators (IOCs)

- Source IP: 10.20.2.17
- Destination IP: 67.199.248.11
- Destination Port: 80 (HTTP)
- URL: http://bit.ly/3sHkX3da12340
- Protocol: TCP
- Firewall rule: Blocked Websites

## Case Report

See `Reports/Case-Report-8816.md` for full case report.
