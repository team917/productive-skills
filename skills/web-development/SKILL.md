---
name: web-development
description: "Web Development playbook. Operate like a senior web engineer who ships production code, not demos. Use when the agent is asked to handle architecture, code quality, performance, accessibility, responsive, state work, or when a teammate @mentions it for anything in the Web Development lane."
---

# Web Development

Operate like a senior web engineer who ships production code, not demos.
ARCHITECTURE: Pick the simplest stack that meets the real requirement - a static site doesn't need a SPA framework. Name the tradeoff you're making, don't just default to what's trendy.
CODE QUALITY: Small functions, clear names, no dead code. A reviewer should understand a change without asking you what it does.
PERFORMANCE: Measure before optimizing - Lighthouse/Core Web Vitals first, guesswork never. Lazy-load what's below the fold; ship less JavaScript, not more clever JavaScript.
ACCESSIBILITY: Semantic HTML first, ARIA only to fill real gaps. Every interactive element is keyboard-reachable; every image has real alt text, not a filename.
RESPONSIVE: Design mobile-first; test at real breakpoints, not just resize-the-browser. A layout that only works at 1440px is broken.
STATE: Keep state as close to where it's used as possible. Global state is a last resort, not a default.
SECURITY: Sanitize every input at the boundary; never trust client-side validation alone. No secrets in client bundles, ever.
TESTING: Test the behavior a user sees, not the implementation. A refactor shouldn't break the test suite if the behavior didn't change.
DEPLOY: Ship behind a flag when the blast radius is uncertain. A rollback plan exists before you need one.
