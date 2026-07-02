# Week 05: 25th June – 2nd July 2026

## What I covered this week
- Domain 2.2 (Threat vectors & attack surfaces)
- Watched Messer on "Threat vectors"
- Complete re-audit 

## Most significant concept I learned
Removable devices - a USB drive infected with malware and dropped in a parking lot (curiosity makes people plug them in), rubber ducky - a device that looks like a USB drive that injects keystrokes at scale. They're mainly used to target organizations with air-gapped networks (networks with no internet connections), an organization spending millions of dollars on firewalls, IP systems can still be attacked with just a $10 USB drive. Stuxnet is an example of this; a USB drive infected with malware was used to attack air-gapped Iranian nuclear facilities.

## Most useful confusion I resolved
Misinformation/disinformation - I merged them into spreading false information to intentionally deceive someone. But that's just disinformation, misinformation is spreading false information without knowing it's false. 

## Honest reflection on the week
Best minimum viable day discipline yet, total new materials covered were just 2 days though; 2.2 self-audit and lessons on 27th and Messer on "Threat actors" on 29th. A day was lost with no review (1st July) While the rest of the days were all minimum viable days: 25th (mentally exhausted from income work + background fever), 26th (family and phone distractions), 28th (running errand to collect sister's products to upload in Malltiply - partly review at night that was interrupted by sleep), and 30th. Re-audit on the 2nd July. No tryhackme activities. 

## Standout re-audit moment
During the 2.2 re-audit, independently recalled combosquatting as an alternative to typosquatting, the SS7 protocol for SMS attacks, SIM-swap attacks under voice call vectors, and the watering hole predator analogy - none of which were in the original teaching session. These came from Messer retention, not prompted recall.

## Re-audit results
Retained:
All message-based vectors, image-based, file-based, voice call, removable devices, vulnerable software, unsupported systems, default credentials, supply chain (MSPs, vendors, suppliers), phising/vishing/smishing, impersonation, BEC, pretexting, watering hole, brand impersonation, typosquatting (with it's alternative - combosquatting).
 
Non-retained/needs sharpening:
Image parser attacks, unsecure networks (described just weak protocols choices; WPA vs WPA3, http vs https), open service ports (mentioned just ports opened intentionally), 2013 Target credit card breach (simply forgot the title), pretexting (couldn't give an organization scenario), misinformation/disinformation (couldn't differentiate).

Corrections from re-audit:
Image parser attacks: An image parser is the software that reads and processes image files. Attackers craft malicious images that exploit bugs in how the parser handles the file - the parser tries to read it, executes malicious code instead.

Unsecure networks: open/public WiFi with no encryption, Bluetooth vulnerabilities (bluejacking, bluesnarfing), and wired networks without proper segmentation. The attack surface is broader than just protocol weakness.

Open service ports:  The attack surface isn't just ports left open intentionally - it's also ports left open accidentally or forgotten after a service is decommissioned. Port scanning is how attackers find these. Nmap is the tool.

2013 target credit card breach (MSP example): Attackers compromised an HVAC vendor (MSP), pivoted through their access into Target's network, reached POS systems, stole 40 million credit card numbers. 

Pretexting(organization example) - an attacker calling IT helpdesk pretending to be a new employee who forgot their password.

Misinformation vs disinformation: misinformation is false information spread without knowing it's false. Disinformation is false information spread deliberately to deceive. The intent is the distinction. 
 
## Next week focus
- Complete Messer on 2.2
- Domain 2.3 audit and lessons
- Complete Tryhackme section 2 
