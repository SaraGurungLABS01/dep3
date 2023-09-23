## Post-Incident Report

## Incident Summary:
On September 23, 2023, at 9:00 AM, an incident occurred that resulted in downtime and malfunctioning of our URL shortener tool, which had a significant impact on our SLA with Nike. This report provides an overview of the incident, its causes, the duration of the disruption, the actions taken for resolution, the final status, and preventive measures to avoid a recurrence.

## 1. Reason for the Incident:
The incident was caused by a new hire deploying version 2 of our URL shortener application by committing directly to the main branch. This triggered an automatic deployment that replaced version 1 in production. The primary reasons for the incident were:

Direct Commit to Main Branch: Version 2 of the application was committed directly to the main branch without proper review and testing, leading to unexpected issues.
## 2. Duration of Downtime:
The URL shortener experienced downtime for a total of 5 minutes during this incident. The downtime began immediately after the deployment of version 2 and continued for this duration.
