# Generated Video Clip Reconciliation Standard

Use this gate for every project that generates clips in Google Flow or VideoExpress and then edits them in HyperFrames or another local timeline editor. A provider success message or thumbnail does not establish that the project contains every planned clip.

## 1. Create a source ledger before generation

For each planned clip record its sequence number, story/action beat, approved first/last frame IDs (when supported), final submitted prompt, provider job/library ID, requested duration, actual duration, QA status, repair history, local filename, byte size, checksum, probe result and timeline location. Keep original/rejected variants identifiable; never overwrite them or silently relabel them as passed.

## 2. Review all provider outputs

Reconcile the provider's completed items against the ledger. Open and play every full clip through the end. Inspect identity, action/cause/effect, spatial and camera continuity, exact start/end pose, black/frozen frames, unwanted subjects/artifacts, audio and measured duration. Record a pass, repair, rejected, blocked or unverified status with specific observations. Review repairs through the same full process. Do not use a toast or thumbnail as evidence of content quality.

## 3. Download and verify every accepted source

Download every approved clip and required audio into the project assets folder. For each, confirm the file exists and is nonempty, probe container/duration/dimensions/frame rate/streams, and decode or play it locally. Record a cryptographic checksum and provider ID-to-file mapping. Do not begin final timeline assembly while a required input is missing. References and storyboard stills remain references; only requested title-card art belongs as a still on the story timeline.

## 4. Reconcile the editor timeline

Before and after assembly, compare the expected approved clip count and order to the video elements/source paths in the timeline. Every approved planned clip must appear exactly once in the correct slot, and every timeline source must map to the ledger. Explicitly report missing, duplicated, substituted, rejected, or unverified clips. Confirm joins, sound/caption timing and total duration in the editor preview. A complete timeline count does not make a rejected source visually accepted.

## 5. Completion and handoff

Report both technical intake status and content-QA status. If a required clip still fails after the allowed repair attempts, keep the project marked incomplete and identify that clip and defect; do not describe the edit as finished. Run the project's HyperFrames check, review the preview, and obtain final-preview approval before rendering unless the user explicitly authorizes render without review. Apply the same source-ledger and exact-count/order gate for Google Flow and VideoExpress.

## 6. HyperFrames Studio workflow

Resume the existing HyperFrames project. If continuing after edits in the desktop app, run `npx hyperframes catch-up <project>` before modifying files. Before editing, run the project's pinned `hyperframes timeline --json` and compare its video rows/source paths with the approved ledger. Keep one distinct ordered video row for each planned story clip; references remain out of story-shot slots, and requested title-card art is a separate opening graphic. Preserve approved story order, verified source ranges, audio, captions and runtime. If a cut changes duration, update downstream starts, cue timings and subtitle files together. After editing, recheck timeline count/order/paths, run the pinned project check, snapshot changed sections, and inspect those moments and joins in the Studio preview. A structural pass does not establish visual or audio QA; report those statuses separately. Leave the editable preview available and wait for final-preview approval before delivery render unless rendering without review was explicitly authorized.
