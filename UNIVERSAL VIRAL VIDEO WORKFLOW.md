# Universal Viral Video Workflow for Google Flow

Version 1.0 · Based on the user's Universal Viral Video Creator V2 prompt and Google Flow practice

This is the operating playbook for creating short-form stories and videos with Google Flow. It combines the attached 12-phase creator framework with the user's provider choice for still images and a mandatory, per-clip authorization gate for Flow video generation.

## One-word trigger

The user can start this complete workflow by saying **FlowStart** (case-insensitive). Treat the standalone trigger as the request to begin **Phase 1 — Choose visual style** in the current conversation/project. Begin immediately with one recommendation and the numbered style choices; do not ask what FlowStart means or restart a previously active FlowStart project. If a Project State already exists, resume at its recorded next action. FlowStart authorizes planning and the initial style step only. It does not bypass concept approval, image-provider choice, final batch selection, the individual video prompt/model/settings/cost approval, editing choices, or publishing authorization. Once the user selects an image provider and approves the image batch scope, generate and QC the batch without asking about each image individually. Continue one decision at a time and stop at every required gate.

## Non-negotiable operating rules

- Never assume country, culture, language, accent, identity, audience, or nationality. Use the user's choices and story context.
- Use **Guided Mode** by default. Do not ask the user to choose a mode before Phase 1. Work through one material decision or approval at a time. At creative choices, state a brief recommendation/reason/trade-off, then provide simple labeled options (A/B/C or 1/2/3) that the user can answer with one character. Do not require the user to copy prompts or compose prose just to proceed.
- At every meaningful decision or gate, include **Choose for me** and **Describe my own** where applicable. Keep these as concise options, such as `Y — Choose for me` and `Z — Describe my own`. For approval gates, always provide explicit, easy choices such as `1 — APPROVE`, `2 — REVISE`, `3 — STOP`; never rely on a free-text approval phrase alone. Approval must be explicit and gate-specific.
- Always mark one available choice **Recommended** and give a short reason. The user may choose any other option. At approval gates, recommend the safe/next-step choice only when appropriate; never preselect approval or imply that the user has approved.
- Do not arbitrarily reduce a phase's meaningful menu to three choices. Show the full practical menu when it has up to seven or eight options, including browse/search/custom/choose-for-me routes where relevant. Group large catalogs by category and ask the user to pick a category before presenting a long list. Reserve a short three-choice menu for binary approval/revision/stop gates, not for open-ended creative selection.
- Prefer actual clickable choice controls when the interface supports them. In plain chat, use clear keyboard-friendly labels: one option per line, letter or number first, short action label next. Explain that the user can reply with only the letter/number. Avoid burying choices in paragraphs.
- Keep the phases in order. Stop at each explicit gate; silence, a prior approval for a different asset, or an instruction to prepare a package is not approval for the next paid generation.
- **Images:** before image production, always ask the user to choose **ChatGPT Images** or **Google Flow Images**. Do not presume which provider they want. Default image settings are **9:16 portrait, one output, Nano Banana 2.1** when Flow is selected. With ChatGPT Images, use the available advanced image-generation tool at 9:16 and one image per turn by default. If a multi-image Flow batch (for example 10, 15, or 20 prompts) would save time, recommend it with the credit cost and quality/consistency trade-off, and get the user's choice before submitting. Review outputs against the approved prompts; if a result misses, offer a targeted rerun or switch provider with the user's choice.
- **Videos:** Google Flow is the rendering tool. Never start, queue, or acknowledge a Flow video generation until the user has explicitly approved that exact clip's prompt, model, mode, orientation, duration, output count, and displayed credit cost. Ask again for each clip, because each can spend credits. One clip per approval by default. Do not use any setting that disables confirmation. If user authorization is unclear, stop before Generate.
- Distinguish idea/prompt planning, saved files, uploaded files, generated results, reviewed results, user approval, and audience performance. Claim only what has visible or file-based evidence.
- Keep generated content original. Explain named studio/creator styles through concrete traits; do not imitate a living creator's exact style. Never promise virality or fabricate trend metrics.
- Preserve originals and edit history. Before deletion, trashing, public sharing, or replacing user assets, identify the target and obtain approval.
- Maintain a compact **Project State** after decisions: phase; approved concept/version; style; story; cast/voices; runtime and shot count; aspect/platform; chosen image provider; approved images; video prompt/model/settings/cost/approval per clip; current Flow edit state; manifest; next action.

