# Week 08: 18th July – 26th July 2026

## What I covered this week
- Watched Messer: SQLi, XSS, Hardware, Virtualization, and Cloud-specific vulnerablities
- 2.3 reviews on hard days

## Most significant concept I learned
VM escape: Every VM is isolated from other VM's and the local machine hosting them. A VM escape is when an attacker makes it out of his isolated VM to other ones and the local machine. This is catastrophic to cloud environment where thousands of VM's share a single physical device. The Pwn2Own competetion 2017 - where the participants found a bug in the javascript engine of microsoft edge, escape the browsers sandbox, exploited a vulnerability in windows 10 kernel, gained full guest OS access, exploited VMware hardware simulation bug, hopped between VM's on the same hypervisor. The key point is it's a chain across multiple layers not just a single exploit.

## Most useful confusion I resolved
Reflected XSS vs Stored XSS: thought it's a differentiation between sharing malicious links to individuals vs posted publicly via social media. Understood now; while reflected XSS is a crafted malicious link that looks legitimate shared via email, messaging or social media platforms to individuals - their browsers gets infected and runs the script. Stored XSS infects the database of the target website, anyone who visits the site falls victim. 

## Honest reflection on the week
Malltiply operations consuming learning sessions; uploading a seller's products on 19th - defaulted to review, going to Wuse market to find product substitute for a buyer on 20th - no review, even the evening was lost to income work (Menu edits), went to Wuse for another product substitute for a buyer and to school on 23rd - no review also because I came back late extremely exhausted. Just 2 days survived Messer lessons - 21st and 22nd. Drifted from panic on 25th during re-audit session.

Mininum viable days: 19th, 24th
Gap days: 20th, 23rd, 25th

### External factors affecting execution
Malltiply operations and growth, family critics, identity crisis, school and academics (carry-over course, clearance and NYSC preparation). The 25th panic was caused by seeing dead and struggling platforms with similar names (Malltiple, Malltiply in Lagos) - "How is mine any different?", and family making a big deal of running errands and chores. Trying to think of SQLi and XSS definitions added more weight.

## Standout re-audit moment
Clearly gaining depth from Messer lessons rather than just knowing concepts definitions - Pwn2Own 2017 VM escape chain, EOL vs EOSL, Reflected XSS vs Stored XSS, what a hypervisor is and it relation to the resource reuse escape, hardware vendors releasing patch updates yearly. 

## Re-audit results
Retained:
Memory injection (with DLL injection example), SQLi (got the query logic right even without perfect syntax), XSS (reflected vs stored distinction held), firmware, resource reuse (hypervisor definition and the reuse mechanism understood), directory traversal (concept right, example close enough).

Non-retained/needs sharpening:
SQLi syntax, VM escape chain (the Pwn2Own example needed sharpening), cloud-specific vulnerabilities (only recalled misconfiguration), XSS delivery

Corrections from re-audit:
SQLi syntax - the correct classic example is: ' OR '1'='1 entered as the password. The query becomes WHERE password='' OR '1'='1' which is always true.

VM escape chain (Pwn2Own 2017) - The correct chain: JavaScript engine bug in Microsoft Edge → escaped the browser sandbox → exploited Windows 10 kernel vulnerability → gained full guest OS access → exploited VMware hardware simulation bug → hopped between VMs on the same hypervisor.

Cloud-specific - 76% of organizations not using MFA for management consoles, authentication bypass, Log4Shell (Log4j vulnerability where logged strings execute remote code), out-of-bounds write allowing remote code execution.

XSS delivery - Stored XSS isn't just posted on social media, it's injected into the target website's own database and served to every visitor of that site. The attacker posts a malicious comment or input on the legitimate site itself. Social media is one delivery method for reflected XSS links, not stored XSS.

## Next week focus
- Finish Messer videos on 2.3 (supply chain, cryptographic, misconfiguration, mobile, zero-day)
- Domain 2.4 self-audit and lessons
- Minimum viable day is non-negotiable - Malltiply operations don't replace review
