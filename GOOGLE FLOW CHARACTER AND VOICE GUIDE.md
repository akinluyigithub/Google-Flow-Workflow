# Google Flow Character and Voice Guide

Practical, beginner-friendly instructions for building reusable characters and assigning repeatable voices in Google Flow. Interface names, model support, and rollout availability can change; follow the live project UI and recheck the official references linked below.

## What a Flow Character stores

Before review or reuse, label each character reference image `REF 01 — Character name` (with a distinguishing description/version as needed) and verify the saved Flow title. Keep the same identifier in the character bible, asset ledger, prompt inputs, and downloaded filename. The Character and saved voice retain recognizable character names. Follow [Asset Naming and Review Guide](ASSET%20NAMING%20AND%20REVIEW%20GUIDE.md).

Google Flow lets a project character bundle visual and audio references for reuse. Google's current Help says a character needs at least one appearance image, and the creation flow accepts one or two. The character can be mentioned in a prompt by typing `@` followed by its name. References help carry identity across shots, but every result still needs continuity review.

## Create a character in a project

**Mandatory Phase 9 gate:** complete and verify these saved Character/voice records for every speaking character after its approved reference image exists and before any video is prepared. Add the approved image from the project rather than generating a replacement. The local cast/voice bible alone is insufficient. The user's selected video family is **Omni 1.1 Flash**; do not substitute Veo without explicit direction. In character clips, attach the actual saved Character plus its saved voice where Omni Ingredients requires it, and verify both inputs before the clip approval request.

1. Open the intended Flow project.
2. In the left navigation, open **Characters**. Select **New Character** if available.
3. Describe the character in concrete visual terms: age range if relevant, face, hair, build, wardrobe, distinctive features, and visual style. Add stable personality/behavior notes separately in character info.
4. Upload or generate one or two clear appearance images. Use a clean, unambiguous image that shows the intended identity. At least one image is required before the character can be used.
5. Generate the character image(s), review them for identity and anatomy, and keep the correct reference.
6. Give the character a stable, recognizable name.
7. Select a voice if this character speaks. For a speaking story character, our workflow always creates and attaches a suitable voice. Mark a genuinely non-speaking character as voice not applicable.
8. Add concise character info for personality, behavior, and continuity. Keep this distinct from the visual description and from voice performance notes.
9. Click **Done** and verify the character appears in the project's Characters area.

To edit later, open the project, go to **Characters**, select the character, change details, and click **Done**. Do not delete a useful character merely to revise it; edit it where possible and preserve approved references.

## Design a voice before opening the picker

Write one complete voice recommendation for each speaking character so the user can approve or revise the whole proposal at once. Record:

- Voice name and best-matching base preset.
- Language and accent/pronunciation (only when specified or intentionally chosen; never infer it from appearance or nationality stereotypes).
- Register/pitch and vocal texture.
- Pace, articulation, breath, and baseline delivery.
- Emotional range and how it shifts under pressure.
- A short sample line that sounds like something this character would actually say.
- Anything to avoid (for example, exaggerated acting, a broad accent, or overly polished narration).

Keep stable identity (“calm, intimate mid-range voice; measured pace”) separate from a scene's temporary direction (“whispers as she listens at the door”).

## Assign and customize a voice

1. In the character sheet, click **Select a voice**.
2. Choose a preset based on the approved voice plan. Review its preview/description; do not choose based only on its label.
3. If customizing, set a distinctive character-specific name.
4. Enter a short representative sample dialogue line, attributed to the character. A preview sample is optional in Google's Help, but our workflow uses one whenever supported to assess the design.
5. Write performance instructions for the audible qualities: texture, register, accent/pronunciation, pace, articulation, breath, baseline emotion, and restrained scene-relevant variation.
6. Preview the custom voice. Google Help describes an optional 8-second sample; current UI may expose **Preview**, **Play preview**, or a similar control. Wait for the preview to finish. Revise the preset, sample, or performance notes if it is unsuitable.
7. Save the custom voice (**Save New Voice** or equivalent), then explicitly choose **Add to character**.
8. Verify the character sheet displays the intended voice and description. Confirm the character name, personality info, sample, and voice notes all align; then click **Done**.

If the UI has a **Sync** step between preview and save, complete it first. Do not assume that saving a custom voice attaches it automatically: confirm the separate **Add to character** step. Button labels and the order of steps may vary across product rollouts.

### Voice preview quality check

When audio is actually accessible, listen for intelligibility, naturalness, pacing, pronunciation, emotional fit, and clear distinction from other characters. If the interface reports a preview is playing but the operator cannot hear audio, report only that preview generation/playback was triggered; do not claim a listening assessment.

Suggested voice record:

| Field | Record |
|---|---|
| Character / Flow character name | |
| Voice name / base preset | |
| Language / accent / pronunciation | |
| Register / texture | |
| Pace / articulation / breath | |
| Baseline delivery / emotional range | |
| Sample dialogue | |
| Preview result / notes | |
| Saved / added to character / verified | |

## Use the character and voice in video prompts

### Character visual/personality reference

Type `@CharacterName` in the project's prompt box and describe the intended role/action for the reference (for example, `@Maya listens at the apartment door; preserve her face, charcoal sweater, and eyebrow scar`).

### Voice reference: model/mode limitation

Google's current video Help documents voice references for **Omni Flash** video generations using **Ingredients**:

1. Select the **Omni Flash** model.
2. Select **Video → Ingredients**.
3. Under the prompt, choose **Add → Voices** and choose the saved voice. The UI may allow a short preview of a preset voice.
4. Reference it in the prompt as `@Voice` (Google's example format is `@Voice: Andrew`).
5. Use one speaker voice reference for a single-speaker clip and state the exact dialogue and scene-specific delivery.

Google states voice references are only available for video generations that use Ingredients; using them in other generation types can produce an error. Verify current model/mode support before preparing the clip. Do not assume that a Character sheet's saved voice is automatically injected into every model/mode: where the supported workflow requires it, add the voice reference explicitly.

Video generation remains subject to the workflow's per-clip approval gate, including prompt, model/mode, settings, and displayed cost. Creating or previewing a voice does not authorize rendering a video.

## Sources

- [Manage your Google Flow projects, assets & collections — Create & manage characters](https://support.google.com/flow/answer/16935308?hl=en)
- [Create videos in Google Flow — Add voice references and create custom voices](https://support.google.com/flow/answer/16353334?hl=en)

Checked against Google Flow Help on 2026-10-16. Recheck the live UI and Help Center for changed labels, availability, and model compatibility.
