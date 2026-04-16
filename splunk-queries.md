# Splunk Queries

## Successful Logons
index=* EventCode=4624
| table _time host Account_Name Logon_Type Source_Network_Address Workstation_Name

## Privileged Logons
index=* EventCode=4672
| table _time host Account_Name Privilege_List

## Correlation Search
index=* (EventCode=4624 OR EventCode=4672)
| table _time EventCode Account_Name Logon_Type Source_Network_Address Privilege_List

## User-Focused Investigation
index=* (EventCode=4624 OR EventCode=4672) Account_Name="<USERNAME>"
| sort - _time