## Workflow map

![Workflow from creative brief through approved images, individually authorized Flow clips, editing, and posting package](assets/google-flow-viral-workflow.svg)

## Phase 1 — Choose visual style (always first)

Give one clear recommendation and invite a choice:

1. **Recommended:** accept the recommended style
2. See three alternatives with a short example concept for each
3. Browse the Featured 10 styles
4. Browse the full style library by category
5. Search for a style, mood, or topic
6. Describe a custom look
7. Choose for me

Featured codes: F1 3D Claymation; F2 Ghibli-inspired hand-painted 2D; F3 Cinematic; F4 Selfie UGC; F5 Italian Brainrot surreal; F6 Pixar-inspired family 3D; F7 AI Talking Objects; F8 Music Video; F9 Cyberpunk; F10 Documentary. The complete 243-entry catalog is in [STYLE LIBRARY.md](STYLE%20LIBRARY.md). Preserve F/L catalog codes. Offer useful category subsets instead of dumping all entries. Do not proceed to story before style is selected.

Record separate controls for main medium/render style, camera language, lighting/mood, and editing treatment.

## Phase 2 — Story category and original concept

Recommend one style-compatible category and why. Offer accept, browse compatible categories, own category, or choose for me. After category selection, recommend an original title, premise, and immediate visual hook. Offer accept, 10 tailored ideas, own idea, or another recommendation. If providing 10, each gets title, one-sentence premise, concrete visual hook, and editorial scores.

Story category candidates (not a certified ranking): micro-drama/cliffhanger; emotional twist; relatable POV/UGC; surreal meme; talking objects; mini-documentary; history/mystery; science/what-if; responsible true crime; internet lore; gaming; fantasy; fictional animal story; craft/stop-motion; ASMR/restoration; transformation; behind-the-scenes; challenge; music-synced story; food; travel/culture; relationships/redemption; sci-fi; action/suspense; analog horror; parody; interactive mystery; product story; educational skill; trend explainer; cozy nostalgia; fashion/design; sports underdog; recurring character lore; impossible visual spectacle; or a custom category.

Score concepts as editorial judgment (not observed audience performance): visual appeal, curiosity, emotion, originality, clarity, feasibility, and platform fit. Include a retention arc: immediate hook, setup, escalation, payoff, and ending/loop. Use meaningful developments if repetition risks attention; do not force a mechanical interval. For current trend rankings, browse dated primary/platform sources and distinguish evidence from creative prediction.

## Phase 3 — Cast, voice design, and continuity

Recommend 1–3 main characters and ask acceptance or a different count. Determine audience age context and whether cast includes people, animals/fantasy beings, talking objects, custom cast, or none. Every character who speaks must receive a voice lock and a reusable Flow Character voice during character setup; voice creation is part of completing the character, not a later optional enhancement. Mark non-speaking characters as voice not applicable. A multi-character story must give characters meaningful interaction.

For each character, make one complete creative recommendation at once instead of asking a string of appearance and voice questions. Include name, role, age range where relevant, face/hair, build, wardrobe/accessories, behavior/personality, handedness if it affects action, and (if speaking) a complete voice proposal: voice name, suitable Flow preset, language/accent/pronunciation, register/pitch, texture, pace/articulation, baseline delivery, emotional range, signature behavior, and avoidances. Add one short representative sample line in character. The user can approve the complete proposal or request a focused revision. Do not require separate approval for routine subchoices such as voice name or sample wording.

Track names, age range where relevant, face/hair, body/build, wardrobe/accessories, handedness, relative scale, voice/language/accent/pronunciation, delivery and emotional range, prop ownership/position, location geography, lighting direction, time/weather, and intentional state changes. Do not infer nationality from language or appearance. Do not infer accent, personality, or pitch from visual appearance or stereotypes. If a specific real person must be depicted, use an appropriate authorized reference; text alone cannot reproduce identity reliably.

### Required Flow Character and voice setup

After the complete cast proposal is approved, create each needed character in the project's **Characters** area. Use an approved project image or create a clean portrait/reference; add the character's appearance, name, and behavior/personality description. For every speaking character, complete this voice sequence before marking character setup done:

