# Week 13: 2nd - 10th September 2026

## What I covered this week
- Messer videos - Cryptographic attacks, Password attacks, Indicators of compromise
- Tryhackme Computer fundamentals - Computer types
- Reviews on hard days (2.1, 2.2 & 2.4)
- Overall 2.4 re-audit
  
## Most significant concept I learned
SSL stripping: downgrade attack coupled with on-path attack. Attacker uses a proxy to sit between a browser and a server during communication initiation, the browser first sends a message to the server using http, the server respond asking to switch to https before continuing, the attacker refuse to send that response to the browser and the browser keeps sending the attacker plaintext HTTP, while the attacker separately maintains a genuine HTTPS session with the server - appearing as the real client to the server, and as the server to the browser.

## Most useful confusion I resolved
Thought birthday attack is when an attacker is given a specific hash to find it's corresponding input. Resolved: that is called a preimage attack. A birthday attack is much easier - computing hashes with multiple inputs (messages, files, videos) to discover at least 2 with the same hashes, backed by the birthday paradox - in a room of 23 people there's a 50% chance 2 share the same birthday. An attacker that discovers 2 inputs with the same hashes can substitute one for the other, failing integrity verification entirely.

## Honest reflection on the week
External factors repeatedly affecting the minimum viable rule (20-mins review); on the 4th I had water unexpectedly leaking from my room's ceiling and had to fix it, water scarcity, no electricity, stomach constipation, cringe feeling continuously because Malltiply went live on public channels (beyond warm network), and physically exhausted after coming back from Friday worship (Jummu'ah) all on the same day making review even harder. But the rule still held across 3 days, Messer lessons on the 5th (closing 2.4), and tryhackme on 6th. 

Review days: 3rd, 8th & 9th 

Gap days: 2nd & 4th 

School: 7th

## Standout re-audit moment
Overall 2.4 re-audit from Malware to indicators. 11 questions and got 6 without corrections. Gaps are mostly precision/mechanism-level, not conceptual misunderstanding.

### External factors affecting execution
Unexpected water leak from room's ceiling, water scarcity, electricity insufficiency, health issues (stomach constipation), family interactions (errands and gist), Malltiply's related mixed feelings (cringe feeling), and the recurring extended morning disruption.

## Re-audit results
Retained: Rootkit, fileless malware mechanism, offline cracking bypassing lockout, spraying vs brute force, lockout as pretext, indicator for spraying vs indicator for brute force 

Needs sharpening/non-retained: Amplified DDoS core mechanism, directory traversal root-cause, collision consequence, preimage attack, SSL stripping 

Corrections from re-audit:
Correctly named spoofing for reflected but dropped it for amplified. Amplification also relies on spoofing the victim's IP - that's why the large response goes to the victim instead of back to the attacker. "Multiple devices sending small requests" describes distribution, not amplification. The defining trait is: spoof victim's address → send small request to a third party → third party sends a disproportionately large response to the spoofed (victim) address. Size multiplication + spoofing, not device count.

"Freedom to navigate files with minimal inputs" isn't a technical cause, it's a restatement of the symptom. The real cause: missing input validation/sanitization on file path parameters - the application fails to strip or reject sequences like ../ before using user input to build a file path, so the attacker's input is trusted and executed literally.

A collision isn't about "accessing permissions" - it's about breaking integrity/signature verification. If a malicious file hashes identically to a legitimate one, any system that checks integrity by comparing hashes gets fooled into treating the malicious file as verified/trusted. No permissions are being accessed via the hash itself; the danger is trust, not access.

Described preimage as "brute force with a list of hashes until granted access" - that's closer to generic password/credential cracking. Actual preimage attack: attacker is given one specific target hash and must find any input that produces that exact hash - no list, no "until access granted," just one fixed target. The real reason birthday is cheaper isn't "higher chance of success" (vague) - it's mathematical: preimage needs ~2^n attempts to hit one specific target, birthday only needs ~2^(n/2) because it's checking all pairs against each other, not against one fixed value.

"Attacker tells the server the browser is now using https" is inaccurate - the attacker isn't telling the server anything, it's actually running a real HTTPS session with the server itself, while simultaneously feeding the victim's browser plain HTTP. The attacker is the genuine TLS endpoint from the server's perspective and a fake plaintext server from the browser's perspective - sitting as the man-in-the-middle on both connections at once, not lying to one side.

## Next week focus
- Domain 2.5 self-audit
- Tryhackme - Computer fundamentals continuation
- One concept-notes log
