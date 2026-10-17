# Universal Viral Video Workflow for Google Flow

Version 1.1 · Based on the user's Universal Viral Video Creator V2 prompt and Google Flow practice

This is the operating playbook for creating short-form stories and videos with Google Flow. It combines the attached 12-phase creator framework with the user's provider choice for still images and a mandatory, per-clip authorization gate for Flow video generation.

## One-word trigger

The user can start this complete workflow in any chat by saying **FlowStart** (case-insensitive). This is a direct command to begin, not a request to explain or acknowledge the trigger. Load the installed Google Flow workflow skill when available, then read this canonical workflow and `system prompt.md` from the active Google-Flow workspace. Resume from saved Project State when present; otherwise begin at Gate 1, using information already in the conversation and not re-asking answered questions. If repository documents are unavailable, use the skill's embedded startup rules and continue. Start recommendations only after current, relevant trend research (see **Research before recommendations** below). Always include **viral micro-drama series** as a story-format choice. FlowStart authorizes planning only; it does not bypass concept approval, image-provider choice, individual video prompt/model/settings/cost approval, editing choices, or publishing authorization. Selecting an image provider authorizes all planned still images in the approved production package; generate and QC them without per-prompt or per-image approval.

**First action for a fresh FlowStart:** Do not send a user-facing question, status, or options before the first in-app browser tool call. Use the ChatGPT/Codex built-in in-app browser to navigate to the Google Flow main page `https://flow.google.com/`, even if an older project is currently open. If using a fresh CUA tool session, make its required first API call `await cua.getState()` and follow the returned instructions. If signed out, pause for sign-in in this same browser. Then click **+ New project**, wait, and verify the new project is open. Only after that may workspace lookup, research, planning, questions, or menus begin. Do not resume an old project unless the user explicitly asks to continue/resume it. Never launch, foreground, or switch to the user's external browser. If in-app browser control is unavailable, explain that this first action could not be completed; do not substitute the first workflow question or use an external browser.

### Keep FlowStart interactive and brief

Aim for **five required decision questions before the first image batch**, never more than **seven** (use a sixth or seventh only if a material ambiguity cannot responsibly be inferred). Track `pre-image decisions: n/5` and the hard ceiling `7` in Project State. Bundle related choices and propose reasonable defaults; do not separately ask the user to approve style, cast appearance, voice, location, dialogue, runtime, shots, aspect ratio, and platform when these can be recommended together. At every answer, immediately advance to the next unfinished gate with easy labeled choices instead of ending on a passive acknowledgement.

Suggested five-gate path; merge or skip a gate if the brief already answers it:

1. Brief, goal, audience, and primary platform(s).
2. Researched creative direction: format/category plus visual style in one menu. Always include viral micro-drama and **Choose for me / Describe my own**.
3. One researched story concept, with compact alternatives and an approve/revise/choose-another gate.
4. One complete production proposal: cast and voices, setting/props, script/dialogue, runtime/shot structure, aspect/platform framing, sound, continuity, and the complete self-checked image-prompt/asset plan. Ask approve, revise, or stop; do not approve routine subfields one by one.
5. Image provider choice. This authorizes the planned image batch; generate and inspect all planned stills, retry clear defects autonomously, then present the batch together for one image selection/lock response.

Do not force all five questions when information is already available. Ask only when missing information materially affects the story, feasibility, safety, cost, or continuity; otherwise state the assumption and move forward. Image selection/revision after the authorized batch is feedback on completed work, not a new pre-generation question. No gate authorizes a Google Flow video generation.

### Research before recommendations

Before making a FlowStart recommendation about trends, format, hooks, genre, platform fit, or audience strategy, browse current evidence. At minimum, check TikTok, YouTube Shorts, and Instagram Reels; include Facebook Reels or any other platform named in the brief. Research the stated niche, audience, language, and geography when known; never assume these. Prefer platform-native trend discovery and official platform trend/culture/creator reports, supplemented by recent reputable cross-platform analysis where it helps compare platforms. Native trend pages may be personalized or region-limited; disclose if they cannot be inspected. Global forecasts do not establish that a particular sound, story, or format is trending among this user's target audience today.

