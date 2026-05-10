# Lessons Learned from This Investigation

## What I Learned

1. **Not all true positives are equal**
   - A blocked connection (8816) is less urgent than an allowed connection to a malicious site (8817)

2. **Firewall logs tell the full story**
   - Without Splunk logs, I would not know that C. Allen actually clicked the link

3. **Different source IPs = different users**
   - 10.20.2.17 (Alert 8816) vs 10.20.2.25 (Alert 8817) – investigate separately

4. **VirusTotal is not perfect**
   - The domain m1crossoftsupport.co showed 0/92 detections – but the email was clearly phishing

5. **Documentation is critical**
   - SOC L1 analysts must document everything: timestamps, IPs, URLs, actions taken

## Skills Demonstrated
- Phishing email analysis
- Firewall log investigation using Splunk
- VirusTotal reputation checking
- Incident classification (True Positive vs False Positive)
- Escalation decision making
- Case report writing
