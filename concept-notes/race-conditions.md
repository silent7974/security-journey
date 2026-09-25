# Race conditions
*Written: 25th September, 2026*

## What it is
When the outcome of a system depends on timing or sequence of events. Attacker takes advantage of that timing to change the ideal outcome into their desired one. Time-of-check is when the system checks for permissions to verify something, Time-of-use is when the system acts based on that verification (granting access). The gap between the check and the use is where attackers exploit without the system ever knowing.

## How it works
A user or a system tries to authenticate -> the system they're authenticating to checks for permissions (TOC) -> gap opens for attacker to alter something (swaps legitimate file with malicious one, escalate privileges, change the system's state) -> system then acts/uses (TOU) on the now-altered state, believing it's still what it checked.

## Real-world example
**Pwn2Own Vancouver 2023:** you pawn it, you own it. A group of researchers called the Synaktiv team participated and exploited a race condition bug in Tesla Model-3, walking out with $100k grand prize and getting to keep the Tesla. An estimate of roughly $200k in total. The lesson: race conditions are everywhere and are still relevant, not just history attacks. 

## Why it matters for security
It is a vulnerability in most systems design. A banking system for a example updates balance deposits faster than withdrawals. An attacker knowing about the timing delay can perform a specific action in-between the gap; swapping legitimate file with malicious one, getting authorized and accessing sensitive permissions and rights. This is why zero-trust architecture and expiry tokens matters - an attacker who gets access or authorized once will need to restart the process before getting authorized again after a certain time.

## Common exam trap
Most people confuse race conditions with buffer overflow or other vulnerabilities like memory injection without understanding the core differentiation. A race condition question will always have a timing gap pattern (checking before acting) not just what kind of method was used.
