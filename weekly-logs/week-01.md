# Week 01: 16th May – 21st May 2026

## What I covered this week
- CompTIA SY0-701 exam objectives: Domain 1.1 - security controls (categories; technical, operational, managerial and physical & control types: preventive, deterrent, detective, compensating, corrective and directive) & Domain 1.2 - core security concepts (CIA, AAA, Authorization models, non-repudiation, gap analysis, zero trust, physical security and deception & disruption)
- Watched Professor Messer on everything covered; from security controls down to deception & disruption.
- Completed self-audit on each topic before the lessons to identify learning gaps


## Most significant concept I learned
Deception & disruption is a tactic used by security professionals to design or build fake assets in a way that makes them look attractive, tricking an attacker into targeting those systems and costing them time and resources while they're quietly being identified. Honeypot is creating a fake device or system, a honeynet is building a network of honeypots (aims to target large number of attackers), honeyfile is dressing a fake file in real ones and making it more attractive (like passwords.txt) and honeytoken is creating fake credentials (like API tokens, database records) an authorized user will almost always have nothing to do with those credentials, who ever access them gets flagged as unauthorized.


## Most useful confusion I resolved
Never fully differentiated hashing from encryption, used to think they're the same thing. Resolved it: hashing is an integrity mechanism used to detect whether data has been modified and is irreversible. Encryption on the other hand is a confidentiality mechanism used to hide a message and can be reversed (seen) by an authorized party using a key.


## Honest reflection on the week
Mostly remembering words and lessons I've already had contact with in college, but some are completely new to me. Scenario tests throughout the week confirmed understanding held under applied pressure, not just in theory. The sessions are covered 2 hours a day between 2pm - 4pm which an hour was lost to exhaustion (slept midway watching zero-trust on professor Messer on 18th) and an hour was lost to attending to conversations with unexpected guest (on 19th). Few professor Messer key points were consumed without proper retention due to the exhaustion (on 19th) and no jottings (across all videos) mostly relying on memory.


## Re-audit summary
Security controls are the measures organizations take for protection against attacks; the categories tells us where it falls under and the control types tells us what type it is. The compensating control type is when the ideal security control can not be implemented due to a constraint, so a different type is implemented. The CIA is the most basic concept of security; where confidentiality means ensuring protection from unauthorized parties, integrity means ensuring data has not being altered with or deleted in storage or in transit and availability means ensuring resources are available whenever authorized parties need access. Non-repudiation is ensuring actions can not be denied by parties, gap analysis is measuring current security posture with a standard requirement, and zero trust is an approach of ensuring verification not only for unknown parties, but with trusted and known ones as well. The control plane is the part that makes decisions for granting, denying or revoking access and consists of a policy engine, policy administration, adaptive identity, threat scope reduction and policy-driven access control (it acts as the brain), while the data plane is that part that enforces the decisions of the control plane and consists of the PEP, subject and implicit trust zones (acts as the muscle). Security professionals don't only focus on the digital space, but the physical one as well - physical security focuses on security devices or just things that can be touched or used to protect the physical space (bollards, fencing, lighting, sensors, video surveillance, access-control vestibules). Deception and disruption is an approach to trick attackers by creating and making fake assets that looks attractive using honeypots, honeynets, honeyfiles or honeytokens depending on the goal.

## Next week focus
- Self-audit and lessons on Domain 1.3 and 1.4 (with Professor Messer)
- TryHackMe Pre-Security path