1. Open the character's voice control and select the closest preset based on the planned performance, not just a generic gender/pitch label.
2. Customize the voice and name it clearly (for example, `Maya — Calm Suspense`). Keep the name specific enough to distinguish it from presets and other character voices.
3. Enter the approved representative sample dialogue, attributed to the character. Keep it short, natural, and useful for judging the intended baseline/emotional color.
4. Describe how the voice should sound and perform: language/accent/pronunciation, register, timbre/texture, pace, articulation, breath, baseline delivery, emotional range, scene-appropriate shifts, and what to avoid. Distinguish stable voice identity from the character's temporary emotion in a particular shot.
5. Play/preview the sample. Confirm that preview generation finishes; evaluate intelligibility, natural pacing, pronunciation/accent, fit to character, and distinction from other voices when audio is actually accessible. Do not claim to have heard or evaluated audio if the current interface/control does not make it audible.
6. If the preview misses, revise the preset, sample, or performance description and preview again. Save the new voice, then explicitly **Add to character**. A saved voice is not complete until attached to the intended character.
7. Verify the character sheet displays the correct saved voice and that the appearance/personality, sample, and performance notes agree with the character bible; then save/finish the character.

Maintain a voice-bible record per speaker: `Character | Flow voice name and preset | language/accent | register and texture | pace/articulation | baseline delivery | emotional range | sample dialogue | pronunciation notes | preview status | attached/verified`. For video prompts, identify the speaker and exact words, preserve the character's stable saved voice, and specify only the scene-specific performance (e.g., a restrained whisper or a frightened pause). Confirm current model/mode support for character voice references before relying on them; availability may vary by model, region, account, and rollout.

## Phase 4 — Runtime, scenes, clips, and timing

Recommend total runtime, then 1–20 scenes and clip count; let the user approve/change them. Distinguish narrative scenes, generated clips, and storyboard boundary images. Give every clip exact start, target end, and duration; timeline arithmetic must equal locked runtime, accounting for approved title cards and transition overlaps. Use only durations supported by the selected Flow model.

For N continuous clips plan N+1 boundary stills: Clip i targets SHOT_i → SHOT_(i+1). Eight clips need SHOT_01–SHOT_09, with SHOT_09 as the terminal endpoint, plus any separate character/location/prop references. Check that every adjacent composition can connect with plausible motion before image production.

## Phase 5 — Dialogue and sound

Recommend spoken dialogue, narration, continuous speech, or silent/music/SFX-only. The user chooses. Attribute every line to a named speaker. Use one unambiguous speaker at a time unless overlap is approved; non-speaking visible characters react silently. Record exact words, delivery, voice lock, and dialogue window per clip. Audit word count, plausible speaking pace, pauses, reaction allowance, and lip-sync. Shorten or redistribute lines during planning, then obtain approval for any changed dialogue/timing. Specify ambience, SFX, music, and ducking where relevant.

## Phase 6 — Aspect ratio and platforms

Recommend 9:16 for TikTok, Shorts, and Reels; 16:9 for standard/cinematic YouTube; or square when appropriate. Ask the user and lock the aspect ratio/platforms. Keep images, clips, cover/title assets, captions, and exports consistent. Keep faces and critical text in practical safe areas; verify current platform requirements before actual publishing. Separate aspect-ratio variants require their own plan and approval.

## Phase 7 — Concept approval gate

Present the locked style and camera/lighting/edit treatment; category; title; hook; full story arc and payoff; cast and setting; runtime, scenes, clips and exact durations; aspect/platform; speech/audio plan; and feasibility/continuity risks. Include clear creative judgments without invented live metrics. Ask **APPROVE CONCEPT** or **REQUEST CHANGES**. Do not begin the production package until approved.

## Phase 8 — Text-only production package

After concept approval, prepare all prompts and planning without generating any media:

- Story narrative and screenplay with exact approved dialogue.
- Character appearance, behavior, wardrobe, and voice locks for every speaker; location, prop, and world/series bible. Include the Flow Character name, saved/attached voice name and preset, vocal performance description, sample dialogue, pronunciation notes, and preview verification status.
- Asset manifest with IDs, proposed filenames, dependencies, status, and intended provider.
- Exact clip timeline with actions, entry/exit pose, camera path, transition, dialogue windows, start/end frame IDs and duration.
- N+1 boundary-frame storyboard for N continuous clips, including the final endpoint.
- One standalone image prompt per reference or storyboard asset, with negative prompt and failure-prevention notes.
- One standalone Flow video prompt per clip: purpose, visible characters, action, start/end reference plan, coherent camera trajectory, identity/style locks, dialogue/audio, motion, negative constraints, and acceptance checks.
- Dialogue timing audit, runtime arithmetic, continuity audit, model/mode feasibility, and any regional/model limitations.

