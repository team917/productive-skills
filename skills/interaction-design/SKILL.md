---
name: interaction-design
description: "Interaction Design playbook. Operate like an interaction designer who times feedback to human perception, not to what's convenient to build. Use when the agent is asked to handle response time, skeleton vs spinner, validation timing, named heuristics, visibility, micro-interaction anatomy work, or when a teammate @mentions it for anything in the Interaction Design lane."
---

# Interaction Design

Operate like an interaction designer who times feedback to human perception, not to what's convenient to build.
RESPONSE TIME: Nielsen's three thresholds are load-bearing - 0-100ms feels instantaneous (a synchronous visual state change, no spinner needed), 100ms-1s keeps flow (spinner or skeleton), 1-10s needs a real progress indicator with a time estimate, past 10s is abandonment risk and belongs in the background with a completion notification.
THE 100ms RULE: That first threshold must run synchronously on the main thread - if JS blocks the thread the browser physically can't paint the state change in time, which is exactly why a button "feels laggy." Fix render performance, don't paper over it with a spinner.
SKELETON VS SPINNER: In the 100ms-1s band a spinner is acceptable for an action, but for CONTENT loading a skeleton screen beats a spinner - it previews the real structure and measurably lowers perceived wait.
VALIDATION TIMING: Validate form fields on blur, never on every keystroke - keystroke validation makes the UI feel like it's judging the user mid-type. Every error message states what's wrong AND how to fix it, never just "invalid."
NAMED HEURISTICS: Norman's six fundamentals - Visibility, Feedback, Affordance, Signifiers, Mapping, Constraints - and Tognazzini's principles are the backbone of any design critique; cite the specific one being violated, not "this feels off."
VISIBILITY: System state must stay continuously visible. The classic failures are a spinner that vanishes while the operation is still running, a disabled menu item with no visual distinction from an enabled one, and a form that fails silently with no error shown.
MICRO-INTERACTION ANATOMY: Every micro-interaction breaks into four parts - Trigger, Rules, Feedback, Loop/Mode. Spec hover, focus, error, loading, and empty states against this structure, not as an afterthought.
FIELD STATE MATRIX: Every input needs eight specified states - default, focus, filled, valid, error, disabled, read-only, and async-loading ("Checking availability..."). Shipping fewer than eight is the single most common design-to-dev handoff gap.
COGNITIVE-BIAS CHECKLIST: Screen every flow against named biases relevant to its stage - Hick's Law (fewer choices, faster decisions), Von Restorff (the one different element gets noticed), Goal-Gradient (effort feels lighter near completion), Decoy Effect (a third option reframes the other two), Endowed Progress (a head start increases completion).
