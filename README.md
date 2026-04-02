# SOC-Failed-Login-Lab
Microsoft Sentinel SOC lab to detect failed login events using KQL queries.

### SOC Lab: Failed Login Detection using Microsoft Sentinel

## Project Overview
This project demonstrates a mini SOC lab setup where failed login attempts on a Windows VM are collected, monitored, and detected using **Microsoft Sentinel**.

## Tools & Technologies
- Microsoft Azure
- Microsoft Sentinel
- Windows VM
- KQL (Kusto Query Language)

## Workflow
1. Configure Windows VM to generate failed login events.
2. Collect Windows Security logs using Microsoft Sentinel.
3. Write **KQL queries** to detect brute-force login attempts (EventID 4625).
4. Create a **custom analytics rule** in Sentinel to generate incidents.
5. Validate the detection workflow.

## KQL Query Example
```kusto
SecurityEvent
| where EventID == 4625
| where TimeGenerated > ago(1h)


## Skills Demonstrated
- SIEM monitoring
- Microsoft Sentinel configuration
- Log analysis
- KQL queries
- Incident detection


