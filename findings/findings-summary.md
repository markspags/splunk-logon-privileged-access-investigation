# Findings Summary

## Overview
This investigation reviewed Windows Security Event Logs in Splunk to analyze successful authentication activity and determine whether a privileged session was created.

## Key Events Reviewed
- EventCode 4624: Successful logon
- EventCode 4672: Special privileges assigned to new logon

## Findings
A successful logon event was identified in Splunk and reviewed for account name, logon type, source details, and general context. A separate search for EventCode 4672 showed that a privileged session was also recorded.

Reviewing both event types together showed how a successful authentication can be correlated with privileged access assignment in a Windows environment.

## Risk Assessment
Based on the available evidence in this lab, the observed activity appeared consistent with expected local or administrative usage. No clear malicious behavior was identified.

## Why This Matters
This case demonstrates:
- basic Splunk log analysis
- familiarity with Windows event IDs
- event correlation across authentication and privilege events
- structured documentation of investigative findings