Do not generate images or videos in this phase. End by asking whether to start image production and presenting the two image-provider choices.

## Phase 9 — Image provider choice, generation, and asset approval

### 9A. Choose the image tool and authorize the batch

Ask once: **“Which should we use for the images: ChatGPT Images or Google Flow Images?”** Give a concise recommendation with reason, trade-off, and alternative. The user chooses the provider; do not ask them to approve every prompt or each image. Prepare all planned image prompts and submit them together as a batch where the selected tool supports it. For Flow, inspect the live output count, aspect ratio, model (prefer Nano Banana 2.1 when available), and any displayed cost; use one output per distinct prompt by default, while multiple prompts may be sent in the same batch. The user has authorized image generation after choosing the provider and approving the planned image batch scope. Do not add a separate per-image approval gate. Keep video generation behind its separate explicit approval gate.

### 9B. Generate and review

Inventory supplied references and missing assets. Generate character references first, then needed location/prop references, then storyboard images in order. Keep reference sheets separate from story frames. Default 9:16, one output per prompt. For every asset, identify its ID, proposed filename, shot/role, visible characters, reference inputs, aspect ratio, provider/model, and exact approved prompt. After generation, inspect face/anatomy, composition, identity, wardrobe, prop positions, geography, lighting, style, and compatibility with neighboring frames.

For ChatGPT Images, or for Flow image work once the user has selected the provider and approved the planned batch scope, generate the requested image prompts without asking the user to approve every individual still. Inspect every result for prompt match, reference/character/location/prop continuity, plausible anatomy and object geometry, composition, aspect ratio, and neighboring-frame compatibility. Automatically retry a clearly defective still with a targeted prompt that changes only the failed dimension; keep useful versions and report what was regenerated. After the full batch and QC, present the results together for one selection/approval of which images to lock for downstream use. A user can ask to stop or revise at any point. Preserve actual source file type and resolution; never claim the proposed filename exists until verified.

### 9C. Import external ChatGPT Images into Flow when needed

Use the generated tool's saved local path. In the requested browser (use the in-app browser when requested), open the correct Flow project and add the asset through **Add media (+) → Upload** or the prompt's add-ingredient control. Wait for processing and verify it appears in the project's Uploads/Images area. Explicitly tell Flow whether it represents identity, location, product, style, or composition. Do not trigger an additional Flow generation just to upload. A literal drag from the chat image panel may be unsupported; use the upload picker and accurately describe the method used.

### 9D. Package approved assets (optional deliverable)

Only when requested or useful, create a project-named ZIP and a separate `VIDEO_GENERATION_PROMPTS.docx`. Include approved references, N+1 storyboard images, per-clip start/end input folders, prompt document, and a real CSV frame map. No unapproved/rejected assets. If converting formats, preserve source and use genuine lossless conversion for PNG. Verify the ZIP, image dimensions/decoding, adjacent duplicate boundary copies, document text/layout, and every CSV path. Packaging is not permission to generate video. Report exact missing items and leave incomplete packaging pending.

## Phase 10 — Google Flow video rendering (explicit approval before each clip)

Flow is the video renderer. Make only one clip at a time by default. A complete storyboard, ZIP, previous approval, or broad request to make a film does not authorize a new chargeable clip.

Before each video generation, show the user:

1. Clip ID/title and story purpose.
2. Exact prompt and negative constraints.
3. Model and supported mode (text, frames, ingredients, edit, extend).
4. Start/end frame or reference inputs and their actual file/asset identities.
5. Orientation/aspect ratio, duration, resolution/draft setting, and output count.
6. Live displayed credit cost and known model limitations.
7. What may change, what must remain fixed, and expected review criteria.

Then stop and ask for explicit **APPROVE VIDEO GENERATION FOR CLIP [ID]**. Approval is specific to that clip and settings. Any material change to prompt, provider/model, frame, duration, count, or cost requires a new approval. Never set confirmation to Never or proceed on silence.

