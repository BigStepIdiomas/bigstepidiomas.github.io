---
layout: default
title: Templates - Blog Postmortem Notice
description: What're ya buyin?
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
.tag:nth-child(1) { background-color: #007bff; } /* UX Writing */
.tag:nth-child(2) { background-color: #28a745; } /* Technical Specification */
.tag:nth-child(3) { background-color: #dc3545; } /* API Docs */
.tag:nth-child(4) { background-color: #ffc107; } /* Technical Documentation */
.tag:nth-child(5) { background-color: #6f42c1; } /* Knowledge Base */
.tag:nth-child(6) { background-color: #fd7e14; } /* Translation */
.tag:nth-child(7) { background-color: #20c997; } /* English */
.tag:nth-child(8) { background-color: #e83e8c; } /* Installation Guides */
.tag:nth-child(9) { background-color: #6c757d; } /* Help Docs */
.tag:nth-child(10) { background-color: #17a2b8; } /* Troubleshooting */
.tag:nth-child(11) { background-color: #87ceeb; } /* Handbooks */
.tag:nth-child(12) { background-color: #90ee90; } /* Support Docs */
.tag:nth-child(13) { background-color: #ff6666; } /* Project Docs */
.tag:nth-child(14) { background-color: #ffff99; } /* Portuguese */
.tag:nth-child(15) { background-color: #d291bc; } /* Release Notes */
.tag:nth-child(16) { background-color: #ffb347; } /* German */
.tag:nth-child(17) { background-color: #98d8d8; } /* SDK */
.tag:nth-child(18) { background-color: #ffb6c1; } /* Product Discovery */
.tag:nth-child(19) { background-color: #d3d3d3; } /* UX Design */
.tag:nth-child(20) { background-color: #afeeee; } /* Spanish */
.tag:nth-child(21) { background-color: #cd853f; } /* Copywriting */
.tag:nth-child(22) { background-color: #ffa07a; } /* Microcopy */
.tag:nth-child(23) { background-color: #f08080; } /* Educational Material */
.tag:nth-child(24) { background-color: #da70d6; } /* Localization */
.tag:nth-child(25) { background-color: #8470ff; } /* User Guides */
</style>

<span class="tag" style="background-color: #007bff;">UX Writing</span>
<span class="tag" style="background-color: #28a745;">Technical Specification</span>
<span class="tag" style="background-color: #dc3545;">API Docs</span>
<span class="tag" style="background-color: #ffc107;">Technical Documentation</span>
<span class="tag" style="background-color: #6f42c1;">Knowledge Base</span>
<span class="tag" style="background-color: #fd7e14;">Translation</span>
<span class="tag" style="background-color: #20c997;">English</span>
<span class="tag" style="background-color: #e83e8c;">Installation Guides</span>
<span class="tag" style="background-color: #6c757d;">Help Docs</span>
<span class="tag" style="background-color: #17a2b8;">Troubleshooting</span>
<span class="tag" style="background-color: #87ceeb;">Handbooks</span>
<span class="tag" style="background-color: #90ee90;">Support Docs</span>
<span class="tag" style="background-color: #ff6666;">Project Docs</span>
<span class="tag" style="background-color: #ff6666;">Portuguese</span>
<span class="tag" style="background-color: #d291bc;">Release Notes</span>
<span class="tag" style="background-color: #ffb347;">German</span>
<span class="tag" style="background-color: #98d8d8;">SDK</span>
<span class="tag" style="background-color: #ffb6c1;">Product Discovery</span>
<span class="tag" style="background-color: #d3d3d3;">UX Design</span>
<span class="tag" style="background-color: #afeeee;">Spanish</span>
<span class="tag" style="background-color: #cd853f;">Copywriting</span>
<span class="tag" style="background-color: #ffa07a;">Microcopy</span>
<span class="tag" style="background-color: #f08080;">Educational Material</span>
<span class="tag" style="background-color: #da70d6;">Localization</span>
<span class="tag" style="background-color: #8470ff;">User Guides</span>

> Template from: [Michael Kehoe](https://michael-kehoe.io/post/postmortem-template/)

# Postmortem Template

## Summary
| Incident Summary     |             | Incident Severity       |             |
| -------------------- | ----------- | ----------------------- | ----------- |
| Incident Number      |             | War-room Required       |             |
| Postmortem Date      |             | SRE Lead                |             |
| Developer Lead       |             | Incident Mgmt Lead      |             |
| Chaos Eng Preventable|             | Postmortem Lead         |             |
| Recording            |             |                         |             |

## Postmortem Attendees
| Name                 | Role        | In attendance |
| -------------------- | ----------- | ------------- |
| John Doe             |             |               |
| Jane Smith           |             |               |
| Alice Johnson        |             |               |

## Incident Timing
| Start Time           |             | Incident Detected By (User-reported/Ad-hoc monitoring/Alerting system) |             |
| -------------------- | ----------- | ----------------------------------------------------------------------- | ----------- |
| Detection Time       |             | Time to Detect (TTD)                                                  |             |
| Mitigation Time      |             | Time to Mitigate (TTM)                                                |             |
| Resolution Time      |             | Time to Resolve (TTR)                                                 |             |

## Incident Timeline
| Date/Time            | Who/What    | Action/Impact |
| -------------------- | ------------| --------------|
| Jan 1, 9:00 AM       |             |               |
| Jan 1, 10:30 AM      |             |               |
| Jan 1, 11:45 AM      |             |               |

## Impact

### End User Impact

### Infrastructure Impact

### Productivity Impact

## What caused the incident?

### Trigger(s)

### Process Breakdown(s)

### Root Cause(s)

## Mitigation & Resolution

## Open Questions
| Person               | Question/Answer |
| -------------------- | --------------- |
| Q (who): A (who):    |                 |
| Q (who): A (who):    |                 |
| Q (who): A (who):    |                 |

## Lessons Learned

### What went well

### What went badly

### Where did we get lucky

## Action Items & Follow-ups
| Action Item          | Type (Mitigate/Prevent/Process/Other) | Who             | Priority | Bug # | Due Date |
| -------------------- | ------------------------------------- | --------------- | -------- | ----- | -------- |
| Fix bug in API       |                                     | John Doe        | High     | #1234 | Jan 10   |
| Update firewall      |                                     | Jane Smith      | Medium   | #5678 | Jan 15   |
| Review procedures    |                                     | Alice Johnson   | Low      | #9101 | Jan 20   |

## Supporting Documents



[Back](./)