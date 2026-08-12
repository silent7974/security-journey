# Week 09: 27th July - 5th August 2026

## What I covered this week
- Watched Messer: supply chain, misconfiguration, mobile device and zero day vulnerabilities
- 2.3 full re-audit
  
## Most significant concept I learned
The credit card breach - November, 2013 (the full picture): a phishing email was sent to a HVAC firm and someone opened the software, the HVAC firm network gets compromised and was used to get to the target's network, the target had the POS and the HVAC on the same network without segmentation, lateral movement was possible for the attacker and 40 million credit card were stolen while it took months for the compromise to be detected. The lesson; supply chain risk is not only IT, an attacker could gain unintended access through any supply chain related to your system - even though in this example a network segmentation could've contained the breach.

## Most useful confusion I resolved
Resource reuse: thought the resource being reused are just details like emails, passwords, tokens. Resolved it: while those are correct, resource reuse is about any residual data - memory contents, disk storage, cached files from a previous VM that wasn't sanitized not just credentials. The risk is a new tenant assigned the same physical resources can recover whatever was left behind. Could be proprietary code, encryption keys, database fragments.

## Honest reflection on the week
Planned the last 2-3 days of every month ending for recovery (a break from monthly executions and cognitive tasks) which was 29th-31st July, the 20-minutes review was supposed to survive those days but life hit with critical cold and fever which made it harder. 2 days gap again due to morning drifts on the 2nd and 3rd August, and 4th was another school errand day. Watched Messer on the 27th and 28th, then full 2.3 re-audit on 1st August.

Planned recovery: 29th-31st July. 

Gap days: 2nd-3rd August. 

School: 4th August.

## Standout re-audit moment
Did a cold audit after 3 days of illness with no reviews and scored 68% with honest self-rating.

### External factors affecting execution
Extended morning disruption on 2nd and 3rd August, affecting TryHackMe session and weekly log timing.

## Re-audit results
Retained: Memory injection, race conditions, malicious updates, XSS, firmware, supply chain, mobile device, zero day. 

Needs sharpening (concepts are there but precision drifts): SQLi syntax, VM escape chain, resource reuse, cloud-specific, crypto vulnerabilities.

Non-retained(blank): Buffer overflow return address, EternalBlue, Mirai botnet.

Corrections from re-audit:

Buffer overflow return address: The attacker overwrites the return address on the stack, not another variable. By controlling where the program goes next, they redirect execution to their own malicious code. Variable-to-variable overflow (Messer's diagram) is the teaching example. Return address overwrite is the real attack.

EternalBlue: NSA-developed Windows SMB exploit, leaked by Shadow Brokers in 2017, used by WannaCry ransomware to spread globally in hours. MS17-010 was the patch. One of the most famous OS vulnerabilities in history. 

SQLi syntax: The query explanation is close but syntactically imprecise. The actual query becomes: SELECT * FROM users WHERE username='' OR '1'='1' AND password='' OR '1'='1'. The '1'='1' is always true, so the WHERE clause returns everything.

Pwn2Own 2017 VM escape chain: JavaScript engine bug in Edge → escape browser sandbox → exploit Windows 10 kernel → gain full guest OS access → exploit VMware hypervisor bug → hop between VMs. Missed the sandbox escape step and the guest OS access step. 5 layers, not 3-4. 

Resource reuse: Said emails, passwords, tokens. Close but too narrow. Resource reuse is about any residual data - memory contents, disk storage, cached files - from a previous VM tenant that wasn't sanitized. The risk is a new tenant assigned the same physical resources can recover whatever was left behind. Not just credentials. Could be proprietary code, encryption keys, database fragments.

Cloud-specific vuln: Named two. The third is authentication bypass/directory traversal, and the fourth is remote code execution (Log4j, out-of-bounds write). Verizon S3 story correct. Gap: add Log4Shell by name or the 76% no-MFA stat.

crypto vuln: Three named: short keys, weak randomness, weak algorithms. All valid. Missing: deprecated protocols (SSL, TLS 1.0), implementation flaws (Heartbleed), downgrade attacks. The ones named are algorithm weaknesses. The missing ones are protocol and implementation weaknesses. Different categories.

Mirai botnet: Not firmware. Mirai was a botnet that scanned the internet for IoT devices (cameras, routers, DVRs) still using default credentials. It had a list of 60+ default username/password pairs. Once infected, those devices became part of a botnet used for massive DDoS attacks. The 2016 Dyn DNS attack took down major websites. This is a misconfiguration vulnerability - default credentials left unchanged. 

## Next week focus
- Domain 2.4 audit and lessons
- Tryhackme - Computer fundamentals