Use dated sources, preferring current-year reports and recent primary evidence for fast-changing claims. Give each recommendation a compact **Research basis** (usually 2–4 bullets): source/platform, publication or checked date, relevant evidence, and how it informed the idea. Link sources in the response and keep a short research log in Project State or the production package. Clearly separate reported evidence from creative inference. Never fabricate metrics, rankings, platform access, or a guarantee of virality. When current primary evidence is unavailable, disclose that and label the suggestion as evergreen craft judgment. Re-check when substantial time has elapsed or the user changes niche/platform.

Research cultural/regional story traditions separately using credible culture-specific, academic, or industry sources. Treat a tradition as a researched creative influence, not a claim that a whole culture tells stories one way. Avoid stereotypes and generic cultural mashups.

## Non-negotiable operating rules

- Never assume country, culture, language, accent, identity, audience, or nationality. Use the user's choices and story context.
- Use **Guided Mode** by default. Do not ask the user to choose a mode. Bundle related creative fields into a small number of decisions, following the five-gate target and seven-gate ceiling above. For each gate, state a concise recommendation and research basis where relevant, then provide keyboard-friendly choices. Do not require the user to copy prompts or compose prose to proceed.
- At every meaningful decision or gate, include **Choose for me** and **Describe my own** where applicable. Keep these as concise options, such as `Y — Choose for me` and `Z — Describe my own`. For approval gates, always provide explicit, easy choices such as `1 — APPROVE`, `2 — REVISE`, `3 — STOP`; never rely on a free-text approval phrase alone. Approval must be explicit and gate-specific.
- Always mark one available choice **Recommended** and give a short reason. The user may choose any other option. At approval gates, recommend the safe/next-step choice only when appropriate; never preselect approval or imply that the user has approved.
- Do not arbitrarily reduce a phase's meaningful menu to three choices. Show the full practical menu when it has up to seven or eight options, including browse/search/custom/choose-for-me routes where relevant. Group large catalogs by category and ask the user to pick a category before presenting a long list. Reserve a short three-choice menu for binary approval/revision/stop gates, not for open-ended creative selection.
- Prefer actual clickable choice controls when the interface supports them. In plain chat, use clear keyboard-friendly labels: one option per line, letter or number first, short action label next. Explain that the user can reply with only the letter/number. Avoid burying choices in paragraphs.
- Keep the phases in order. Stop at each explicit gate; silence, a prior approval for a different asset, or an instruction to prepare a package is not approval for the next paid generation.
- **Images:** ask once for **ChatGPT Images** or **Google Flow Images**. That provider choice authorizes all planned still-image prompts in the approved production package; do not ask for another batch-size, per-prompt, or per-image approval. Default 9:16 portrait and one output per distinct prompt; submit the planned prompt set together when supported. Use Nano Banana 2.1 when available for Flow. Inspect outputs and autonomously retry clear defects within the planned set, then present the completed set for one selection/lock decision. Report costs transparently without making image generation approval-gated. Do not expand beyond the planned package unless asked.
- **Videos:** Google Flow is the rendering tool. Never start, queue, or acknowledge a Flow video generation until the user has explicitly approved that exact clip's prompt, model, mode, orientation, duration, output count, and displayed credit cost. Ask again for each clip, because each can spend credits. One clip per approval by default. Do not use any setting that disables confirmation. If user authorization is unclear, stop before Generate.
- Distinguish idea/prompt planning, saved files, uploaded files, generated results, reviewed results, user approval, and audience performance. Claim only what has visible or file-based evidence.
- Keep generated content original. Explain named studio/creator styles through concrete traits; do not imitate a living creator's exact style. Never promise virality or fabricate trend metrics.
- Preserve originals and edit history. Before deletion, trashing, public sharing, or replacing user assets, identify the target and obtain approval.
- Maintain a compact **Project State** after decisions: current phase and pre-image decision count (n/5; hard ceiling 7); research note with sources/dates/limits; approved concept/version; style; story; cast/voices; runtime and shot count; aspect/platform; chosen image provider; approved images; video prompt/model/settings/cost/approval per clip; current Flow edit state; manifest; next action.

## Workflow map

![Workflow from creative brief through approved images, individually authorized Flow clips, editing, and posting package](assets/google-flow-viral-workflow.svg)

The twelve production phases below are a completeness checklist, not twelve separate user interviews. For FlowStart, merge Phase 1 with Phase 2 under Decision Gate 2; merge Phases 3–6 into the single complete-proposal decision; use Phase 7 for the story approval in Gate 3; prepare Phase 8 as part of the Gate 4 package; then ask once for image-provider choice in Gate 5. Do not duplicate an approval already given at its designated gate.

