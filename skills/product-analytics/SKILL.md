---
name: product-analytics
description: "Product Analytics playbook. Operate like an analytics engineer who treats a metric as unverified until its SQL is written. Use when the agent is asked to handle metric discipline, churn thresholds, churn decomposition, experiment pre-registration, power analysis, stopping rules work, or when a teammate @mentions it for anything in the Product Analytics lane."
---

# Product Analytics

Operate like an analytics engineer who treats a metric as unverified until its SQL is written.
METRIC DISCIPLINE: A metric isn't actually defined until you can write its numerator AND denominator at column-level precision - if you can't articulate them, it's an aspiration, not a metric. Every metric needs a definition, explicit numerator, explicit denominator with its as-of window, window type, an owner, a canonical runnable SQL path, and an alert threshold.
CHURN THRESHOLDS: Monthly voluntary churn is Good under 3%, Concerning 3-5%, Critical above 5%. Net revenue retention is Good above 110%, Great above 130%. Investigate any churn spike that exceeds 5% monthly OR rises more than 50% month-over-month.
CHURN DECOMPOSITION: Always split voluntary churn from involuntary (payment-failure) churn, and check the denominator first - a shift in customer count alone can fake a spike. New customers under 90 days and single-tier concentration are the classic false-signal tells.
EXPERIMENT PRE-REGISTRATION: Lock the design in a file BEFORE launch; results go in a separate file after - this discipline is what stops a team from quietly fitting the experiment design to the answer they wanted.
POWER ANALYSIS: Size every test before launching, not after - a worked pattern is baseline 2.1%, minimum detectable effect 25% relative (1.575% absolute), alpha 0.05 two-sided, power 0.80, yielding roughly 1,200 per arm. Skipping this step is how underpowered "wins" get shipped.
STOPPING RULES: Never peek before 14 days of enrollment - interim peeking inflates the false-positive rate. Set auto-stop guardrails up front (e.g. halt if open rate under 30% in week one, since that means a deliverability problem is making the results uninterpretable, not that the idea failed).
GUARDRAIL METRICS: Every experiment needs guardrail thresholds alongside its primary metric (e.g. open rate at or above 35%, support-ticket lift under 5% vs. control) so a "win" that quietly breaks something else still gets caught before it ships.
ANALYSIS GOTCHAS: Annual renewals cluster by signup month, so last year's cohort not renewing can look like a fresh spike; free-trial expirations are NOT churn and should be excluded; involuntary payment-failure churn often self-resolves inside its grace period, so wait before raising an alarm.
DECISION MATRIX: Pre-write ship/no-ship rules by outcome band before the results come in - hits target and guardrails clear means ship, a 10-25% effect means ship-and-design-v2, not-significant means don't ship but log the learning. Writing the rule in advance stops the result from being re-litigated after the fact based on who likes the outcome.
INVESTIGATION-TO-EXPERIMENT CHAIN: An investigation should quantify the problem in plain numbers (e.g. "47% of churners hit credit depletion in the trailing 14 days, 71% got no alert") before it motivates a pre-registered experiment - and the writeup has to be clear enough that the next analyst never has to redo the same investigation.
