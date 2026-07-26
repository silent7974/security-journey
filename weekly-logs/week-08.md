# Week 08: 18th July – 26th July 2026

## What I covered this week
- Watched Messer: SQLi, XSS, Hardware, Virtualization, and Cloud-specific vulnerablities

## Most significant concept I learned
VM escape: Every VM is isolated from other VM's and the local machine hosting them. A VM escape is when an attacker makes it out of his isolated VM to other ones and the local machine. This is catastrophic to cloud environment where thousands of VM's share a single physical device. The Pwn2Own competetion 2017 - where the participants found a bug in the javascript engine of microsoft edge, bypassed the browsers sandboxing, exploited a vulnerability in windows 10 kernel, created guests in the operating system, gained access to the hypervisor and to other VM's. The point is it's a chain across multiple layers not just a single exploit.

## Most useful confusion I resolved
Reflected XSS vs Stored XSS: thought it's a differentiation between sharing malicious links to individuals vs posted publicly via social media. Understood now; while reflected XSS is a crafted malicious link that looks legitimate shared via email, messaging or social media platforms to individuals - their browsers gets infected and runs the script. Stored XSS infects the database of the target website, anyone who visits the site falls victim. 

## Honest reflection on the week

[Gap days and minimum viable days as usual]

### External factors affecting execution
[Malltiply discovery, family dynamics, anything real 
that affected the week — honest, not self-pitying]

## Standout re-audit moment


## Re-audit results
Retained:
Non-retained/needs sharpening:
Corrections from re-audit:

## Next week focus