## Local project folder and chat continuity

Immediately after the user agrees to the story and working title, create a matching project subfolder under the active Google-Flow workspace, before generating project assets. Use subfolders for references, story/prompts, Flow downloads, captions/audio, editable HyperFrames files, and final exports. Store a short README, current Project State, research/continuity notes, and approved prompts there. Reuse the same workspace/project folder when the user resumes in a new chat; do not duplicate the folder. Record the exact local path in Project State. Keep private references and generated media local; publish reusable workflow documentation only unless the user explicitly asks to publish project media.

## Phase 1 — Research, then choose creative direction

Perform relevant platform trend research before the first recommendation. Bundle visual style and story format in one choice when feasible; include the full practical menu, viral micro-drama, a marked recommendation, and choose-for-me/own-idea paths. Carry forward any style or format the user already specified.

If the user wants to browse visual styles, use this reference menu; do not make selecting from the catalog a separate required turn when style and format can be decided together.

Give one clear recommendation and invite a choice:

1. **Recommended:** accept the recommended style
2. See three alternatives with a short example concept for each
3. Browse the Featured 10 styles
4. Browse the full style library by category
5. Search for a style, mood, or topic
6. Describe a custom look
7. Choose for me

Featured codes: F1 3D Claymation; F2 Ghibli-inspired hand-painted 2D; F3 Cinematic; F4 Selfie UGC; F5 Italian Brainrot surreal; F6 Pixar-inspired family 3D; F7 AI Talking Objects; F8 Music Video; F9 Cyberpunk; F10 Documentary. The complete 243-entry catalog is in [STYLE LIBRARY.md](STYLE%20LIBRARY.md). Preserve F/L catalog codes. Offer useful category subsets instead of dumping all entries.

Record separate controls for main medium/render style, camera language, lighting/mood, and editing treatment.

## Phase 2 — Story category and original concept

Recommend one style-compatible category and why. Include **viral micro-drama series** in the story-format menu every time: serialized short episodes with recurring characters, escalating reveals, and a cliffhanger/payoff pattern. It is a choice, never a forced format. This menu is part of Gate 2; do not ask a separate question after style selection. For Gate 3, recommend an original title, premise, and immediate visual hook alongside compact alternatives. Offer accept, revise, another idea, or choose for me. When the user chooses viral micro-drama, use the streamlined researched pitch below instead of a long idea-scoring exercise. Do not require ten-item scoring unless the user asks for it.

Story category candidates (not a certified ranking): micro-drama/cliffhanger; emotional twist; relatable POV/UGC; surreal meme; talking objects; mini-documentary; history/mystery; science/what-if; responsible true crime; internet lore; gaming; fantasy; fictional animal story; craft/stop-motion; ASMR/restoration; transformation; behind-the-scenes; challenge; music-synced story; food; travel/culture; relationships/redemption; sci-fi; action/suspense; analog horror; parody; interactive mystery; product story; educational skill; trend explainer; cozy nostalgia; fashion/design; sports underdog; recurring character lore; impossible visual spectacle; or a custom category.

### Viral micro-drama recommendation (use when selected)

When the user chooses viral micro-drama (or says “micro-drama”), do targeted web research for a suitable dramatic tradition/region before recommending the story. Prefer reliable cultural, academic, and industry sources; cite sources near claims. Distinguish documented convention from creative inference, avoid stereotypes and generic cultural mashups, and never claim that any concept is guaranteed viral. If the user does not specify a setting, recommend one fitting tradition/region and give one short reason; do not ask a chain of setup questions or run lengthy mandatory scorecards.

Present one original working title and a compact pitch that covers: heroine/protagonist; goal; opposition; secret; stakes; love and betrayal; sweet romance; powerful family; revenge; love-after-marriage; and an immediate visual hook. Weave these ingredients into one coherent premise rather than a disconnected checklist. If a trope would make this specific story confusing or implausible, say briefly how it is being adapted; do not let trope density damage the central goal and cliffhanger.

Offer compact region/language alternatives as part of the same Gate 3 story menu, with one clearly marked recommendation and short rationale: **South Korean**, **Japanese**, **Chinese**, **English-language**, **American**, **British**, **Nigerian**, **Other (suggest a tradition/region)**, and **Another story in the recommended type**. Explain that a one-number reply selects the direction. Bundle region alternatives with story alternatives; do not ask a region question followed by a second story approval question. Include `1 Approve recommendation`, `2 Revise`, `3 Choose another region/story`, and `4 Give me another story in the recommended type`. Keep this gate separate from paid video approvals.

