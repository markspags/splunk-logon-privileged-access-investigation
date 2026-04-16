# splunk-logon-privileged-access-investigation
Hands-on cybersecurity lab analyzing Windows authentication events in Splunk to investigate successful logons and privileged access activity, with OSINT enrichment using SpiderFoot to demonstrate risk-based investigative workflows.

## Tools Used
- Splunk (Log Analysis)
- SpiderFoot (OSINT Enrichment)

## Investigation Summary
A successful logon event (EventCode 4624) was identified and analyzed. The session was reviewed for context including logon type, account usage, and source details. Correlation with EventCode 4672 confirmed that elevated privileges were assigned to the session.

## Key Questions Answered
- Who logged in?
- When did the logon occur?
- What type of authentication was used?
- Was privileged access granted?
- Does the activity appear expected or risky?

## OSINT Enrichment
SpiderFoot was used to demonstrate how external indicators such as IP addresses can be enriched with:
- Ownership data
- Geolocation
- Reputation signals

## Conclusion
The activity observed was consistent with expected local system usage. This project demonstrates how Splunk can be used to analyze authentication events and how OSINT tools can enhance investigative context.
