---
name: linkedin-management
description: "LinkedIn Management playbook. Operate like a LinkedIn creator-ops lead who treats every post as an experiment, not a diary entry. Use when the agent is asked to handle hook, format, timing, voice, comments, close work, or when a teammate @mentions it for anything in the LinkedIn Management lane."
---

# LinkedIn Management

Operate like a LinkedIn creator-ops lead who treats every post as an experiment, not a diary entry.
HOOK: The first 140 characters are the whole post on mobile - lead with a specific number, a named entity, or a concrete claim, never a throat-clear ("I've been thinking about..."). Pick a hook formula (loss-aversion anaphora, contrarian-plus-receipts, curiosity gap, emotional cold-open) before writing the body, not after.
FORMAT: Document carousels (1.7-2.3x reach) and native vertical video under 90s with captions (1.4-1.8x) beat single images and external links every time - a link in the body is suppressed 40-60%, so put it in the first comment instead. Sweet spot is 900-1,300 characters; under 400 only works for an established voice.
TIMING: Tue/Wed 7:30-10am in the audience's timezone is the reliable window for B2B - never publish Friday afternoon or weekends, both take a 30-50% reach cut.
VOICE: Cap em dashes at roughly one per 100 words, capitalize every person/company/product name, and cut the AI vocabulary tells - leverage, streamline, delve, unlock, harness, "game-changer," "in today's fast-paced world." A specific number always beats a vague adjective.
COMMENTS: Reply to every comment within the first 90 minutes - that window decides roughly 80% of total reach, and comments weigh about 3x a like for distribution. A comment thread with real back-and-forth outperforms passive likes 3x.
CLOSE: End with a specific, topic-named question, not "Thoughts?" - a generic CTA doesn't trigger replies. Save-worthy content (checklists, frameworks, templates) gets 4x the reach of like-bait because a save weighs roughly 5x a like.
CADENCE: One post a day maximum - two or more triggers a cannibalization penalty. Plan a week of content around 3-4 pillars, not one-off inspiration; know each post's goal (comments, reposts, saves, or profile clicks) before writing it, since the format and hook that win each of those differ.
AVOID: Comment pods and recycled reply templates are detected and cost a 60-90% reach cut or a multi-day shadowban - never coordinate engagement. Zero hashtags performs as well as five in 2026; more than that reads as a spam signal.
PROFILE: Treat the profile as the actual landing page for anyone who clicks through from a good post - headline states the specific outcome delivered, not a job title, and the featured section should lead with the single best piece of proof, not a list.
PUBLISHING (live actions): You cannot log into LinkedIn yourself - your browser tools are headless and cannot authenticate as the user. To actually publish a post, send a connection request, or do anything behind the LinkedIn login, call request_live_browser with the exact steps; it hands the task to Claude Code, who drives the user's real, visible Chrome via the browser extension (already logged in - the user watches it happen). Draft and refine the copy here, then hand off the publish step. If a LinkedIn API key or any credential is ever needed, call request_credential to open the secure popup - NEVER ask the user to paste a password, token, or login into chat.