Score concepts as editorial judgment (not observed audience performance): visual appeal, curiosity, emotion, originality, clarity, feasibility, and platform fit. Include a retention arc: immediate hook, setup, escalation, payoff, and ending/loop. Use meaningful developments if repetition risks attention; do not force a mechanical interval. For current trend claims, cite dated platform evidence and distinguish evidence from creative prediction; trends inform the recommendation but do not predict success.

## Phase 3 — Cast, voice design, and continuity

For the single complete production proposal (Gate 4), recommend 1–3 main characters and state the assumption; do not ask a separate cast-count question. Determine audience age context and whether cast includes people, animals/fantasy beings, talking objects, custom cast, or none. Every character who speaks must receive a voice lock and a reusable Flow Character voice during character setup; voice creation is part of completing the character, not a later optional enhancement. Mark non-speaking characters as voice not applicable. A multi-character story must give characters meaningful interaction.

For each character, make one complete creative recommendation at once instead of asking a string of appearance and voice questions. Include name, role, age range where relevant, face/hair, build, wardrobe/accessories, behavior/personality, handedness if it affects action, and (if speaking) a complete voice proposal: voice name, suitable Flow preset, language/accent/pronunciation, register/pitch, texture, pace/articulation, baseline delivery, emotional range, signature behavior, and avoidances. Add one short representative sample line in character. The user can approve the complete proposal or request a focused revision. Do not require separate approval for routine subchoices such as voice name or sample wording.

Track names, age range where relevant, face/hair, body/build, wardrobe/accessories, handedness, relative scale, voice/language/accent/pronunciation, delivery and emotional range, prop ownership/position, location geography, lighting direction, time/weather, and intentional state changes. Do not infer nationality from language or appearance. Do not infer accent, personality, or pitch from visual appearance or stereotypes. If a specific real person must be depicted, use an appropriate authorized reference; text alone cannot reproduce identity reliably.

### Required Flow Character and voice setup

After the complete cast proposal is approved, create each needed character in the project's **Characters** area. Use an approved project image or create a clean portrait/reference; add the character's appearance, name, and behavior/personality description. For every speaking character, complete this voice sequence before marking character setup done:

1. Open **Select a voice** and choose the closest preset based on the planned performance, not just a generic gender/pitch label.
2. To customize, give the voice a clear character-specific name (for example, `Maya — Calm Suspense`). Enter the approved short sample dialogue, attributed to the character, and describe language/accent/pronunciation, register, timbre/texture, pace, articulation, breath, baseline delivery, emotional range, scene-appropriate shifts, and what to avoid. Keep stable identity separate from temporary emotion in a particular shot.
3. Preview the sample. Google's Help describes this as an optional 8-second custom-voice sample; labels may read **Preview** or **Play preview** in the live Character UI. Confirm preview generation finishes; evaluate intelligibility, natural pacing, pronunciation/accent, fit to character, and distinction from other voices when audio is actually accessible. Do not claim to have heard/evaluated audio if it is not audible to the operator.
4. Follow any current **Sync** step, save the custom voice, then explicitly **Add to character**. Google's documented custom-voice route is prompt box → model **Omni Flash** → **Add → Voices → Create New Voice** → base voice → name → Voice Performance → optional Sample Dialogue → Sync → Save New Voice. The Character sheet also offers voice selection/creation in supported UI. Labels and flow can vary by rollout; use the live controls.
5. Verify the character sheet displays the correct saved voice and that appearance/personality, sample, and performance notes agree with the character bible; then save/finish the character. A saved custom voice is not complete until attached to the intended character.

Maintain a voice-bible record per speaker: `Character | Flow voice name and preset | language/accent | register and texture | pace/articulation | baseline delivery | emotional range | sample dialogue | pronunciation notes | preview status | attached/verified`. For video prompts, identify the speaker and exact words, preserve the character's stable saved voice, and specify only the scene-specific performance (e.g., a restrained whisper or a frightened pause).

