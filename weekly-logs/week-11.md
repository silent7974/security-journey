# Week 11: 13th - 22nd August 2026

## What I covered this week
- Messer videos - Spyware, Bloatware & other Malwares(keyloggers, logic bomb, and rootkit), Physical, DoS, DNS, Wireless, On-path, Replay, Malicious code, and Application attacks
- Concept-notes directory initiated 
- 2.4 review repeatedly on hard days
- Re-audit with scenarios
  
## Most significant concept I learned
**Logic bomb:** A malware that sits dormant until a specific condition is met, then executes. A disgruntled employee might plant a logic bomb to delete the entire database record when their name gets deleted, meaning they got fired. A time-based logic bomb executes during a specific time or event. **South Korea March 19, 2013** is the real-world example: A trojan was attached to email sent to banks and broadcasting companies. If that trojan is run, it affects every system vulnerable to it - including the bank's ATMs. On March 20th (the next day) exactly at 2pm, everything in storage on the affected systems was deleted including the master boot record. The systems were then rebooted, but the Operating system has just been deleted. Showing "Boot device not found. Please install an Operating System on disk."

## Most useful confusion I resolved
Thought trojan is a malware that actively hides itself, making it difficult for security tools to detect. While I understand that is exactly what rootkit does (actively hiding itself deep in OS), mistook trojan with having the same trait. Resolved: while they're trojans that evade security tools, a trojan is mostly known for packaging itself as a legitimate tool or software tricking users to install it.

## Honest reflection on the week
Initiated the concept-notes directory - concepts retained enough to teach (logic-bomb.md logged). Review held most days, and a gap day due to a carry-over exam study. 3 days survived Messer lessons. No tryhackme activities and still have couple of Messer sessions to close the domain. 

Review days: 15th, 17th, 18th, 21st August.

Gap days: 19th August.

School: 20th August.

## Standout re-audit moment
The 2.4 re-audit were Messer reinforced from the weekly lessons and were mostly scenario questions rather than concepts definitions. 8 questions and got 6 right with honest self-rating. 

### External factors affecting execution
Extended morning disruption on 15th, exam study on 19th (one-off - final exam for the degree).

## Re-audit results
Retained: Worm vs virus, tailgating, amplified DDoS vs reflected DDoS, directory traversal, pass-the-hash, on-path vs replay

Needs sharpening: rootkit vs trojan differentiation, directory traversal command, pass-the-hash (other means aside on-path)

Corrections from re-audit:
The tell in the scenario is "hidden CPU usage that evades standard process listings" - that's rootkit territory: it operates at a level (often kernel-mode) below or alongside the OS's own visibility tools, which is exactly why Task Manager can't see it. A trojan's defining trait is different: it's malware disguised as legitimate, wanted software to get you to install it voluntarily - the deception is in the delivery, not in hiding itself post-infection afterward (though some trojans do also hide).

"runs with a 'dir' command" doesn't belong here - dir is a Windows shell command for listing folder contents; it has nothing to do with how ../ path traversal works in a URL parameter.

On-path is one way to grab the hash, but not the definition - malware, memory-scraping tools (like Mimikatz), or a compromised server can capture it too. The core of pass-the-hash isn't how you got the hash, it's that you authenticate using the raw hash directly, without ever cracking it back into plaintext.

## Next week focus
- Messer on 2.4 - Cryptgraphic & password attacks, Indicators of compromise
- Tryhackme - Computer fundamentals (critical)
