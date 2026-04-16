# Investigation Notes

## Investigation Goal
Review Windows Security logs in Splunk to identify successful authentication activity and determine whether the session was associated with privileged access.

## Approach
I began by searching for EventCode 4624 to identify successful logon events. From there, I reviewed available fields such as account name, logon type, source network address, and workstation name.

Next, I searched for EventCode 4672 to determine whether any successful sessions were granted elevated privileges. I then used a correlation search to review 4624 and 4672 events together in a timeline-style format.

## What I Looked For
- User account involved in the logon
- Timestamp of the activity
- Logon type
- Source network address, if available
- Whether a privileged access event followed the logon
- Whether the activity appeared normal in context

## Logon Type Reference
- 2 = Interactive logon
- 3 = Network logon
- 10 = Remote interactive logon

## Analyst Perspective
A successful logon is not suspicious by itself. The value comes from identifying who logged in, how they logged in, whether elevated privileges were granted, and whether the activity makes sense based on the system context.