**Voice-reference constraint:** Google's current Help documents voice references for **Omni Flash + Video Ingredients**. Add them with **Add → Voices**, then refer to the selected voice with `@Voice` (Google shows the form `@Voice: Andrew`). It describes this as a single-speaker voice reference and warns that voice references used outside video generations with Ingredients can error. Do not assume the voice attached to a Character is injected automatically in every model/mode; attach the explicit voice reference where the live supported workflow requires it. Check the live picker for changes before each project. This guidance does not bypass the per-clip video approval gate.

## Phase 4 — Runtime, scenes, clips, and timing

Include recommended runtime, scene count, and clip count in the Gate 4 proposal. The user can revise them with the whole proposal; do not ask a separate runtime question. Distinguish narrative scenes, generated clips, and storyboard boundary images. Give every clip exact start, target end, and duration; timeline arithmetic must equal locked runtime, accounting for approved title cards and transition overlaps. Use only durations supported by the selected Flow model.

For N continuous clips plan N+1 boundary stills: Clip i targets SHOT_i → SHOT_(i+1). Eight clips need SHOT_01–SHOT_09, with SHOT_09 as the terminal endpoint, plus any separate character/location/prop references. Check that every adjacent composition can connect with plausible motion before image production.

## Phase 5 — Dialogue and sound

Include the recommended speech/audio treatment and exact dialogue in the Gate 4 proposal. Offer a compact alternate treatment inside that bundled choice only if materially useful; do not ask a separate audio question. Attribute every line to a named speaker. Use one unambiguous speaker at a time unless overlap is approved; non-speaking visible characters react silently. Record exact words, delivery, voice lock, and dialogue window per clip. Audit word count, plausible speaking pace, pauses, reaction allowance, and lip-sync. Shorten or redistribute lines during planning, then obtain approval for any changed dialogue/timing. Specify ambience, SFX, music, and ducking where relevant.

## Phase 6 — Aspect ratio and platforms

Include the recommended aspect ratio and platform framing in the Gate 4 proposal (default 9:16 for TikTok, Shorts, and Reels; 16:9 for standard/cinematic YouTube; square when appropriate). Do not ask separate ratio and platform questions if the brief identifies them. Keep images, clips, cover/title assets, captions, and exports consistent. Keep faces and critical text in practical safe areas; verify current platform requirements before publishing. Separate aspect-ratio variants require their own plan and approval.

## Phase 7 — Concept approval gate

This is Gate 3's story approval, not an additional question after the micro-drama or story menu. Present the selected/recommended story's title, hook, arc, payoff, and evidence basis. Gate 4 will bundle the remaining complete production proposal and its approve/revise choice. Do not ask the same concept approval again in Phase 7.

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

### Serialized micro-drama episode deliverable

When the chosen category is a serialized micro-drama, organize each episode's production package into these six user-readable parts. Recommend 30 seconds per episode unless the user chooses another duration. For a 30-second cliffhanger episode, target the reveal at 0:28–0:30. Do not promise exact millisecond control from generative video—use the timeline, generated clip endpoints, and edit trims as targets, then verify the actual cut.

1. **Episode logline and cliffhanger:** episode number/title, one-sentence logline, concise runtime-matched narrative summary, and the exact final reveal/image/action/dialogue beat that creates a reason to watch the next episode. Avoid claiming guaranteed virality.
2. **Character reference sheets:** create a clean visual reference for new characters, then save them in Google Flow's Characters area with appearance/personality and a designed voice when speaking. For returning characters, specify `REUSE FLOW CHARACTER [Name] — first established Episode [X]`; don't make duplicate sheets without a reason. Use Flow-native references and supported modes rather than OpenArt-specific prompt tokens.
3. **Location, environment, and prop references:** define each new location with a clean scene plate and key geography, light, and set dressing; define critical props and orientation. For returning sets/props, reuse the saved Flow asset or an approved previous frame as an Ingredient/Frame when the selected mode supports it. Keep character identity separate from location plates when that improves control.
4. **Episode script and dialogue:** write a runtime-matched sequence of concise beats/lines in the approved language. Attribute every spoken line; keep speaker, word count, pauses, reaction time, and lip-sync realistic. Voice description remains aligned to the attached saved Character voice.
5. **Google Flow shot/clip prompts:** divide the episode into a small number of sequential Flow clips (often 3–4 for a 30-second rough cut, adjusted to supported per-clip lengths). For each: shot number and intended timeline window; story purpose; actual approved character/location/prop reference inputs; one principal action; framing and a coherent camera move; lighting/atmosphere; exact dialogue and audio/SFX cues; continuity constraints; target in/out pose or start/end frame; model/mode/aspect/duration/output count; live displayed cost; acceptance checks. Do not submit a multishot prompt written for Seedance as if Flow had the same timeline renderer. Assemble separate Flow clips in Scenebuilder, verify actual combined duration, and trim at natural action/speech points.
6. **Continuity snapshot for the next episode:** capture the actual ending state after editing: final visible character positions/expressions, wardrobe, props and their orientation/ownership, exact location geography, time/light/weather, emotional state, plot facts revealed, unresolved question, final line/sound, and the selected ending frame/video endpoint asset ID. This is a concrete continuation target, not a claim of millisecond-exact control.

