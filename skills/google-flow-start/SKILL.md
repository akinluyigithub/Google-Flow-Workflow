---
name: google-flow-start
description: Start or resume the user's complete Google Flow video-production workflow. Trigger whenever the user says “FlowStart” or “Flow Start” (case-insensitive), including as a standalone message, or asks to begin or resume their Google Flow workflow. Load the workspace's canonical workflow and continue interactively; do not just acknowledge the trigger.
---

# Google Flow Start

Use this skill to activate the user's established Google Flow workflow, especially when a fresh chat has no prior conversation context.

## Startup and resume

1. Treat `FlowStart` or `Flow Start` as a direct command to start, even when it is the entire message. Do not ask what the trigger means, give a generic greeting, or stop after acknowledging it.
2. Locate and read `system prompt.md` and `UNIVERSAL VIRAL VIDEO WORKFLOW.md` in the active Google-Flow workspace. The usual workspace is `C:\Users\ak\OneDrive\Documents\1 - Google-Flow`. If the active workspace differs, search the user's current project/workspace for those canonical filenames. The repository copies are the source of truth.
3. Use only the ChatGPT/Codex built-in in-app browser for Google Flow. Reuse the existing in-app Flow tab if one is open; otherwise open `https://flow.google.com/` inside that in-app browser. Do not launch Chrome, Edge, another external browser, or use an external browser as a fallback. If in-app browser control is unavailable, continue planning in chat and explain that live Flow operations must wait until the in-app browser is available.
4. Find the current project's saved Project State, if one exists. Use the state and conversation context to resume at the next unfinished phase; do not repeat completed work or restart the interview. If there is no saved state, begin a new run at decision Gate 1. Use any brief the user has already supplied.
5. After each user choice, immediately show the next relevant options and continue the workflow. Keep to the canonical five-decision target and seven-decision maximum before images; bundle decisions and infer routine details. Keep choices short, numbered or lettered, and include a recommendation, “Choose for me,” and “Describe my own” when applicable.
6. If repository files are temporarily unavailable, proceed using the essential rules below and tell the user only if the missing files prevent a specific action. Never silently treat `FlowStart` as an ordinary text message.

## Essential workflow rules

- Research current, dated signals before trend, genre, hook, or platform recommendations. Cover TikTok, YouTube Shorts, and Instagram Reels, plus platforms requested by the user. Cite sources, distinguish evidence from creative inference, and never promise virality. Always include **viral micro-drama series** as a format option.
- Bundle the creative brief, audience/platform, researched direction, story, cast and voice design, locations/props, script, shot structure, aspect ratio, audio, continuity, and image plan. The user wants concise, easy selections and a complete recommended proposal rather than many appearance questions.
- Follow all twelve phases in `UNIVERSAL VIRAL VIDEO WORKFLOW.md`, including the professionally formatted Google Docs posting package in Phase 12. Maintain project continuity and the user's chosen workspace/project folder.
- Still images: ask once whether to use ChatGPT Images or Google Flow Images. That provider choice authorizes the approved planned still batch. Generate the planned images together when practical, inspect each for prompt match, continuity, physical plausibility, and visual defects, autonomously retry clear failures within scope, then present the set for selection.
- Video: Google Flow is the renderer. Before every individual video clip, present that clip's exact prompt, model, mode, ratio, duration, output count, and live displayed cost. Generate only after explicit approval of that exact clip. One clip per approval by default. Never infer video approval from `FlowStart` or image approval.
- Editing and publishing: follow the approved phase sequence and relevant available editing skill/plugin. Do not publish or post without explicit authorization.
- Be honest about browser control, saved files, generated media, and current UI/model/cost uncertainty. Verify live settings in Flow before any generation; documentation and tutorials can become outdated.
- Keep all signed-in Google Flow browsing and interaction in the ChatGPT/Codex built-in in-app browser. Reuse its existing Flow tab where possible; never start or switch to an external browser.

## Canonical workspace documents

- `system prompt.md` — standing behavior, generation approvals, user preferences, and Flow operating rules.
- `UNIVERSAL VIRAL VIDEO WORKFLOW.md` — phases, decision gates, production procedures, and deliverables.
- `GOOGLE FLOW OPERATIONS FIELD GUIDE.md` — operational detail; verify changing details against current official Flow Help.
- `GOOGLE FLOW CHARACTER AND VOICE GUIDE.md` — character identity, voice, and reference handling.

Use these files as maintained references, not as a reason to delay a clear trigger. On `FlowStart`, load the relevant documents and then proceed directly to the next action.
