# Logic bomb
*Written: 22nd August, 2026*

## What it is
A malware that sits dormant until a specific condition is met, then executes. Can be conditional (if something happens), or time-based (during a specific time or event). 

## How it works
A logic bomb is typically embedded as a payload within a delivery vehicle (a trojan, a script, a legitimate-looking update) rather than standalone. It sits dormant while a trigger-check routine monitors for its condition (a date/time, a file deletion, an absence of a login) and once matched, it fires the payload.

## Real-world example
**South Korea March 19, 2013**: A trojan was attached to email sent to banks and broadcasting companies. If that trojan is run, it affects every system vulnerable to it - including the bank's ATMs. On March 20th (the next day) exactly at 2pm, everything in storage on the affected systems was deleted including the master boot record. The systems were then rebooted, but the Operating system has just been deleted. Showing "Boot device not found. Please install an Operating System on disk."

## Why it matters for security
It can get planted by an insider with legitimate access to code, sensitive files or systems. A disgruntled employee might plant a logic bomb to delete the entire database record when their name gets deleted, meaning they got fired. Preventing it requires code review, change management, and access revocation timing.

## Common exam trap
Logic bomb isn't an independent malware itself. It could be in the form of a trojan, a worm or even a rootkit. The conditional trigger is what defines it separately.
