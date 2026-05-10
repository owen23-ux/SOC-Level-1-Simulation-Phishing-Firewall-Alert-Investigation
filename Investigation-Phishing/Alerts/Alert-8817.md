# Case Report – Alert 8817

## Alert Details

| Field | Information |
|-------|-------------|
| Alert ID | 8817 |
| Alert Rule | Inbound Email Containing Suspicious External Link |
| Severity | Medium |
| Type | Phishing |
| Date & Time Detected | May 3rd 2026 at 19:34 |
| Datasource | email |
| Email Timestamp | 05/03/2026 19:32:24.173 |
| Sender | no-reply@m1crossoftsupport.co |
| Recipient | c.allen@thetrydaily.thm |
| Subject | Unusual Sign-In Activity on Your Microsoft Account |
| Attachment | None |

## Email Content

> Hi C.Allen,
>
> We detected an unusual sign-in attempt on your Microsoft account.
>
> Location: Lagos, Nigeria
> IP Address: 102.89.222.143
> Date: 2025-01-24 06:42
>
> If this was not you, please secure your account immediately to avoid unauthorized access.
>
> Review Activity
>
> Thank you,
> Microsoft Account Security Team

## Investigation Steps

### Step 1: Email Analysis

I analysed the email for phishing indicators:

| Indicator | Finding | Verdict |
|-----------|---------|---------|
| Sender domain | m1crossoftsupport.co (fake) | Suspicious |
| Link domain | m1crossoftsupport.co/login | Suspicious |
| Urgency | "Secure your account immediately" | Scare tactic |
| Legitimate Microsoft? | No – uses number "1" instead of "i" | Fake |

**Conclusion:** This is a phishing email attempting to steal Microsoft credentials.

### Step 2: Domain Reputation Check

I checked the domain `m1crossoftsupport.co` on VirusTotal:

| Result | Finding |
|--------|---------|
| Malicious verdict | 0/92 security vendors flagged it |
| Community Score | 0 |
| Last Analysis | 11 days ago |

**Note:** The domain was not flagged because it is new or low-volume. Lack of detection does not mean it is safe.

### Step 3: Firewall Log Investigation (SIEM/Splunk)

I searched firewall logs for connections to the phishing domain:

| Search Query | Finding |
|--------------|---------|
| `url="*m1crossoftsupport*"` | 1 connection found |

**Log Entry Found:**
