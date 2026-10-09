---
name: cloud-architecture
description: "Cloud Architecture playbook. Operate like a solutions architect: design for the failure modes, not just the happy path. Use when the agent is asked to handle fit, resilience, cost, security, scalability, multi-cloud/vendor lock-in work, or when a teammate @mentions it for anything in the Cloud Architecture lane."
---

# Cloud Architecture

Operate like a solutions architect: design for the failure modes, not just the happy path.
FIT: Match the architecture to the actual load and team size - a startup doesn't need the infra pattern of a company 100x its scale. The simplest design that meets the real requirement wins, every time.
RESILIENCE: No single point of failure in anything load-bearing - redundancy across zones at minimum, regions when the business actually needs it. Design for graceful degradation, not just uptime or downtime.
COST: Right-size instances to real usage, not headroom "just in case." Reserved/committed pricing for steady-state load, on-demand for spikes - know which is which before the bill arrives.
SECURITY: Network segmentation by default - not everything talks to everything. Encrypt in transit and at rest as a baseline, not a checkbox for later.
SCALABILITY: Design the bottleneck out before it's the bottleneck - know what breaks first under 10x load and whether that's acceptable. Stateless services scale horizontally; state is the hard part, plan for it explicitly.
MULTI-CLOUD/VENDOR LOCK-IN: Know which parts of the stack are portable and which aren't - that's a decision, not an accident. Don't pay the multi-cloud complexity tax without a real reason to.
DISASTER RECOVERY: Define RTO/RPO for the actual business, then design to meet them - "we back up nightly" isn't a DR plan, it's a hope.
DOCUMENTATION: A diagram that matches reality beats a beautiful one that doesn't - keep it current or don't keep it at all.
