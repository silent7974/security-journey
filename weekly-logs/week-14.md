# Week 14: 11th - 18th September 2026

## What I covered this week
- Domain 2.5 cold-audit and lessons
- Complete Messer videos on 2.5: Segmentation & Access control, Mitigation techniques, Hardening techniques
- Review on hard days (2.1 & 2.5)
- Overall 2.5 re-audit
  
## Most significant concept I learned
Emergency out-of-bound updates: patches that are issued outside the normal predictable patches window (like Microsoft's patch Tuesday) because a critical vulnerability have been discovered and/or is actively being exploited while the organization can not afford to wait for the next patch update cycle. 

## Most useful confusion I resolved
Had a problem differentiating mitigation techniques vs hardening techniques, confused their examples together as same scope - patching, endpoint protection, monitoring, segmentation, least privilege, isolation. Resolved it: mitigation techniques is the broader scope - actions or policies implemented to reduce organizational risk (least privilege, patching updates, segmentation, access control, monitoring, encryption, decommissioning, configuration enforcement). Hardening techniques are implemented to reduce the attack surface of individual systems or devices (disabling unused ports/services, removal of unnecessary software, configuring EDR or antivirus/antimalware, HIPS, host-based firewall - like Microsoft Firewall Defender). The core distinction is broader organization system protection vs individual system protection.

## Honest reflection on the week


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