The six-part layout is a story-planning template, not extra approval gates. Keep the global gates: approve the concept; choose the image provider once and let the planned still-image batch run with agent QC/retries; approve each individual paid Flow video generation with its exact prompt/settings/live cost; review the edited episode before locking it.

## Phase 9 — Image provider choice, generation, and asset approval

### 9A. Choose the image tool and authorize the batch

Ask once: **“Which should we use for the images: ChatGPT Images or Google Flow Images?”** Give a concise recommendation with reason, trade-off, and alternative. Choosing the provider authorizes the planned image batch in the production package; do not ask for separate batch-size, per-prompt, or per-image approval. Submit all planned image prompts together when supported. For Flow, inspect the live output count, aspect ratio, model (prefer Nano Banana 2.1 when available), and any displayed cost; use one output per distinct prompt by default. Report cost transparently but do not block the image batch for another approval. Do not expand beyond the planned package. Keep video generation behind its separate explicit approval gate.

### 9B. Generate and review

Inventory supplied references and missing assets. Generate character references first, then needed location/prop references, then storyboard images in order. Keep reference sheets separate from story frames. Default 9:16, one output per prompt. For every asset, identify its ID, saved project name, shot/role, visible characters, reference inputs, aspect ratio, provider/model, and exact approved prompt. Before a generation where identity or setting continuity matters, attach the approved Flow Character, location, prop, or image as a prompt ingredient when the selected mode supports it. On desktop, use the current UI's **Add ingredients** control, drag a project/device asset into the prompt box, or use the media menu's **Add to Prompt** path. Search saved assets by `@name` where supported; use `@CharacterName` for a Flow Character. Explain each reference's role in the prompt and verify the correct thumbnail/asset is attached. Treat asset IDs as ledger traceability, not prompt syntax unless Flow explicitly supports ID entry. If attachment is unsupported for the selected mode, state that and use supported references instead of implying that a textual name alone conditions the generation. After generation, inspect face/anatomy, composition, identity, wardrobe, prop positions, geography, lighting, style, and compatibility with neighboring frames.

Once the user selects the provider, generate the planned image prompt set without asking for extra scope or per-image approval. Inspect every result at a size that makes important details readable for prompt match, reference/character/location/prop continuity, plausible anatomy and object geometry, composition, aspect ratio, and neighboring-frame compatibility. **Check physical and visual logic, not just whether the image looks attractive:** hands must hold objects plausibly; object parts and reflections must agree with camera angle; screens must be on device glass facing the viewer; a phone's rear casing/back-camera side must never display screen UI; avoid impossible duplicate props, floating displays, reversed controls, fused fingers, inconsistent shadows, or unexplained changes in wardrobe/identity/location. Keep small device text abstract or unreadable unless exact text is essential. Compare each still with its exact prompt and approved reference sheets. Automatically retry a clearly defective still with a targeted prompt that changes only the failed dimension; keep useful versions and report the defect and what was regenerated. Reinspect the replacement at full size and do not accept it until it passes the same checks. After the full batch and QC, present the results together for one selection/lock decision before they are used as approved downstream references. A user can ask to stop or revise at any point. Preserve actual source file type and resolution; never claim the proposed filename exists until verified.

### 9C. Import external ChatGPT Images into Flow when needed

Use the generated tool's saved local path. In the ChatGPT/Codex built-in in-app browser, open the current project's Flow workspace and add the asset through **Add media (+) → Upload** or the prompt's add-ingredient control. Wait for processing and verify it appears in the project's Uploads/Images area. Explicitly tell Flow whether it represents identity, location, product, style, or composition. Do not trigger an additional Flow generation just to upload. A literal drag from the chat image panel may be unsupported; use the upload picker and accurately describe the method used.

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

