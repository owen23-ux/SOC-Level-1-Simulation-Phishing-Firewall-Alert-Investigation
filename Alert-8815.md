# Case Report – Event ID 8815

## Incident Classification

| Field | Information |
|-------|-------------|
| Alert ID | 8815 |
| Alert Rule | Inbound Email Containing Suspicious External Link |
| Incident Type | Phishing |
| Severity Level | Medium |
| Date and Time Detected | May 3rd 2026 at 19:32 |
| Time of Activity | Pending – need email timestamp |

## Classification

- [x] True Positive
- [ ] False Positive

## List of Affected Entities

- Recipient: (to be identified from email details)
- Source IP: (to be identified from firewall logs if user clicked)

## Reason for Classifying as True Positive

This is a suspected phishing email based on the alert rule. The email contains one or more external links with potentially suspicious characteristics. This alert was triggered at 19:32, one minute before Alert 8816 (firewall block at 19:33). These may be related to the same phishing campaign.

## Investigation Steps Taken

1. Alert was triggered for inbound email containing suspicious external link
2. Need to review email content for red flags
3. Need to search Splunk firewall logs for connections to any domains found
4. Need to check if the recipient is the same as Alert 8817 (c.allen)

## Correlation with Other Alerts

| Alert ID | Time | Type | Possible Relation |
|----------|------|------|-------------------|
| 8814 | 19:28 | Phishing | Same campaign |
| 8815 | 19:32 | Phishing | Same campaign |
| 8816 | 19:33 | Firewall (Blocked) | User clicked different link |
| 8817 | 19:34 | Phishing (Clicked) | User c.allen clicked |
| 8818 | 19:34 | Phishing | Same campaign |

**Timeline:**
