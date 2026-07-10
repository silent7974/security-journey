# Week 06: 3rd July – 10th July 2026

## What I covered this week
- Completed Messer on the rest of 2.2 
- Domain 2.3 self-audit and lessons
- Watched Messer (Memory injection, Buffer overflow, Race conditions, Malicious updates, OS vulnerabilities)
- Tryhackme Activities (Module 2 final room walkthrough - "Extending your networking", Module 3 first room - "DNS in Details" (free room))
- Domain 1.3 review (minimum viable day)
- Complete re-audit

## Most significant concept I learned
Race conditions describes the time it takes for a function to run sequentially. TOC - time-of-check is the time it takes to verify something, while TOU - time of use is the time it takes to act based on that verification. A finance system verifies and update a deposit to an account balance faster than a withdrawal, attackers take advantage of the delay. The 2004 Mars rover spirit is an example - where a race condition bug caused a reboot loop in a file system, engineers on earth had to fix it remotely. Another example is Pwn2Own Vancouver 2023, Tesla Model 3 where a tesla was breached - race conditions are everywhere and could cause serious problems. 

## Most useful confusion I resolved
Genuinely confused zero day with zero trust. Zero trust is ensuring parties within trusted zones also get verified always. Zero day are existing vulnerabilities that are unknown to vendors, attackers discover them first and they're extremely valuable because they could be sold to nation-state levels or organized crimes on dark markets. Completely different concepts.

## Honest reflection on the week
Best week yet actually, 5 real sessions (Messer videos, 2.3 audit and lessons, tryhackme activities), 1 minimum viable day on 4th due to an exhausted afternoon - reviewed domain 1.3, and 1 gap day - Malltiply received its first sale and the day was consumed by the emotional weight of that milestone.

## Standout re-audit moment
During the 2.3 re-audit, retained SolarWinds 2020 Orion (malicious update), 2013 Target credit card breach (service provider), Mars rover Spirit 2004 (race condition), and Pwn2Own 2023 Tesla (race condition) across a 5-day gap with no Messer on most of 2.3 yet. Real-world examples are sticking better than definitions.

## Re-audit results
Retained:
Buffer overflow, race conditions, malicious updates, EOL, legacy, sideloading, jailbreaking, misconfiguration, hardware provider concept, software provider.
 
Non-retained/needs sharpening:
Memory injection, TOC/TOU definition, OS-based vulnerabilities, SQLi, XSS, firmware, VM escape, resource reuse, service provider target breach example, cryptographic vulnerabilities, 

Corrections from re-audit:
Memory injection: not OS infection generally. Memory injection is forcing malicious code into a running process's memory space. DLL injection is the main example - malicious code runs inside a legitimate process like explorer.exe, inheriting its permissions and hiding from security tools. The OS isn't the target, a specific running process is.

TOC/TOU definition: TOC is Time-Of-Check when the system verifies something. TOU is Time-Of-Use when the system acts on that verification. The attack exploits the gap between those two moments.

OS-based vulnerabilities: OS code has millions of lines meaning inevitable undiscovered vulnerabilities. Patch Tuesday is Microsoft's monthly patch cycle addressing discovered OS vulnerabilities. EternalBlue is the famous example - NSA-developed Windows SMB exploit used by WannaCry ransomware. Always patch, have a backout plan, test before deployment.

SQLi: SQLi is inserting malicious SQL code into an input field to manipulate the database query. Classic example: entering ' OR '1'='1 into a login field makes the query always true, bypassing authentication entirely.

XSS: "affects the visitor" is too vague. XSS injects malicious scripts into a webpage that execute in the visitor's browser with the trust of the legitimate site. It can steal session cookies, capture keystrokes, redirect users. Stored XSS is saved in the database and hits every visitor. Reflected XSS is in a URL the victim clicks.

Firmware: "second class devices" is wrong. Firmware is low-level software embedded directly into hardware - routers, printers, cameras, medical devices. It runs below the OS meaning OS security tools can't detect firmware-level attacks. Rarely updated, almost never checked. Compromised router firmware means invisible traffic interception.

VM escape: An attacker breaks out of an isolated VM to access the host system or other VMs on the same physical hardware. Catastrophic in cloud environments where thousands of customers share hardware. One escaped VM could reach another customer's data.

Resource reuse: It's not credentials specifically, it's any residual data (files, memory contents, stored data) from a previous tenant that wasn't properly wiped before reassignment. An attacker assigned old storage recovers whatever wasn't sanitized.

Service provider (Target breach): 2013 Target credit card breach. Attackers compromised an HVAC vendor (MSP/service provider), pivoted into Target's network, reached POS systems across all stores, stole 40 million credit card numbers.

Cryptographic vulnerabilities: weak algorithms and leaked keys are right but incomplete. Others are short key lengths vulnerable to brute force, deprecated protocols (SSL, TLS 1.0), implementation flaws like Heartbleed where a bug in OpenSSL allowed memory contents to be read despite strong encryption.
 
## Next week focus
- Watch the rest of Messer on 2.3
- Complete tryhackme module 3
- Domain 2.4 self-audit and lessons
