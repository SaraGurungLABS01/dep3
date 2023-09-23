## Post-Incident Report

## Incident Summary:
On September 23, 2023, at 9:00 AM, an incident occurred that resulted in downtime and malfunctioning of our URL shortener tool, which had a significant impact on our SLA with Nike. This report provides an overview of the incident, its causes, the duration of the disruption, the actions taken for resolution, the final status, and preventive measures to avoid a recurrence.

## 1. Reason for the Incident:
The incident was caused by a new hire deploying version 2 of our URL shortener application by committing directly to the main branch. This triggered an automatic deployment that replaced version 1 in production. The primary reasons for the incident were:

Direct Commit to Main Branch: Version 2 of the application was committed directly to the main branch without proper review and testing, leading to unexpected issues.
## 2. Duration of Downtime:
The URL shortener experienced downtime for a total of 5 minutes during this incident. The downtime began immediately after the deployment of version 2 and continued for this duration.
## 3. Steps Taken to Resolve the Incident:
Upon detection of the incident and the email alert, our incident response team initiated the following step to resolve the situation:

Rollback to Version 1: As version 1 of the application was known to be stable, we initiated a rollback procedure to revert to the previous version. This rollback successfully restored the functioning of the URL shortener.
##             Steps:

 ## Create a New Branch: 
 A new branch was created using the command git checkout -b <branch name> <commit hash ID>, which contained only the version 1 commit
 ## Changes to the file:
 test_app.py : Fixed the typo in the test_app.py file 
 application.py : Fixed the typo. 

 ![image](https://github.com/SaraGurungLABS01/dep3/assets/140760966/ca9dc69c-9f74-4e74-84a2-ab7bd2a93106)

## Git add and Push
Saving the Changes:

a. $ git add . - All changes made during the rollback process were staged for commit.

b. $ git commit -m "Made Changes to Files in Dep3 File" - A commit was made to save the changes made during the rollback process, with a descriptive commit message.

c. $ git push -u origin main - The changes were pushed to the main branch on the remote repository to ensure that the known good version 1 code was now in production.

## 4. Status of Incident Resolution:
The incident was successfully resolved after the rollback to the last known good commit of version 1, and the URL shortener tool is now operational without any issues. Full functionality was restored, and no further disruptions have been reported.

![image](https://github.com/SaraGurungLABS01/dep3/assets/140760966/20b78212-bbc0-4047-ad81-bff51f51c5df)


## 5. Preventive Measures:
To prevent a similar incident from occurring in the future, we will implement the following preventive measures:

a. Branching and Code Review: We will enforce a branching strategy that requires code changes to be reviewed and tested in dedicated branches before being merged into the main branch.

b. Rollback Plan: We will establish a clear and well-documented rollback plan that can be executed swiftly in case of any issues during deployment, including specific procedures for rolling back to a known good commit.



    
