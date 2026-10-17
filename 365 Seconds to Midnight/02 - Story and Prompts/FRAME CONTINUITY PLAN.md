# 365 Seconds to Midnight — Frame Continuity Plan

**Purpose:** Keep every clip's opening frame tied to the previous approved clip's real final frame, with a shared approved storyboard boundary planned in Phase 9.
**Status:** Mapping recorded; actual video clips/endpoints do not exist yet. The SHOT assets are planned storyboard frames, not generated clip endpoints.

## Core rule

Within one continuous segment, a shared storyboard still has two roles: the outgoing clip's end target and the incoming clip's planned start. After a video is generated, inspected, and explicitly approved, extract its exact final displayed decoded frame losslessly. That actual frame becomes the next clip's start input where the selected model supports it; the next SHOT remains its end target. Do not use a storyboard still as if it were an actual generated video endpoint.

Each of the six episodes is a separate continuity segment because its opening is a new time-loop reset. Therefore the current plan is 18 clips + 6 segments = 24 storyboard boundaries. The episodes do not share a boundary across the reset.

## Planned boundary map

| Episode segment | Clip | Planned start boundary | Planned end boundary | Shared role at end |
|---|---:|---|---|---|
| EP1 | CLIP 01 | SHOT 01 | SHOT 02 | CLIP 01 END / CLIP 02 START |
| EP1 | CLIP 02 | SHOT 02 | SHOT 03 | CLIP 02 END / CLIP 03 START |
| EP1 | CLIP 03 | SHOT 03 | SHOT 04 | Segment end |
| EP2 | CLIP 04 | SHOT 05 | SHOT 06 | CLIP 04 END / CLIP 05 START |
| EP2 | CLIP 05 | SHOT 06 | SHOT 07 | CLIP 05 END / CLIP 06 START |
| EP2 | CLIP 06 | SHOT 07 | SHOT 08 | Segment end |
| EP3 | CLIP 07 | SHOT 09 | SHOT 10 | CLIP 07 END / CLIP 08 START |
| EP3 | CLIP 08 | SHOT 10 | SHOT 11 | CLIP 08 END / CLIP 09 START |
| EP3 | CLIP 09 | SHOT 11 | SHOT 12 | Segment end |
| EP4 | CLIP 10 | SHOT 13 | SHOT 14 | CLIP 10 END / CLIP 11 START |
| EP4 | CLIP 11 | SHOT 14 | SHOT 15 | CLIP 11 END / CLIP 12 START |
| EP4 | CLIP 12 | SHOT 15 | SHOT 16 | Segment end |
| EP5 | CLIP 13 | SHOT 17 | SHOT 18 | CLIP 13 END / CLIP 14 START |
| EP5 | CLIP 14 | SHOT 18 | SHOT 19 | CLIP 14 END / CLIP 15 START |
| EP5 | CLIP 15 | SHOT 19 | SHOT 20 | Segment end |
| EP6 | CLIP 16 | SHOT 21 | SHOT 22 | CLIP 16 END / CLIP 17 START |
| EP6 | CLIP 17 | SHOT 22 | SHOT 23 | CLIP 17 END / CLIP 18 START |
| EP6 | CLIP 18 | SHOT 23 | SHOT 24 | Final endpoint |

## Naming convention

Keep each existing `SHOT_XX` identifier stable. For each shared frame, name the Flow asset so the dual clip role is visible, for example:

- Compact Flow title: `EP1 S02 — C01 END / C02 START`
- Full beat and IDs in ledger; export filename: `EP01_SHOT_02__CLIP_01_END__CLIP_02_START__reset-reveal_v01.jpg`
- In per-clip folders: `CLIP_01_END_FRAME_SHOT_02.jpg` and `CLIP_02_START_FRAME_SHOT_02.jpg`

The two folder copies must be pixel-identical and keep the actual source extension. At an episode reset, use a new segment opening label, such as `EP2 SHOT 05 — CLIP 04 START — Loop Reset`; do not describe it as CLIP 03's end.

## Phase 10 handoff record

For every clip, record: clip ID/title, episode segment, duration, planned start/end SHOT IDs and asset IDs, actual start input, accepted predecessor clip/version, extracted predecessor endpoint path and extraction frame/time, model/mode, audio/dialogue, generation version, review status, and user approval. Extract the last displayed decoded frame from the approved video at native resolution; do not use a black trailing frame or an approximate player screenshot. Compare each next clip's actual first displayed frame to that accepted endpoint. If model conditioning does not support the needed frame input, mark continuity as unsupported/unverified and resolve through a user-approved compatible method before continuing.

## Existing prompt-pack note

`Video Prompts 06-24.md` was authored as one prompt per supplied SHOT still, with that image described as the source/first frame. It predates this paired-boundary workflow and is **not a Phase 10 paired-frame prompt pack**. Before video generation, author each actual clip prompt against the start/end mapping above, include both frame file identities, and describe the action/camera/sound path between them. The individual shot prompts may inform story beats, but they do not establish shared endpoints by themselves.
