# Google Flow Workflow

An approval-driven production playbook for planning original short-form stories, creating reference images with the user's chosen image provider, rendering video in Google Flow, editing clips into a sequence, and preparing platform-specific publishing materials.

## The workflow at a glance

![Google Flow viral video workflow diagram](assets/google-flow-viral-workflow.svg)

**Core rule:** still-image production always begins with a provider choice—ChatGPT Images or Google Flow Images. Videos render in Google Flow, and each video clip requires explicit approval of its prompt, settings, and displayed credit cost before generation.

**Start the workflow by saying `FlowStart`.** It begins at visual-style selection, then advances through the phases while preserving all concept, image, cost, clip, editing, and publishing approval gates.

## Documents

- [Universal Viral Video Workflow](UNIVERSAL%20VIRAL%20VIDEO%20WORKFLOW.md) — the complete 12-phase workflow, including image-provider choices, per-clip Flow video approval, Scenebuilder cuts, Flow Agent edits, Extend limitations, continuity checks, and posting package.
- [System Prompt](system%20prompt.md) — standing assistant behavior and current beginner Google Flow procedures.
- [Video Editing Prompt](video%20editing%20prompt.md) — copy-ready template for planning and editing a project.
- [Style Library](STYLE%20LIBRARY.md) — the 243 style options from the supplied master prompt, with catalog codes.
- [Workflow Diagram](assets/google-flow-viral-workflow.svg) — visual overview.

## Default image and video controls

| Work | Default | Approval rule |
|---|---|---|
| Image generation | Ask ChatGPT Images or Google Flow Images; 9:16 portrait; one image per prompt. Flow image model: Nano Banana 2.1. | Ask the provider choice before image work. Review results and offer rerun/provider switch if needed. Large Flow batches are optional and require the user's choice after showing count/cost. |
| Video rendering | Google Flow only; one clip at a time; verify supported mode, model, aspect, duration, output count, and current credit cost. | Require explicit approval for each specific clip and settings before Generate. Re-approval is required after a material change. |
| Basic editing | Flow desktop Scenebuilder: arrange clips, reorder, trim in/out, preview, and download. | Preserve originals. AI-assisted edits/extensions are media generation and need their own cost approval. |

These defaults reflect the user's requested workflow, not a promise that every feature is available in every account or region. Check the live Flow interface and its displayed costs each time.

## Flow editing essentials

1. Add accepted clips to a Scene/Scenebuilder, arrange them in story order, and use each clip's handles to trim its beginning and end.
2. Preview the complete sequence and inspect cuts for clipped dialogue, unfinished movement, repeated frames, awkward pacing, or abrupt audio changes.
3. Use Agent/video editing for a focused change to a selected clip. Say what must stay fixed and change one main thing at a time. Compare versions in History/asset stack; keep the original.
4. Extend a clip only when the selected model supports it. Confirm the exact model, limitation, duration, and cost before approval.
5. Download the scene and verify the file. Use a dedicated editor for detailed audio mixing, captions, titles, grading, or frame-accurate finishing beyond Flow's current controls.

Google's current Help Center documents the desktop editor and Scenebuilder here: [Edit videos and build scenes in Google Flow](https://support.google.com/flow/answer/16935718?hl=en). Model compatibility, upload constraints, geography, and costs can change.

## Approval checkpoints

The phases are: **Style → Story → Cast → Runtime/Scenes/Shots → Speech/Audio → Format/Platforms → Concept Approval → Text Production Package → Images → Flow Video Clips → Editing Handoff → Posting Package**.

- Concept approval locks the creative plan, not generated assets.
- Image provider selection happens before images are made. Generated images are checked against their prompts and continuity references.
- Each Flow video generation is an individual spend decision. The assistant must show the exact clip, model/mode, frame inputs, orientation, duration, output count, prompt, and live cost, then wait for explicit approval.
- Editing preparation, a ZIP, or a finished prompt is not permission to render video or publish.

## Updating the knowledge base

Prefer official Google Flow Help for current interface/model details. Treat tutorial recordings as examples rather than guarantees. When updating this repository, record newly observed behavior, which model/mode was selected, what was verified in the UI, and any limits or region/account caveats. Never record private account details or claim an action succeeded without evidence.

## Sources

- [Google Flow Help Center](https://support.google.com/flow/)
- [Create videos in Flow](https://support.google.com/flow/answer/16353334?hl=en)
- [Use the Flow Agent](https://support.google.com/flow/answer/17093911?hl=en)
- [Edit videos and build scenes](https://support.google.com/flow/answer/16935718?hl=en)
- [Models and supported features](https://support.google.com/flow/answer/16352836?hl=en)
- [Manage Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
