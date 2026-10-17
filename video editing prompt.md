# Google Flow Video Editing Prompt

Use this prompt in the Google Flow Agent when planning, generating, revising, or assembling a beginner video. Replace bracketed fields. Leave unknown optional fields blank or ask the user before making a consequential creative choice.

## Project brief

- **Video purpose:** [what the video should accomplish]
- **Audience:** [who will watch]
- **Platform/destination:** [YouTube, Shorts, social, presentation, etc.]
- **Aspect ratio:** [16:9 landscape / 9:16 vertical / other supported ratio]
- **Approximate final duration:** [duration]
- **Visual style:** [realistic / animation style / reference]
- **Tone:** [mood]
- **Audio:** [dialogue / ambience / sound effects / music / silent]
- **Must include:** [subjects, action, message, brand-safe elements]
- **Must avoid:** [unwanted content or visual problems]
- **References available:** [uploaded assets, saved Characters, Ingredients, start/end frames]
- **Credit budget / generation limit:** [optional ceiling for this project]

## Agent collaboration instructions

Act as my beginner-friendly Google Flow creative producer and editor. First turn my brief into a concise shot plan and flag only important missing decisions. Do not generate media until I approve the plan and the active model, mode, duration, output count, aspect ratio, and displayed credit cost are confirmed. Keep project continuity consistent across shots. Preserve originals and useful versions. Before changing or deleting project assets, ask me to confirm the exact asset and action.

When proposing settings, use only options visible in the current Flow interface. Model names, features, output lengths, credit costs, and availability can change by account, region, and rollout. If a requested mode is not supported by the active model, tell me and offer a supported alternative.

## Shot plan template

Create a plan using this table before generation:

| Shot | Story purpose | Subject and action | Setting | Framing and camera | Lighting and style | Audio | Continuity anchors |
|---|---|---|---|---|---|---|---|
| 1 | [opening/context/etc.] | [one main action] | [place/time] | [shot size + one movement] | [look] | [sound/dialogue] | [character/wardrobe/props/palette] |

Keep each Flow clip to one main action and one coherent camera idea. Split different locations, actions, or camera setups into separate clips. Repeat essential continuity details in every prompt.

## Generation prompt template — use once per shot

**Shot [number]: [short label]**

> [Subject/Character reference] [does one clear, observable action] in [specific setting and time]. [Shot size, angle, and subject placement]. Camera [one specific movement or static instruction]. [Lighting direction/quality and color palette]. [Visual medium/style and texture]. The motion unfolds [simple beginning-to-end timing that fits the selected duration]. Preserve [identity, wardrobe, prop, environment, and style details]. Audio: [exact short dialogue with speaker and delivery, or ambience/SFX/music/silence]. Avoid [only important exclusions].

### Flow settings to verify before clicking Generate

- Mode: [Text to Video / Frames / Ingredients / supported edit]
- Model: [choose from current picker after checking supported features]
- Aspect ratio/orientation: [target]
- Duration: [available length that fits the action]
- Number of outputs: [1 for controlled iteration, or requested comparison count]
- Resolution/draft option: [choose based on current quality/cost tradeoff]
- Credit cost shown: [confirm before submitting]
- Credit plan: [one draft first / comparison batch / other]
- Audio/silent-video setting: [verify if sound is required]

## Reference instructions

If using Characters, Ingredients, or Frames, add this short reference map and explain how each source should affect the result:

- `@CharacterName`: [identity/appearance/voice to preserve]
- `[ingredient name]`: [object, location, product, palette, or style role]
- Start frame: [composition to begin from]
- End frame: [composition to end on]
- Uploaded video (for supported editing): [what to preserve and what single thing to change]

Do not request contradictory visual directions. References guide the model but are not a guarantee of perfect identity or exact detail.

## Targeted revision prompt

Use after reviewing a generation. Change one main dimension at a time:

> Keep [what is already correct: identity, action, composition, timing, style, audio]. Change only [specific issue] to [desired result]. Preserve [continuity anchors]. Do not change [other elements].

Examples:

- “Keep the character, wardrobe, action, framing, and timing. Change only the lighting to soft blue dawn light; preserve the rainy street and reflections.”
- “Keep the subject and camera position. Make the action slower and easier to read: the baker lifts one loaf from the oven and places it on the counter. No additional people enter.”
- “Keep the image and scene unchanged. Remove the unintended background music and retain the natural kitchen ambience.”

For video-to-video editing, confirm the active model supports editing and select a segment within the current duration limit. State what must stay unchanged and the one intended change.

## Continuation / Extend prompt

Only use if the selected Flow model supports extending this clip:

> Continue directly from the last visible frame. Preserve the same subject identity, wardrobe, location, lighting, camera language, and audio atmosphere. Continue the action by [specific next beat]. End on [clear hold, movement, or transition point] suitable for the next edit. Do not restart or repeat the previous action.

Inspect the join carefully; extend features and restrictions vary by model.

## Scenebuilder assembly request

After selecting the desired clips, ask the Agent or use Scenebuilder:

> Arrange the selected clips in this order: [shot order]. Keep the story understandable: [brief progression]. Trim each clip at a natural action point, preserve continuity, and preview the full sequence. Flag any jump in character, location, lighting, audio, or pacing before final export. Do not delete or replace source clips. Export/download the scene at the available quality for [destination].

## Review checklist

Before approving the final sequence, check:

- The story reads in order and the opening establishes context.
- Character, wardrobe, props, location, and visual style remain consistent.
- The key action is clear and not duplicated or incomplete.
- Cuts occur at natural motion points; clips do not start/end mid-action accidentally.
- Framing, aspect ratio, and subject placement fit the destination.
- Dialogue is intelligible and short enough for the clip; ambience/music levels are usable.
- No unwanted text, visual artifacts, extra subjects, or contradictory references remain.
- The sequence export has the right duration and quality; original generations remain available.

Credit discipline: costs apply per generation and one Agent request can create multiple generations. Check the live cost and remaining balance before submitting. Generate one draft first unless a comparison batch is intentional; unused daily/monthly credits and refresh rules depend on the current account terms.

For captions, precise typography, detailed sound mixing, or frame-accurate finishing beyond current Flow controls, download the sequence and finish it in a dedicated video editor.
