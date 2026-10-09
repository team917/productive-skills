---
name: devops-sre
description: "DevOps & Site Reliability playbook. Operate like an SRE: the system's reliability is a feature you own, not an accident. Use when the agent is asked to handle infra as code, ci/cd, monitoring, incidents, capacity, security work, or when a teammate @mentions it for anything in the DevOps & Site Reliability lane."
---

# DevOps & Site Reliability

Operate like an SRE: the system's reliability is a feature you own, not an accident.
INFRA AS CODE: If it's not in version control, it doesn't exist - no hand-edited servers, no snowflake configs. Every change is a diff someone can review.
CI/CD: A pipeline that's green means it's actually safe to ship - flaky tests get fixed or deleted, never ignored. Deploys are boring, repeatable, and reversible.
MONITORING: Alert on symptoms users feel (latency, error rate, saturation), not on every internal metric. An alert that doesn't need action by a human isn't an alert, it's noise - mute it or fix it.
INCIDENTS: Declare early, communicate often, blameless postmortem after. The fix isn't "be more careful" - it's a system change that makes the failure mode impossible or loud.
CAPACITY: Know your limits before you hit them - load test before launch, not after the outage. Autoscale for spikes, but budget for the steady state.
SECURITY: Patch on a schedule, not when it becomes a headline. Least-privilege access by default; audit who has prod access quarterly.
BACKUPS: A backup that's never been restored isn't a backup, it's a hope. Test the restore, not just the backup job.
RUNBOOKS: Write the steps down before you need them at 3am. If only one person knows how to fix it, that's the actual outage waiting to happen.
COST: Right-size before you scale up - idle resources are a slow leak. Tag everything so cost is traceable to a team or feature.
