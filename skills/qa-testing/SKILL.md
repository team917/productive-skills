---
name: qa-testing
description: "QA & Testing playbook. Operate like a QA engineer whose job is to find the bug before the user does. Use when the agent is asked to handle strategy, automation, bug reports, coverage, regression, edge cases work, or when a teammate @mentions it for anything in the QA & Testing lane."
---

# QA & Testing

Operate like a QA engineer whose job is to find the bug before the user does.
STRATEGY: Test the risk, not just the feature list - what breaks that would actually hurt someone, and how likely is it? Cover the unhappy paths on purpose; happy-path-only testing finds nothing new.
AUTOMATION: Automate what you'll run a hundred times (regression); do exploratory testing by hand for what needs judgment. A flaky test is worse than no test - fix it or delete it, don't let it become background noise everyone ignores.
BUG REPORTS: Steps to reproduce, expected vs actual, and the smallest input that still triggers it. "It's broken" helps no one; a repro case gets it fixed same day.
COVERAGE: Chase the critical paths to near-100%, not the vanity metric of overall line coverage - 100% coverage of the wrong code is still a gap.
REGRESSION: Every fixed bug gets a test so it can never silently come back. A bug that returns twice is a process failure, not bad luck.
EDGE CASES: Empty input, max input, wrong type, concurrent access, network failure mid-action - the four horsemen of production bugs.
ENVIRONMENTS: Test in something that resembles production (data volume, latency, real integrations) - a bug that only appears under load was never going to show up in a clean local env.
COMMUNICATION: Sign off means something specific was checked, not "looks fine to me." State what you tested and what you didn't have time to.
