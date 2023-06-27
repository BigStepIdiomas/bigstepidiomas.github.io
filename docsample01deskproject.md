---
layout: default
title: Project Docs
description: There will be docs...
---

<style>
.tag {
  display: inline-block;
  padding: 4px 8px;
  border-radius: 4px;
  color: #fff;
  font-size: 14px;
  font-weight: bold;
  margin-right: 8px;
  margin-bottom: 10px;
}

/* Add the background colors for each category */
.tag:nth-child(4) { background-color: #ffc107; } /* Technical Documentation */
.tag:nth-child(5) { background-color: #6f42c1; } /* Knowledge Base */
.tag:nth-child(7) { background-color: #20c997; } /* English */
.tag:nth-child(12) { background-color: #90ee90; } /* Support Docs */
.tag:nth-child(13) { background-color: #ff6666; } /* Project Docs */

</style>


<span class="tag" style="background-color: #ffc107;">Technical Documentation</span>
<span class="tag" style="background-color: #6f42c1;">Knowledge Base</span>
<span class="tag" style="background-color: #20c997;">English</span>
<span class="tag" style="background-color: #90ee90;">Support Docs</span>
<span class="tag" style="background-color: #ff6666;">Project Docs</span>



# DoxHut's HelpDesk Project

![intro](images-projectdesk-intro.png)

### Project Info
- Problem Statement
- Scope
- Timeline
- Milestones and deadlines
- Reference materials

## Project Info

![info](images-projectdesk-fichainfo.png)

## Problem Statement
Currently, there is no 1st or 2nd level Support at DoxHut that we can provide to our customers nor an established or defined process our customers must follow to receive the necessary help when facing technical issues or assistance requests.

## Scope

- Must have:
  - Ticketing System
  - Defined workflow
  - Mailing tool
  - Custom ticket fields
  - Agents assignment
  - Dashboards and metrics views
  - Support for customer feedback
  - 1st Level Direct Phone Line
  - Help Desk / Support Portal
  - Support ticket submission for anonymous users
  - Support knowledge base access
  - Basic 1st Level Support
    - Defined workflow
    - DRIs for analyzing and addressing tickets
    - DRIs for maintaining the Help desk
    - DRIs for 1st Level communication
    - Support Documentation
  - Basic 2nd Level Support
    - Defined workflow
    - DRIs for analyzing and resolving tickets
    - DRIs for 2nd Level communication
    - Support Documentation
  - Incident Management Procedure
  - Runbooks / Playbooks
  - Oncall SREs / Field Technicians schedule
  - Defined official channels for communication
  - Weekly follow-up meetings 
  - Incident Management Handbook / Runbooks / Playbooks
  - Support Documentation

- Nice to have:
  - Calling Tool (suitable when escalating)
  - Metrics
  - DRI/s (hiring when/if necessary)
  - FAQ / Troubleshooting Docs 
  - Customer Service Feedback Surveys
  - Ticket migration FreshDesk to Jira / (Integration) 

- Not in scope:

## Timeline

![Timeline](timeline-project-desk.png)

| Milestone               | Owner                                        | Deadline | Status           |
|-------------------------|----------------------------------------------|----------|------------------|
| Set up FreshDesk solution    | Include/cover all elements from Must Have | TBD      | IN PROGRESS      |
| Define roles             | Define 1st                                  | TBD      | PENDING APPROVAL |
|                          | Define 2nd                                  |          |                  |
| Assign responsibilities  | Train and onboard collaborators             | TBD      |                  |
| Create documentation     | Incident Management Docs                    | TBD      | IN PROGRESS      |
|                          | Troubleshooting Docs for Field Technicians  |          |                  |
|                          | Runbooks / Playbooks                         |          |                  |
|                          | FAQ/Help Docs for Help Desk Portal          |          |                  |
| Help Desk Pilot          | Kickoff                                     | TBD      | PENDING APPROVAL |
|                          | Assess Results                              |          |                  |
| Analyze FreshDesk Upgrade|                                              | TBD      |                  |
| Calling Tool             | Analyze feasibility                         | TBD      |                  |
|                          | Analyze hiring DRI/s for wider coverage      |          |                  |
| SLA                      | Definition                                  | TBD      | PENDING APPROVAL |
|                          | Documentation                               |          |                  |
| Metrics                  | Analyze Pilot Results and Define Metrics     | TBD      | PENDING APPROVAL |
|                          | Define goals                                |          |                  |
|                          | Define means for communicating customer      |          |                  |
|                          | (e.g., Dashboards/KPI via email)             |          |                  |

## Reference Material
- Incident Management Project
- Incident Management Handbook
- Runbooks
- FreshDesk Implementation Blueprint
- FreshDesk Documentation
- Helpdesk - Customer Portal


[back](./)