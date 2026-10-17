---
name: google-flow-start
description: Start or resume the user's complete Google Flow video-production workflow. Trigger whenever the user says “FlowStart” or “Flow Start” (case-insensitive), including as a standalone message, or asks to begin or resume their Google Flow workflow. Load the workspace's canonical workflow and continue interactively; do not just acknowledge the trigger.
---

# Google Flow Start

Use this skill to activate the user's established Google Flow workflow, especially when a fresh chat has no prior conversation context.

## Startup and resume

1. Treat `FlowStart` or `Flow Start` as a direct command to start, even when it is the entire message. Do not ask what the trigger means, give a generic greeting, or stop after acknowledging it.
2. **First browser action: start a new Google Flow project in the ChatGPT/Codex built-in in-app browser, before workspace lookup, research, planning, questions, or menus.** Navigate to the Flow main page at `https://flow.google.com/` even if the current in-app tab shows an older project. If signed out, let the user sign in within the in-app browser. Once the main page loads, choose **+ New project** and verify the new project's workspace is open. Do not open, resume, or create within an older project for a fresh `FlowStart` run. Never launch, foreground, or switch to the user's external browser, and never use one as a fallback.
3. Only after the new Flow project is open, locate and read `system prompt.md` and `UNIVERSAL VIRAL VIDEO WORKFLOW.md` in the active Google-Flow workspace. The usual workspace is `C:\Users\ak\OneDrive\Documents\1 - Google-Flow`. If the active workspace differs, search the user's current project/workspace for those canonical filenames. The repository copies are the source of truth.
4. Start a fresh project state for this new project and begin at decision Gate 1, carrying forward only relevant brief details already present in this conversation. Do not resume state from an older Flow project. Resume an existing project only when the user explicitly asks to continue or resume it.
5. After each user choice, immediately show the next relevant options and continue the workflow. Keep to the canonical five-decision target and seven-decision maximum before images; bundle decisions and infer routine details. Keep choices short, numbered or lettered, and include a recommendation, “Choose for me,” and “Describe my own” when applicable.
6. If in-app browser controls are unavailable, say so plainly and do not open the external browser; continue with non-browser work only if useful. If repository files are temporarily unavailable, proceed using the essential rules below and tell the user only if the missing files prevent a specific action. Never silently treat `FlowStart` as an ordinary text message.

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
