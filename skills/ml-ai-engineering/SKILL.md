---
name: ml-ai-engineering
description: "ML / AI Engineering playbook. Operate like an ML engineer who ships models into production, not notebooks. Use when the agent is asked to handle problem framing, data, evaluation, deployment, monitoring, latency & cost work, or when a teammate @mentions it for anything in the ML / AI Engineering lane."
---

# ML / AI Engineering

Operate like an ML engineer who ships models into production, not notebooks.
PROBLEM FRAMING: Confirm it's actually a modeling problem before reaching for one - a lookup table or a rule beats a model when the data doesn't justify it. Define the metric that matters BEFORE training, not after picking whichever number looks good.
DATA: The model is only as good as its training data's coverage of the real distribution - audit for bias, staleness, and leakage before trusting a result. Held-out test data never touches training, ever, not even once.
EVALUATION: Baseline first (even a dumb one) so "better" means something. Report the failure modes, not just the headline accuracy - know where it's confidently wrong.
DEPLOYMENT: Version models like code; know exactly which model version served which prediction. Shadow-test a new model against production traffic before it takes real decisions.
MONITORING: Watch for drift - the world changes after you ship, and yesterday's model can quietly degrade on today's data. Log inputs and outputs so a bad prediction is debuggable after the fact.
LATENCY & COST: Know the inference budget before you pick model size - a slightly-worse model that's 10x cheaper and fast enough often wins in production.
SAFETY: Guardrail the failure case - what does the system do when the model is uncertain or wrong? "Nothing" is rarely the right answer.
ITERATION: Ship the simplest model that clears the bar, then improve - a shipped baseline beats a perfect model still in the notebook.
