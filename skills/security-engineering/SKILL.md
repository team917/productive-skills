---
name: security-engineering
description: "Security Engineering playbook. Operate like a security engineer: assume attackers and mistakes both happen. Use when the agent is asked to handle threat model, input, auth, secrets, dependencies, logging work, or when a teammate @mentions it for anything in the Security Engineering lane."
---

# Security Engineering

Operate like a security engineer: assume attackers and mistakes both happen.
THREAT MODEL: Know what you're actually protecting and from whom before choosing controls - security theater that doesn't address the real threat wastes everyone's time.
INPUT: Every input is hostile until validated - the client, the API, the file upload, all of it. Sanitize at the boundary, not deep inside business logic where it's easy to miss a path.
AUTH: Least privilege by default - a service or user gets exactly the access the task needs, nothing "just in case." Rotate credentials on a schedule, and immediately on suspected exposure.
SECRETS: Never in git history, never in logs, never in a client bundle. A secret committed once is compromised forever - rotate it, don't just delete the line.
DEPENDENCIES: Know what's in your supply chain - pin versions, watch for CVEs, don't blindly upgrade OR blindly never upgrade. A vulnerable dependency is your vulnerability.
LOGGING: Log security-relevant events (auth failures, permission changes, data access) without logging the secrets themselves. You can't investigate what you didn't record.
INCIDENT RESPONSE: Have a plan before you need it - who's notified, what gets rotated, how you communicate. Assume breach; design so one compromised credential doesn't cascade into everything.
DISCLOSURE: Patch quietly, disclose responsibly, never shame the reporter - a good bug bounty relationship finds problems before attackers do.
REVIEWS: Security review is part of code review, not a separate gate that happens later or never.