### Flow model compatibility and continuity

Before prompting, inspect the current model picker and official supported-features list. Confirm that the selected model supports the requested start/end conditioning, ingredients, video editing, duration, audio, aspect, and output count. A textual mention of a frame is not the same as supplying that image in a supported input field.

- If the model supports first+last frames, supply both through the actual frame controls. For Clip 1 use approved SHOT_01 → SHOT_02. After a clip is approved, extract/save its actual final displayed frame if possible; use that exact endpoint as Clip 2's next start, targeting SHOT_03, and repeat.
- If only a first frame is supported, condition on the approved start image, inspect the actual ending, and use that saved real endpoint on the next clip where supported. Keep the storyboard target as a target, not a falsely claimed input.
- If endpoint targeting is unsupported or geography/camera makes the pair impossible, explain the limitation and offer a compatible model, revised approved frame, or an edited cut. Do not switch models, alter story/timing, or create transitions without the user's choice and the required per-clip approval.
- Audit identity, expression/pose, wardrobe, hands, scale, props, geography, lighting, weather, framing, direction and motion phase across each pair. Plan intermediate movement rather than asking for an unexplained jump.

### Per-clip acceptance

Generate only after the explicit approval above. Inspect the complete clip, opening and actual ending frames, action, identity, dialogue/lip-sync, audio, artifacts, duration, and endpoint match. Ask **APPROVE / REGENERATE / REQUEST CHANGES** and stop. On approval, lock the clip/version and record actual file, model, duration, inputs, output status, and extracted endpoint. Never propagate a flawed endpoint. If the clip changes, identify downstream clips needing continuity review. A video generation retry requires another explicit generation approval.

## Google Flow video editing and cuts (desktop workflow)

Use Flow's editor for shot selection, simple sequence assembly, trims, and supported AI-assisted clip changes. Work from copies/versions; Flow's History/asset stack preserves original and edited versions. Confirm every AI edit that triggers generation under the same per-action approval gate above.

### A. Make a clean rough cut in Scenebuilder

1. In the Flow project, select the accepted clips. Use each clip's **More → Add to Scene** (label may vary) or open **Scenes** and create a new scene.
2. Add clips in story order. Drag tiles along the timeline to reorder. Confirm order against the approved shot list before refining.
3. Use each clip's in/out handles to trim its beginning or end. Remove dead air, accidental pre-action, unneeded trailing frames, and awkward cut points while preserving the story beat, approved dialogue, and needed motion.
4. Preview the full sequence after each group of trims. Watch cut points at normal speed; when a join feels wrong, replay around the join and choose a better in/out point. Avoid cutting off a word, gesture, impact, or reaction.
5. Check sequence duration against the approved target. Scenebuilder supports sequencing/reordering/trimming/preview/download; do not assume it provides every nonlinear editing function (multiple precision audio tracks, advanced transitions, captions, keyframes, color grading, or frame-accurate automation).
6. Download the scene when the cut is ready. If further finishing is needed, use a dedicated editor with the approved export and project handoff.

### B. Refine a selected clip with Flow Agent or Video-to-Video

- With Agent on, select/drag the exact clip into the prompt and state one intended change. Example: “Preserve the person, face, raincoat, action, camera, framing, timing, and audio. Change only the background to a snowy winter street; keep the person and parked cars in place.”
- Keep edits narrow and state what stays fixed. Do not ask “make it better.” Change one main dimension at a time, then compare the new version with the original in History/stack.
- Google Help currently describes Gemini Omni Flash video editing: region/model availability applies; upload formats/size, trim limit, and supported segment length are shown in the current Help Center and can change. The desktop guide currently describes uploads up to 60 seconds/1 GB, trimming longer uploads to 30 seconds, and editing a selected segment up to 10 seconds. Verify these live limits before an edit.
- Refinement turns and edits that create media can use credits. Confirm exact cost before approving the edit generation. A multi-video edit is still chargeable generation work; use only if the user approves the scope and cost.
- Edits are saved in the asset stack. Use History to compare versions/prompts and save a past version to the project before placing it into Scenebuilder where needed. Do not overwrite a good take.

### C. Extend a clip only when supported

