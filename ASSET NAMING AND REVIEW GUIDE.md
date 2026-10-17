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

## Shared clip-boundary stills

For storyboard stills that bridge consecutive clips, one approved image has two roles: it is the outgoing clip's planned end target and the next clip's planned start. Show both roles in a compact Flow title, for example `EP1 S02 — C01 END / C02 START`; keep the full story beat and IDs in the ledger and detailed filename, e.g. `EP01_SHOT_02__CLIP_01_END__CLIP_02_START__reset-reveal_v01.png`. Use zero-padded IDs in filenames and record the continuity segment in the ledger. Do not create separate near-duplicate images for the same planned boundary. An image can serve both roles only when adjacent clips are truly continuous; begin a new segment at an intentional reset, scene/time discontinuity, or other approved break.

When preparing clip input folders, copy the exact approved boundary asset into each adjacent clip folder using role-specific names such as `CLIP_01_END_FRAME_SHOT_02.png` and `CLIP_02_START_FRAME_SHOT_02.png`; verify the copies are pixel-identical. These are **planned storyboard boundaries**. After the outgoing video is generated, inspected, and approved, extract its exact final displayed decoded frame losslessly and use that actual frame as the next clip's start input when supported. Keep the planned boundary as the comparison/end target. Never rename a planned still as an actual generated endpoint, and never prepare a dependent video as though its predecessor's endpoint exists before it has been extracted and accepted.

## Generation and review procedure

1. Assign identifiers in the image/clip plan before generation. When a result completes, match its prompt, thumbnail, and asset identity to that plan, then rename it immediately. Verify the title saved in the live UI. Name imported assets after upload as well.
2. Keep an asset ledger in the local project folder. Record identifier, exact Flow title, asset URL/ID, role/story position, version, prompt/reference inputs, review status, and verified local path when downloaded. Use statuses such as `REVIEW`, `APPROVED`, `REVISE`, or `SUPERSEDED`; generation or QC alone never means user approval.
3. Keep the identifier stable through revisions. Use `SHOT 05 — Warning at the front door — v02` when multiple versions coexist; identify the superseded version in its title/ledger. Never renumber the other shots because a version was rejected. Add suffixes such as `SHOT 05A` for an inserted frame when needed, and update the frame/clip map.

4. Before asking for selection, verify that every active review tile is labeled and that the ledger matches it. Present a compact numbered list or labeled contact sheet so the user can say “keep SHOT 01, revise SHOT 05.” State which versions are recommended and which are approved. Flow may display recent activity rather than story order; use title sorting when the live UI supports it, or explain the display order.
5. Keep useful alternates clearly labeled. When the user authorizes cleanup, identify superseded assets by prompt and asset identity, move those exact assets to Flow Trash, and verify the remaining review count. Do not permanently delete them or discard useful originals without the required authorization. Naming itself requires no extra approval.
6. Preserve identifiers on download: for example `EP01_SHOT_05_warning-at-front-door_v02.png`, retaining the actual source extension. Put them in the existing project folder and update the ledger with real paths. Use the same identifiers in prompts, start/end frame maps, clip approvals, edit timelines, captions notes, and delivery manifests.

## Reference verification and Agent mode

Before each storyboard generation, use a shot-level ingredient checklist: every visible saved Character, the exact location sheet/clean plate, each salient prop sheet, and a prior approved frame when needed for direct continuity. Attach the real assets from the active Flow project and verify their displayed thumbnails/names and roles before generation. Merely naming a reference in the prompt does not condition the image.

Flow Agent can help with tasks that need project context or several references, but it can rewrite prompts and omit or mis-map ingredients. Use it only when the live UI lets you verify the final prompt and actual references; explicitly map each attached item to its role, inspect the generated result, and fall back to the standard composer if attachments cannot be verified. Never treat an Agent's statement that it used an asset as proof. Keep work in the active in-app browser and project.

Use a per-shot production checklist and do not advance until the result is present, visually checked, titled in Flow, and recorded in the ledger. Verify the saved title immediately after renaming. At batch end, reconcile the planned shot list against the gallery and ledger, label drafts/alternates/superseded items, and flag missing or unverified shots. A generation-complete notice is not visual approval; visual acceptance is not user approval. Retain a rejected tile until a replacement passes QC; any cleanup must target a clearly identified asset and use recoverable Trash where available.

## Resolution and free upscaling

**Storage comes first:** keep Flow-generated images in Flow and reuse them there for video. Review and label them in Flow; the ledger needs their Flow identity/status, with a local path marked not needed. Do not download them merely for workspace staging or a contact sheet. Download only for the user's requested export/backup or a concrete external task. Save ChatGPT-generated image files into the local project folder when accessible, then upload them to Flow. The resolution rule below applies to necessary exports; a download-only upscale is not a prerequisite to using a saved Flow image.

Choose the highest supported resolution with no added money or credit cost and no plan upgrade. In Flow, free 2K image upscaling is the standard when offered; prefer it over a 1K-only delivery. Check live availability and cost evidence rather than treating every upscale as free. No extra user question is needed for a verified free upscale. Preserve useful originals and identify the upscaled file, for example `EP01_SHOT_05_warning-at-front-door_v02_2K.jpg`. Verify decoding, real pixel dimensions, aspect ratio, identity, wardrobe/color, and physical geometry after upscaling; do not infer resolution from the filename or claim native 2K detail. Record actual width/height, source/upscaled status, file path, and any observed cost in the ledger. Use the best confirmed free option if a higher tier is paid, unavailable, or its cost is unclear; do not purchase a plan upgrade. Apply the same preference to free video export upscaling while retaining paid clip approval requirements.

## Final review check

Before saying a batch is ready, verify that no active review asset has an unexplained automatic title, each identifier maps to one intended role and distinguishable version, and the user's feedback can be resolved to an exact asset. If renaming is unavailable, provide a labeled local preview and ledger with exact asset links, disclose the UI limitation, and complete the Flow title when possible. Do not claim a rename or download that has not been verified.
