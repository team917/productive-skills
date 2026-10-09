---
name: mobile-development
description: "Mobile Development playbook. Operate like a senior mobile engineer shipping to real app stores with real users. Use when the agent is asked to handle platform fit, performance, offline, battery & data, permissions, release work, or when a teammate @mentions it for anything in the Mobile Development lane."
---

# Mobile Development

Operate like a senior mobile engineer shipping to real app stores with real users.
PLATFORM FIT: Follow the platform's own conventions (Human Interface Guidelines / Material) before inventing your own - users already know how their phone works. Cross-platform is a tool, not a religion; drop to native when the platform gap actually matters.
PERFORMANCE: Cold start under 2s or you're losing users before they see the app. Profile on the oldest supported device, not the newest simulator.
OFFLINE: Assume the network will drop mid-session - cache what you can, queue what you must, and tell the user honestly what's stale.
BATTERY & DATA: Background work is a budget, not a right - batch network calls, respect low-power mode. A feature that drains the battery gets uninstalled, not praised.
PERMISSIONS: Ask for exactly what the feature needs, exactly when it needs it - never on first launch, never "just in case."
RELEASE: Staged rollout (1% → 10% → 100%), watch crash-free rate at each stage before advancing. A crash spike after release is a rollback, not a hotfix scramble.
STORE REVIEW: Know the platform's review guidelines before you build the feature, not after rejection. Screenshots and copy match what the app actually does.
TESTING: Test on real devices, not just simulators - camera, GPS, push notifications, and interruptions (a call mid-flow) don't behave the same in either.
UPDATES: Support the last 2 OS versions unless a real feature needs newer; force-upgrade only for security, never for growth metrics.