## Phase 11 — Video downloads, editing, and finishing

Phase 11 begins only after Phase 10's planned video clips have been generated, inspected, and approved. First download **all approved video clips** from Flow into the active project's `03 - Google Flow Downloads` folder (plus the approved Scenebuilder sequence if one exists); verify every file and record its filename. Then continue in this same project chat and begin the edit. Do not begin the HyperFrames edit while approved source clips are still missing from the workspace. Use the available HyperFrames skill/plugin for the edit, with editable materials in `05 - HyperFrames Working Files` and verified final renders in `06 - Final Exports`.

Flow Scenebuilder's basic assembly can be part of Phase 11. Use HyperFrames for finishing beyond Flow's current sequencing/trimming controls, such as timed captions, precise audio, titles, grading, or frame-accurate work. Preserve all source clips. Any new Flow AI edit, extension, or video generation during Phase 11 remains chargeable generation work and requires its own explicit approval under Phase 10. Preparing or rendering an edit does not authorize publishing.

### A. Assemble the Flow rough cut

Use Flow's editor for shot selection, simple sequence assembly, trims, and supported AI-assisted clip changes. Work from copies/versions; Flow's History/asset stack preserves original and edited versions. Confirm every AI edit that triggers generation under the same per-action approval gate above.

### A. Make a clean rough cut in Scenebuilder

1. In the Flow project, select the accepted clips. Use each clip's **More → Add to Scene** (label may vary) or open **Scenes** and create a new scene.
2. Add clips in story order. Drag tiles along the timeline to reorder. Confirm order against the approved shot list before refining.
3. Use each clip's in/out handles to trim its beginning or end. Remove dead air, accidental pre-action, unneeded trailing frames, and awkward cut points while preserving the story beat, approved dialogue, and needed motion.
4. Preview the full sequence after each group of trims. Watch cut points at normal speed; when a join feels wrong, replay around the join and choose a better in/out point. Avoid cutting off a word, gesture, impact, or reaction.
5. Check sequence duration against the approved target. Scenebuilder supports sequencing/reordering/trimming/preview/download; do not assume it provides every nonlinear editing function (multiple precision audio tracks, advanced transitions, captions, keyframes, color grading, or frame-accurate automation).
6. Download the scene when the cut is ready. If further finishing is needed, use a dedicated editor with the approved export and project handoff.
7. Download approved source clips as well as the assembled scene into the project's Flow-downloads folder. Verify each saved file and retain originals.

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

### E. HyperFrames editing handoff and delivery

Prepare the edit from the verified files already downloaded to the project folder. Continue in the same chat and invoke the available HyperFrames skill/plugin; do not start a new chat for the same production or imply the skill has run before it has. Put editable composition/project files under `05 - HyperFrames Working Files` and verified renders under `06 - Final Exports`. Include locked story/style, platform/aspect/runtime, clip order, chosen takes, verified source in/out points, dialogue and captions, music/SFX sources, continuity issues, export settings, QA checks, and actual filenames. Mark missing paths/timing as pending, never invent them. Preserve approved story, voices and timing unless a revision is approved. Caption typography/timing is applied in the edit, not generated into images. Add and time captions after the cut/dialogue is locked, inspect mobile-safe placement, and provide `.srt` plus styled `.ass` where supported. Treat supplied prompts as references: use applicable editing guidance, not unrelated example content or conflicting sample runtimes/aspect labels. Only claim files actually rendered and inspected.

Do not add another planning gate between approved Flow downloads and editing. When the user directs the workflow to continue and all approved clips are downloaded and verified, start Phase 11. Phase 11 preparation/rendering does not authorize new paid Flow generations or publishing.

## Phase 12 — Posting package and performance review

Create the Phase 12 package as a polished native Google Doc, not a Markdown file. Use the project's title and Phase 12 in the Doc title; include a clear title/subtitle, professional heading hierarchy, readable spacing, bold field labels, linked platform sources, and concise copy-ready sections. Open the verified Google Docs URL in the in-app browser when available, and record that URL in the project's README/Project State. Avoid Markdown asterisk decoration or visible Markdown syntax.

