# Week 17: 11th - 24th October 2026

## What I covered this week
- Domain 3.1 cold-audit and lessons
- Practice questions simulation across domains 1-3.1 (15 questions, 15 mins timer)
- **iac.md** log (concept-notes)
- Tryhackme OS basics - Intro to OS room
- Exam target decision
- Minimum viable review (3.1)
  
## Most significant concept I learned
Infrastructure as code: defining infrastructure (servers, networks, storage) as machine readable config-files (run by tools like Terraform, Ansible, CloudFormation) instead of manual configuration. It is fast, consistent and repeatable, and because the templates live in version control, every change leaves an audit trail of who changed what and when. The security concern: it makes it possible to deploy to thousands of machines at a time, but errors or hardcoded API secrets scale at the same rate. A single line of error doesn't affect one server, it affects thousands of servers at a time.

## Most useful confusion I resolved
Wasn't able to tell how logical segmentation differs from physical isolation. While they're related, thought they're the same thing. Resolved: Logical segmentation uses software defined rules (ACLs, firewalls, VLANs) to isolate systems, networks or devices separate from each other. Physical isolation is total physical separation - different servers, different data centers, different locations - it’s the extreme end of segmentation, makes remote attacks extremely difficult but is very expensive, and introduces more security complexity (managing multiple servers from multiple locations manually). 

## Most significant realization
Recency is not retention: after 6 weeks of understanding and reviewing SSL stripping, was confident I've retained it enough to log under concept-notes. Completely forgot what it even is now, and defaulted to logging IaC because it's the recent one in my memory. So retention has to be tested with cold recall on older material, not judged by how familiar it feels.

## Honest reflection on the week
Exam date target decided on the 14th - SY0-701 by the end of April 2027 with a checkpoint of completing Domains 3 and 4 by 15th January (which is about 12 objectives in 13 weeks, about 0.9 per week). If I hit it, I book the exam for April, if I miss it I switch to SY0-801 and a date around Q3, 2027 - which means domain 1-3 work carries over. Every item on last week’s plan list was completed: the 3.1 self-audit and lessons on the 12th and 13th, the practice simulation and iac.md (two passes) on the 19th and 20th, and a TryHackMe Intro to OS room on the 22nd. Aman was put on hold on the 18th. The 16th and 17th were blocked by a family operational issue. The 14th and 21st were hit by 24-hour electricity cuts (the 21st still held a review). The 23rd was lost to the recurring extended morning disruption, then Malltiply ad-account setup took the rest of the day.

Active days: 12th, 13th, 19th, 20th, 22nd

Review days: 15th, 21st

Other: 14th (exam target decision, no review)

Gap days: 16th, 17th, 23rd

Excused Sundays: 11th, 18th

## Practice result
Got 14/15 with 1.07mins to spare and got most of the concepts I struggled with in previous sims right - the category confusion pattern is weakening (the set deliberately re-tested earlier misses, so this shows the corrections held, not general readiness). The one question missed is choosing phishing for a smishing scenario.

Correction from result:
Phishing is the umbrella term and, in its narrow sense, means deceptive emails with a malicious link. Smishing is the same attack delivered by SMS, and vishing by voice call. When a scenario names the channel, the exam wants the channel-specific term.

### External factors affecting execution
Family operational issue, electricity cuts (14th, 21st), the recurring extended morning disruption (21st, 23rd), Malltiply ad management, and a friend visiting (15th).

## Next week focus
- Messer sessions on 3.1
- Domain 3.2 cold audit and lessons (Checkpoint: 0/12)
- Practice questions simulation across domains 1-3.1
- Tryhackme OS basics (at least 2 rooms)
- One concept-notes log
- Cold-recall check on 3 older concepts (SSL stripping first)
- Weekly log capped at 10 days (closes by 3rd November)
- Sunday exempted from execution
