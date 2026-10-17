# Asset naming and review

Naming is a required production step. Every generated or imported reference, storyboard still, screenshot, and video clip must have a stable, readable label before it is presented for review or reused. Set the actual asset title in Flow; a label written only in chat or a local note is insufficient. For external media, use the same identifier in the local filename and in Flow after upload. Never leave the review set with automatic titles such as “Man reading paper.”

## Labels and order

| Asset | Title format | Example |
|---|---|---|
| Character, location, or prop reference | `REF 01 — Short description` | `REF 02 — Sixth passenger and red scarf` |
| Storyboard still | `SHOT 01 — Story beat` | `SHOT 05 — Warning at the front door` |
| Generated video | `CLIP 01 — Story beat — v01` | `CLIP 01 — Last bus arrives — v02` |
| Captured UI screenshot | `SCREENSHOT 01 — What it documents` | `SCREENSHOT 01 — Clip settings before generation` |

Use two-digit numbers in story order, assigned in the approved asset plan. Keep references separate from storyboard numbering. In a series project containing multiple episodes, prefix story assets with the episode, for example `EP01 SHOT 05 — Warning at the front door`. Keep descriptions short enough for tile labels to remain useful. Do not burn labels into reference images or video frames unless requested; titles, filenames, and the review list provide the labels.

## Generation and review procedure

1. Assign identifiers in the image/clip plan before generation. When a result completes, match its prompt, thumbnail, and asset identity to that plan, then rename it immediately. Verify the title saved in the live UI. Name imported assets after upload as well.
2. Keep an asset ledger in the local project folder. Record identifier, exact Flow title, asset URL/ID, role/story position, version, prompt/reference inputs, review status, and verified local path when downloaded. Use statuses such as `REVIEW`, `APPROVED`, `REVISE`, or `SUPERSEDED`; generation or QC alone never means user approval.
3. Keep the identifier stable through revisions. Use `SHOT 05 — Warning at the front door — v02` when multiple versions coexist; identify the superseded version in its title/ledger. Never renumber the other shots because a version was rejected. Add suffixes such as `SHOT 05A` for an inserted frame when needed, and update the frame/clip map.
4. Before asking for selection, verify that every active review tile is labeled and that the ledger matches it. Present a compact numbered list or labeled contact sheet so the user can say “keep SHOT 01, revise SHOT 05.” State which versions are recommended and which are approved. Flow may display recent activity rather than story order; use title sorting when the live UI supports it, or explain the display order.
5. Keep useful alternates clearly labeled. When the user authorizes cleanup, identify superseded assets by prompt and asset identity, move those exact assets to Flow Trash, and verify the remaining review count. Do not permanently delete them or discard useful originals without the required authorization. Naming itself requires no extra approval.
6. Preserve identifiers on download: for example `EP01_SHOT_05_warning-at-front-door_v02.png`, retaining the actual source extension. Put them in the existing project folder and update the ledger with real paths. Use the same identifiers in prompts, start/end frame maps, clip approvals, edit timelines, captions notes, and delivery manifests.

## Completion check

Before saying a batch is ready, verify that no active review asset has an unexplained automatic title, each identifier maps to one intended role and distinguishable version, and the user's feedback can be resolved to an exact asset. If renaming is unavailable, provide a labeled local preview and ledger with exact asset links, disclose the UI limitation, and complete the Flow title when possible. Do not claim a rename or download that has not been verified.
