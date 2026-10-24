# Week 17: 11th - 24th October 2026

## What I covered this week
- Domain 3.1 cold-audit and lessons
- Practice questions simulation across domains 1-3.1 (15 questions, 15 mins timer)
- **iac.md** log (concept-notes)
- Tryhackme OS basics - Intro to OS room
- Exam target decision
- Minimum viable review (3.1)
  
## Most significant concept I learned
Infrastructure as code: defining infrastructure (servers, networks, storage) as machine readable config-files (run by tools like Terraform, Ansible, CloudFormation) instead of manual configuration. It is fast, consistent, and repeatable making it a good choice for version control (an audit trail of who changed what and when) and ease of deployment. The security concern: it makes it possible to deploy to thousands of machines at a time, but errors or hardcoded API secrets scale at the same rate. A single line of error doesn't affect one server, it affects thousands of servers at a time.

## Most useful confusion I resolved
Wasn't able to tell how logical segmentation differs from physical isolation. While they're related, thought they're the same thing. Resolved: Logical segmentation uses software defined rules (ACLs, firewalls, VPNs) to isolate systems, networks or devices separate from each other. Physical isolation is total physical separation - different servers, different data centers, different locations - it's the last mile of segmentation, makes remote attacks extremely difficult but is very expensive, and introduces more security complexity (managing multiple servers from multiple locations manually). 

## Most significant realization
Recency is not retention: after 6 weeks of understanding and reviewing SSl stripping, was confident I've retained it enough to log under concept-notes. Completely forgot what it even is now, and defaulted to logging IaC because it's the recent one in my memory. 

## Honest reflection on the week
Exam date target decided on the 14th - SY0-701 by the end of April 2027 with a checkpoint of completing Domains 3 and 4 by 15th January (which is about 12 objectives in 13 weeks, about 0.9 per week). If I hit it, I book the exam for April, if I miss it I switch to SY0-801 and a date around Q3, 2027 - which means domain 1-3 work carries over. The week also has no carryovers - 3.1 self-audit and lesson on the 12th and 13th, practice questions (scored 14/15 and got most of the concepts I struggled with in previous sims right - the category confusion pattern is weakening) and iac.md log (two days pass) on the 19th and 20th, and tryhackme Intro to OS room on 22nd. Aman was put put on hold on 18th, so no external deadlines from the venture now. 2 days were blocked by a family operational issue (16th & 17th) and a day was lost to a 24-hour electricity crisis and Malltiply ad management setup took priority throughout the rest of the day (23rd). 

Review days: 15th, 21st

Gap days: 16th, 17th, 23rd

Excused Sundays: 11th, 18th

## Next week focus
- First-time practice exams from Domain 1-2 overall
- Tryhackme - Computer fundamentals continuation (at least 2 rooms)
- One concept-notes log (non-negotiable)
