# SpiderFoot Findings

## Objective
Demonstrate how OSINT enrichment can support log-based investigations by adding context to an IP address or external indicator.

## Method
SpiderFoot was used to scan an IP address and collect contextual information such as:
- ownership / ASN data
- geolocation
- reputation-related information
- related internet-facing data points

## Findings
The SpiderFoot scan provided a summary view of the selected IP address and showed how analysts can quickly gather external context that may support further investigation.

## Analyst Note
In this lab, SpiderFoot is included to demonstrate enrichment methodology. Even when Splunk logs do not contain a clearly suspicious external IP, the workflow shows how OSINT can support a real-world investigation when an unfamiliar indicator is identified.
