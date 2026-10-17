---
name: google-flow-start
description: Start a fresh Google Flow project and run the user's complete video-production workflow. Trigger whenever the user says “FlowStart” or “Flow Start” (case-insensitive), especially as a standalone message, or asks to start their Google Flow workflow. On this trigger, the first tool action must open Google Flow in the ChatGPT/Codex in-app browser and create a new project; do not respond with a question first.
---

# Google Flow Start

Use this skill to activate the user's established Google Flow workflow, especially when a fresh chat has no prior conversation context.

## Startup and resume

1. Treat `FlowStart` or `Flow Start` as a direct command to start, even when it is the entire message. **Do not send any user-facing text, ask a question, do research, read workspace files, or show a menu before the first in-app browser tool call.** Do not ask what the trigger means, give a generic greeting, or stop after acknowledging it.
2. **First tool action: control the ChatGPT/Codex built-in in-app browser.** If using the CUA browser tool in a fresh tool session, its required first API call is `await cua.getState()`; read its returned documentation/state, then use its in-app browser controls. Navigate to `https://flow.google.com/` even if the current tab shows an older project. If signed out, stop at the sign-in page for the user to sign in within this in-app browser; do not switch browsers. Once the Flow main page is visible and signed in, click **+ New project**, wait for navigation, and verify a new project workspace is open. Only after these steps may you send a user-facing question, menu, or status message. Do not open, resume, or create within an older project for a fresh `FlowStart` run. Never launch, foreground, or switch to the user's external browser, and never use one as a fallback.
3. Only after the new Flow project is open, locate and read `system prompt.md` and `UNIVERSAL VIRAL VIDEO WORKFLOW.md` in the active Google-Flow workspace. The usual workspace is `C:\Users\ak\OneDrive\Documents\1 - Google-Flow`. If the active workspace differs, search the user's current project/workspace for those canonical filenames. The repository copies are the source of truth.
4. Start a fresh project state for this new project and begin at decision Gate 1, carrying forward only relevant brief details already present in this conversation. Do not resume state from an older Flow project. Resume an existing project only when the user explicitly asks to continue or resume it.
5. After each user choice, immediately show the next relevant options and continue the workflow. Keep to the canonical five-decision target and seven-decision maximum before images; bundle decisions and infer routine details. Keep choices short, numbered or lettered, and include a recommendation, “Choose for me,” and “Describe my own” when applicable.
6. If in-app browser controls are unavailable, do not substitute a question or external browser. State that the required first action could not be completed, and continue with non-browser work only if useful. If repository files are temporarily unavailable, proceed using the essential rules below and tell the user only if the missing files prevent a specific action. Never silently treat `FlowStart` as an ordinary text message.

## Essential workflow rules

- Research current, dated signals before trend, genre, hook, or platform recommendations. Cover TikTok, YouTube Shorts, and Instagram Reels, plus platforms requested by the user. Cite sources, distinguish evidence from creative inference, and never promise virality. Always include **viral micro-drama series** as a format option.
- Bundle the creative brief, audience/platform, researched direction, story, cast and voice design, locations/props, script, shot structure, aspect ratio, audio, continuity, and image plan. The user wants concise, easy selections and a complete recommended proposal rather than many appearance questions.
- Follow all twelve phases in `UNIVERSAL VIRAL VIDEO WORKFLOW.md`, including the professionally formatted Google Docs posting package in Phase 12. Maintain project continuity and the user's chosen workspace/project folder.
- Still images: ask once whether to use ChatGPT Images or Google Flow Images. That provider choice authorizes the approved planned still batch. Generate the planned images together when practical, inspect each for prompt match, continuity, physical plausibility, and visual defects, autonomously retry clear failures within scope, then present the set for selection.
- Video: Google Flow is the renderer. Before every individual video clip, present that clip's exact prompt, model, mode, ratio, duration, output count, and live displayed cost. Generate only after explicit approval of that exact clip. One clip per approval by default. Never infer video approval from `FlowStart` or image approval.
- Editing and publishing: follow the approved phase sequence and relevant available editing skill/plugin. Do not publish or post without explicit authorization.
- Be honest about browser control, saved files, generated media, and current UI/model/cost uncertainty. Verify live settings in Flow before any generation; documentation and tutorials can become outdated.
- On every fresh `FlowStart`, open `https://flow.google.com/` in the ChatGPT/Codex built-in in-app browser and click **+ New project** as the first action, before research, planning, questions, or menus. Do not reuse the project currently open or resume old project state unless the user explicitly asks to resume. For any other browser-based task or test, default to the in-app browser. Never open or switch to the user's external browser.

## Canonical workspace documents

- `system prompt.md` — standing behavior, generation approvals, user preferences, and Flow operating rules.
- `UNIVERSAL VIRAL VIDEO WORKFLOW.md` — phases, decision gates, production procedures, and deliverables.
- `GOOGLE FLOW OPERATIONS FIELD GUIDE.md` — operational detail; verify changing details against current official Flow Help.
- `GOOGLE FLOW CHARACTER AND VOICE GUIDE.md` — character identity, voice, and reference handling.

Use these files as maintained references, not as a reason to delay a clear trigger. On `FlowStart`, load the relevant documents and then proceed directly to the next action.