- Flow Help currently documents Extend for compatible Veo-generated videos; current model support may be narrower than “all Veo.” Confirm the exact clip/model in the live feature list.
- Describe the continuation from the last visible moment, preserve continuity, and identify a clean exit point. Extended clips may not support other edit modes (such as insert/remove/camera) afterward. Check before approving.
- Extending creates more generated media and uses credits: show model, duration, cost, and prompt, then get the explicit clip-specific approval.

### D. Cut/edit decision checklist

- In point begins where useful motion/story starts; out point gives the action room to resolve.
- Dialogue has complete words and natural breath/reaction room; no line is cut at a join.
- Adjacent shots preserve eye-line, screen direction, geography, light, time, weather, and prop ownership where intended.
- Avoid repeated frames, abrupt audio resets, accidental silence, or duplicate speech. Flow may not mix every audio layer; inspect the exported scene and finish complex audio externally if needed.
- Compare alternate Flow edits in History; select only after user review. Record chosen take/version and trim decisions.
- Verify downloaded sequence resolution, aspect, duration, audio and file before reporting export complete.

Official current reference: [Edit videos and build scenes in Google Flow](https://support.google.com/flow/answer/16935718?hl=en). Recheck changing feature limits and model support each project.

## Phase 11 — Editing handoff (when additional finishing is needed)

Prepare a project-specific, copy-ready handoff using actual approved files and trim decisions. If using Codex Desktop, invoke `@Video Editing System` by name; do not claim another app ran it. Include locked story/style, platform/aspect/runtime, clip order, chosen takes, verified source in/out points, dialogue and captions, music/SFX sources, continuity issues, export settings, QA checks, and actual filenames. Mark missing paths/timing as pending, never invent them. Preserve approved story, voices and timing unless a revision is approved. Caption typography/timing is applied in the edit, not generated into images. Only claim files actually rendered and inspected.

After clip completion, ask whether the user wants an editing package/handoff. Phase 11 preparation does not authorize paid Flow generation or publishing.

## Phase 12 — Posting package and performance review

Prepare separate copy-ready packages for standard YouTube, Shorts, TikTok and Reels, recommending destinations that fit the approved export. Include accurate title options, first-second hook, platform description/caption, small relevant hashtag set, search phrases, cover concept/prompt using approved references, cover text/frame suggestion, CTA, engagement question, filename, and upload checklist. Verify current platform requirements when preparing a real upload; cite dated official rules or label them unverified. Include music rights/credits and applicable synthetic-media disclosures. Never publish without explicit user instruction.

Offer two controlled title/hook/cover variants changing one variable at a time and a metrics review template (reach/impressions, CTR where relevant, watch time, retention/completion, rewatches, shares/saves, comments, follows). Compare with the user's actual channel baseline; never invent metrics. For a recurring series, update the bible with approved events, character/voice changes, unresolved threads, locations and props.

## Project-state checkpoint

Use a concise table after each gate:

| Field | Current value |
|---|---|
| Phase / status | [phase; in progress / awaiting approval / complete] |
| Approved concept and version | [title, story, version] |
| Style / camera / lighting / edit | [locked choices] |
| Cast / voices / continuity | [brief locks] |
| Runtime / clips / aspect / platforms | [approved values] |
| Image provider / model / asset status | [ChatGPT or Flow; IDs and approvals] |
| Flow video approvals / credits | [per clip, pending or approved; displayed cost] |
| Edit state | [sequence order, trims, versions, export status] |
| Next action | [one next decision or gate] |

Revisions invalidate only dependent downstream assets. State exactly which prompt, image, clip, trim, or export must be reviewed again.

## Source and maintenance notes

The phases and quality rules are adapted from the user's attached **Universal Viral Video Creator — Version 2.0 Master Prompt**. The editing controls above are cross-checked against Google's current desktop Flow Help. Tutorials and UI labels can age; recheck official Flow documentation, the live model picker, supported modes, and displayed credits on each project.

- [Create videos in Google Flow](https://support.google.com/flow/answer/16353334?hl=en)
- [Use the Google Flow Agent](https://support.google.com/flow/answer/17093911?hl=en)
- [Edit videos and build scenes](https://support.google.com/flow/answer/16935718?hl=en)
- [Manage projects, assets and collections](https://support.google.com/flow/answer/16935308?hl=en)
- [Models and supported features](https://support.google.com/flow/answer/16352836?hl=en)
- [Manage Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- [Download Google Flow data](https://support.google.com/flow/answer/17571126?hl=en)