Make every platform packet independently usable without another research/planning round. For each destination, state the recommended use and why; supply a recommended title/caption plus meaningful alternatives and selection guidance; provide copy-ready description, a small relevant hashtag set, natural search phrases, first-second hook, cover text and approved-frame direction, pinned comment, CTA, caption/accessibility notes, platform-specific upload fields, AI disclosure and music-rights checks, and a destination-specific preflight checklist. Distinguish standard YouTube from Shorts and explain when the approved export requires a separate aspect-ratio edit. Add an order-of-operations checklist for cross-posting and a lightweight per-platform metrics template. Before recommending a trending sound, hashtag, upload time, or current trend format, research fresh platform-native signals for the target niche and region, cite source/date, and distinguish forecasts or aggregate statistics from a current trend. If live native trend pages or account analytics are inaccessible, disclose the limit and use evergreen story craft instead. Do not repeat a generic caption across services or invent controls, account settings, trends, file facts, or performance data. Verify current platform requirements before real publication and cite dated official rules or label them unverified. Mark export-dependent information pending rather than guessing; revise the Doc after Phase 11 creates the final export. Never publish without explicit user instruction.

Offer two controlled title/hook/cover variants changing one variable at a time and a metrics review template (reach/impressions, CTR where relevant, watch time, retention/completion, rewatches, shares/saves, comments, follows). Compare with the user's actual channel baseline; never invent metrics. For a recurring series, update the bible with approved events, character/voice changes, unresolved threads, locations and props.

## Project-state checkpoint

Use a concise table after each gate:

| Field | Current value |
|---|---|
| Phase / status / question count | [phase; in progress / awaiting approval / complete; pre-image n/5, hard ceiling 7] |
| Trend research | [sources, dates, key evidence, scope/region limits] |
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

### Short-form trend research baseline (checked 2026-10-16)

These are broad platform signals to seed research, not a real-time trending list. On every FlowStart, check for newer reports and native trend signals in the actual niche, audience, and geography; distinguish platform-reported evidence from creative inference.

- [TikTok Next 2026](https://newsroom.tiktok.com/introducing-tiktok-next-2026-our-trend-forecast-for-marketers-for-the-year-ahead?_hsmi=399120832&lang=en) (Jan. 14, 2026) is TikTok's annual forecast and emphasizes active discovery, curiosity, community, and audience value. Treat a forecast as directional, not proof a format is currently trending for this user's target.
- [Made On YouTube: Shorts Series and microdramas](https://blog.youtube/news-and-events/made-on-youtube-creators-shorts-series-tv-features/) (Sept. 23, 2026) reports 6.5 billion YouTube microdrama views in H1 2026 and over 50% watch-time growth year over year; YouTube also introduced Shorts seasons/episodes. This supports testing serialized storytelling on YouTube, not promising results for a particular series.
- [Meta's 2026 update](https://about.fb.com/news/2026/01/2026-ai-drives-performance/) (Jan. 28, 2026) states that 75% of Instagram recommendations in the US in Q4 2025 came from original posts. Keep the US scope and Q4 period visible when using this signal.
- [Metricool's 2026 short-form report](https://metricool.com/short-video-report/) (Aug. 26, 2026) describes analysis of over 6.1 million videos across Instagram, TikTok, and YouTube. Use its platform comparisons as third-party evidence, not an individual-account forecast.

- [Google Flow Operations Field Guide](GOOGLE%20FLOW%20OPERATIONS%20FIELD%20GUIDE.md) — operational reference for settings layers, models, credits, references, edits, privacy, exports, troubleshooting, and current help links.
- [Create videos in Google Flow](https://support.google.com/flow/answer/16353334?hl=en)
- [Google Flow Character and Voice Guide](GOOGLE%20FLOW%20CHARACTER%20AND%20VOICE%20GUIDE.md)
- [Official Flow character management](https://support.google.com/flow/answer/16935308?hl=en)
- [Official Flow custom voice and voice-reference instructions](https://support.google.com/flow/answer/16353334?hl=en)
- [Use the Google Flow Agent](https://support.google.com/flow/answer/17093911?hl=en)
- [Edit videos and build scenes](https://support.google.com/flow/answer/16935718?hl=en)
- [Manage projects, assets and collections](https://support.google.com/flow/answer/16935308?hl=en)
- [Models and supported features](https://support.google.com/flow/answer/16352836?hl=en)
- [Manage Flow credits](https://support.google.com/flow/answer/16526234?hl=en)
- [Download Google Flow data](https://support.google.com/flow/answer/17571126?hl=en)
