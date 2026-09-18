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
Fastest domain to complete (2.5) since domain 2.1 in **week-04.md**, everything covered in the same week unlike 2.2-2.4 that took multiple weeks. External factors affecting real sessions + minimum viable reviews. On the 16th, did a research and provided insights/suggestions for a new venture (Aman - a deferred payments agreement management startup for my elder brother, might be some funding, and opportunity to operate under CBN sandbox), potential UI/UX role, disrupted Messer session and if not careful might slow this path further. Then income work (Menu editing for a catering service business) throughout the entire evening blocking gap for a review. 

Review days: 14th & 15th

Gap days: 11th (social media scrolling drift), 12th (cousins visiting), & 16th

## Standout re-audit moment
Overall 2.5 re-audit (same scenario-style) - 12 questions. Got 6 precise, 4 needed corrections and 2 blanks. Scope and precision of definition named as the root skill gap. 

### External factors affecting execution
Aman's activity (new venture), income work, cousins unexpected visit, social media drift, the recurring extended morning disruption

## Re-audit results
Retained: Segmentation/PCI DSS, ACL, self-lockout, emergency out-of-band, EDR vs traditional antivirus, heuristic analysis tradeoff

Needs sharpening: SIEM's term ("correlation" not "cross-interaction logs"), enforcement methods for application allow list (certificate answer is narrow), decommissioning methods included, ACL category, EDR category reasoning

Non-retained: NAC & NGFW

Corrections from re-audit:
SIEM's term ("correlation" not "cross-interaction logs"): a SIEM can connect events across sources that look harmless individually but form an attack pattern together (a failed login on one system + a firewall alert + a file access on another, tied together by timestamp/user). That correlation capability, not just storage in one place, is the actual value proposition.

Certificate enforcement: Tied it specifically to "Microsoft, Google" as named companies — the actual concept is trusting any publisher whose certificate the organization has chosen to trust, not those two specifically. A company could trust its own internal code-signing certificate, or a smaller vendor's. The mechanism is "signed by a trusted publisher," not "signed by a big-name company."

decommissioning methods included: correctly named decommissioning as the failed process, but the answer shouldn't stop at the label — what specifically should decommissioning have included here? Removing the device from the network, revoking its access/credentials, and wiping or destroying its data.

ACL category: ACL doesn't belong in hardening list. Segmentation and Access control (which includes ACLs) are listed as their own top-level items alongside patching/encryption/monitoring — separate from the "Hardening techniques" sub-bucket, which is specifically the single-device list (endpoint protection, host-based firewall, HIPS, port/protocol disabling, password changes, unnecessary software removal). ACL operates at the network/policy level, which makes it mitigation, not hardening.

NAC (Network Access Control): the scenario - posture check at login, quarantine to a restricted VLAN for non-compliant devices — is the textbook definition.

NGFW: adds application-layer awareness - it can identify and control traffic by application, not just port/protocol, and typically bundles in IPS and threat-intelligence feeds. A traditional stateful firewall only inspects up through the transport layer; NGFW inspects what's actually running inside the traffic.

EDR category reasoning: Self-correction on segmentation was right; the reasoning on EDR was off. Segmentation and access control are correctly mitigation, not hardening (network/policy scope). But EDR hardening reasoning — "because you're manually configuring it" — isn't the actual distinguishing logic. It's hardening because it protects one endpoint's attack surface, regardless of whether its response is manual or automated. 

## Next week focus
- First-time practice exams from Domain 1-2 overall
- Tryhackme - Computer fundamentals continuation (at least 2 rooms)
- One concept-notes log (non-negotiable)
