# Week 10: 6th - 11th August 2026

## What I covered this week
- Domain 2.4 self-audit & lessons - Malware attacks, Physical attacks, Network attacks, Application attacks, Cryptographic attacks, Password attacks and Indicators
- Messer videos - Overview of malware, Viruses and worms
  
## Most significant concept I learned
Fileless virus chain: gets executed when the user performs a specific function (clicking a link), exploits OS vulnerability, uses legitimate tools (Powershell, WMI) to write scripts to memory, controls the memory to write more scripts to apps or exfiltrate data, creates auto-start entry to registry to start its process again and maintain persistence after a reboot all without touching disks. Bypasses traditional anti-virus/anti-malware scanners. It requires memory forensics and behavioral analysis, not file inspections. 

## Most useful confusion I resolved
Thought a virus or a ransomware alone can cause a major attack. Resolved: malware usually work together not as a single tool; a malicious link infected with a virus, the virus creating a backdoor on victim's system, the backdoor installing a RAT to enable remote control, attacker use the RAT to run a ransomware that encrypts file system. Every single tool playing its role, it's how every major malware attack works. The Wannacry ransomware is an example: a worm uses EternalBlue vulnerability to scan for vulnerable SMBv1 port 445, creates a backdoor that installs a ransomware that encrypts the file system on victim's device, propagates across other vulnerable systems on the same network, and repeats the same process.

## Honest reflection on the week
20 minutes review held on every minimum viable day, no gap days. Had to study for a carry over test on 6th but reviewed domain 2.1, went to write the test on 7th (school errand day - legit reason even for reviews). Extended morning disruption affecting lessons again on the 8th and 9th - overstimulation keeping me awake at night due to Malltiply's weight, reviewed 2.2 and 2.3. Domain 2.4 self-audit and lessons on the 10th and watched 2 Messer videos on 11th (Malware, viruses and worms). No tryhackme activity, haven't done that in a while. 

Review days: 6th, 8th and 9th August.  

School: 7th August.

## Standout re-audit moment
Did the 2.4 re-audit of Messer reinforced concepts only, scored 62% with honest self-rating. 

### External factors affecting execution
Extended morning disruption on 8th and 9th August due to Malltiply's weight at night.

## Re-audit results
Retained: WannaCry chain (minus the initial vector error), worm vs virus distinction, malware protection fundamentals (mostly).

Needs sharpening: Virus types incomplete, boot sector misnamed, WannaCry initial vector wrong.

Non-retained(blank): Fileless chain.

Corrections from re-audit:

WannaCry spread via SMB scanning, not email phishing. No user clicked anything. That's what made it devastating.

The five virus types: program, boot sector, script, macro, fileless.

Fileless infection chain: link → exploit → PowerShell → memory-only execution → registry persistence.

Boot sector, not "bootless."

## Next week focus
- Messer on 2.4 - Other malwares, physical attacks, wireless attacks
- Tryhackme - Computer fundamentals (non-negotiable)
