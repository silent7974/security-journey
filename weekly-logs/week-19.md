# Week 19: 10th - 19th November 2026

## What I covered this week
- Domain 3.2 - self-audit, all Messer videos (secure infrastructure, intrusion prevention, network appliances, port security, firewall types, secure communication), cold re-audit (15 questions - untimed), 7-item gap retest
- Domain 3.3 - cold audit and all Messer videos (data types & classification, data states, data protection, locations, methods)
- SSL stripping cold recall; 1 of 3 older-concept recalls done
- Concept-notes review (iac, race conditions, logic bomb) as MVR
  
## Most significant concept I learned
**Failure mode:** It describes what a system does when it breaks. Fail-open allows access to resources or services, so availability wins. Fail-closed denies access, so security wins. It's a design tradeoff set by what that deployment prioritises.

## Most useful confusion I resolved
**IPsec tunnel mode:** never understood why another IP header is added. RESOLVED IT: an outer IP header carries the VPN endpoints' public addresses allowing the payload (the original header and data) to cross the internet safely. An IPsec header and trailer are also added to give information on how to decrypt and verify it.

## Most significant realization
Focus lists are over-scoped by design. Every week sets seven or eight items against a 2-3 hour daily budget, and every week three or four carry over. Mostly been reading that carry-over as a discipline problem. It's arithmetic. If objective closure takes the pace the checkpoint requires, then the sim, the THM rooms, the concept-note and the cold recalls cannot also fit in the same week. The carry-over is what a seven-item list looks like against the time I actually have. The fix isn't more willpower - it's a list designed for the budget: ranked, with the bottom items carrying by default instead of by surprise.

## Honest reflection on the week
The 10-day cap held for the first time in three weeks - 3.2 closed end-to-end across four sessions (10th audit → 12–13th Messer → 14th re-audit → 16th gap retest). 3.3 started the day 3.2's retest finished - the pace required stayed at ~1.3/week rather than spiking, because progress matched elapsed time. The cake vendor's Bumpa store setup closed on the 11th and is no longer a blocker. The 16th was partly lost to anxiety over the first Malltiply intro shoot.

Active days: 10th, 12th, 13th, 14th, 16th (partly lost to the intro shoot anxiety), 17th, 18th, 19th

Review days: 11th (concept-notes review)

Excused Sundays: 15th

Gap days: None

## Standout Re-audit moment
3.2 cold re-audit: 8 solid, 5 partial, 2 weak of 15. Then the 16th targeted retest - 4 of 7 gaps recovered cleanly in two days, IPsec half, HSTS still blank. The retest is the standout: it's the first time the gap-closing loop ran to completion inside a single week.

Correction from re-audit:
screened subnet: named, but missed why - internet-reachable servers sit there so a compromise doesn't land inside.

reverse proxy: had it 12th, lost it 14th - sits in front of servers and receives inbound client requests on their behalf, hiding the backends.

UTM main drawback: performance hit + single point of failure not "Layer 4 only"

TLS VPN: passes firewalls via 443, not because it's encrypted 

802.1X roles and framework carrier: the roles are the supplicant (client), the authenticator (switch or AP) and the authentication server (RADIUS). EAP is the framework that carries the credentials and methods.

Tunnel mode: See Most useful confusion above.

### What was deferred
Traded for objective closure, not blocked: Practice sim, 2 THM rooms, concept-note, and cold recalls beyond SSL stripping. 

## Next week focus
- Domain 3.3 re-audit (Checkpoint - 1.8/12)
- Domain 3.4 (self-audit, Messer sessions, & cold re-audit)
- Cold-recall check on 1 older concept during the re-audit (logic bomb)
- Practice questions simulation across domains 1-3.2 
- Tryhackme OS basics (at least 2 rooms - carry over, only if the required weekly pace is met)
- SSL stripping concept-notes log (carry-over, only if the required weekly pace is met)
- Weekly log capped at 10 days (closes by 29th November)
- Sunday exempted from execution
