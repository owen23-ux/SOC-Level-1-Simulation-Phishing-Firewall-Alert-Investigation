# Case Report – Alert 8817

## Incident Classification: True Positive

## Time of Activity
05/03/2026 19:35:10.217 (link clicked)

## Affected Entities
C. Allen (c.allen@thetrydaily.thm) – Source IP 10.20.2.25

## Reason for True Positive
- Fake sender domain: m1crossoftsupport.co (not microsoft.com)
- Phishing email using scare tactics about unusual sign-in activity
- Firewall logs confirm user clicked the link at 19:35:10.217
- Connection was ALLOWED (not blocked)

## Escalation Required: YES

## Reason for Escalation
The user clicked the phishing link and the firewall allowed the connection. The user may have entered credentials on the fake Microsoft login page.

## Recommended Remediation Actions
1. Force password reset for c.allen's account immediately
2. Enable MFA if available
3. Scan workstation (10.20.2.25) for malware
4. Block domain: m1crossoftsupport.co
5. Educate user on phishing indicators
6. Monitor account for 30 days

## Attack Indicators
| Indicator | Value |
|-----------|-------|
| Sender | no-reply@m1crossoftsupport.co |
| Recipient | c.allen@thetrydaily.thm |
| Malicious URL | https://m1crossoftsupport.co/login |
| Source IP | 10.20.2.25 |
| Destination IP | 45.148.10.131 |
| Firewall Action | Allowed |
