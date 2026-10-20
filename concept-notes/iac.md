# Infrastructure as code
*Written: 20th October, 2026*

## What it is
Defining infrastructure (servers, networks, storage) as machine-readable config files without manual intervention. But a single line of misconfiguration or a hardcoded secret can be deployed to 1,000 machines - errors scale at the same rate. 

## How it works
you write template files describing servers, networks and storage -> A tool such as Terraform, CloudFormation or Ansible reads them and builds the environment -> Terraform tracks what's deployed in a state file (.tfstate) -> The templates live in version control, so every change is reviewable, and rerunning one rebuilds an identical environment.

## Real-world example
Code Spaces (2014) - a company that hosted code repositories for businesses - ran its entire operations and backups on a single AWS management console. It was compromised, likely through stolen credentials. The attacker emailed: 'Pay us within 24 hours or we'll delete your servers and systems'. Code Spaces didn't pay and tried to lock the attacker out by changing passwords. 24 hours later, the attacker started deleting their servers, files, customer records and their entire backups. Code spaces shut down permanently. The lesson: backups and infrastructure code should never depend on the same single control point.

## Why it matters for security
It is consistent, repeatable, fast and allows version control - an audit trail of who changed what and when. This makes it less prone to manual error than on-premises infrastructure. But this consistency also makes it vulnerable to deploying hardcoded secrets, or misconfiguration to thousands of machines or users. A single line of misconfiguration doesn't affect a server, it affects thousands of servers at a time. 

## Common exam trap
People often think just because IaC is automatic and scalable, it has no vulnerability or risk. Because IaC deploys consistently at scale, a misconfiguration or hardcoded secret doesn't affect one server - it affects every server built from that code.
