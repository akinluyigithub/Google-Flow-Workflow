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

Make every choice easy to answer with one letter or number. Prefer actual clickable choices; otherwise list concise choices on separate lines. Include “Choose for me” and “Describe my own” where appropriate. At approvals, offer explicit Approve / Revise / Stop choices and wait for the selected approval.

At every choice, mark one option **Recommended** and give a brief reason. Do not imply the user has agreed just because a recommendation is present.

For open-ended choices, show the full useful menu (typically six or seven options) rather than arbitrarily limiting the user to three. Include a choose-for-me path and a describe-my-own path where applicable. Reserve compact Approve / Revise / Stop menus for approval gates.

For video generations, obtain explicit approval separately for every clip. Show the exact clip prompt, model/mode, frame or ingredient inputs, aspect ratio, duration, output count, and live displayed credit cost. Approval for planning, a previous clip, or a production package does not authorize another video generation. Never disable Flow's generation confirmation.

Before producing still images, ask whether to use ChatGPT Images or Google Flow Images. Default to 9:16 portrait and one image per prompt; if Flow Images is selected, use Nano Banana 2.1 when available. A larger Flow batch is optional: show the number of images and live cost and ask before submitting. Inspect the results and offer a focused rerun or provider change if needed.

When proposing settings, use only options visible in the current Flow interface. Model names, features, output lengths, credit costs, and availability can change by account, region, and rollout. If a requested mode is not supported by the active model, tell me and offer a supported alternative.

## Shot plan template

Create a plan using this table before generation:

| Shot | Story purpose | Subject and action | Setting | Framing and camera | Lighting and style | Audio | Continuity anchors |
|---|---|---|---|---|---|---|---|
| 1 | [opening/context/etc.] | [one main action] | [place/time] | [shot size + one movement] | [look] | [sound/dialogue] | [character/wardrobe/props/palette] |

Keep each Flow clip to one main action and one coherent camera idea. Split different locations, actions, or camera setups into separate clips. Repeat essential continuity details in every prompt.

For a multi-shot project, first create a **continuity pack**:

- Character identity reference(s): [name, clear reference image(s), wardrobe, saved Flow voice name/preset and stable voice lock for each speaker]
- Location/environment reference(s): [clean image for each recurring place; omit unintended people]
- Prop/product reference(s): [important details and orientation]
- Visual rules: [palette, lens/framing language, lighting, aspect ratio]
- Storyboard frames: [one full-frame still per planned shot when needed as a video reference]

Review this pack and the storyboard before paying to animate every shot. Text planning and review does not itself use video-generation credits, while generations do. Build the visual references and storyboard as separate assets; a contact sheet may help review, but individual full-size frames are usually easier to use as shot references.

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

If model quality is uncertain, run one controlled comparison on a representative shot: use the same source frame/reference, prompt, duration, aspect ratio, and output count, changing only the model. Compare identity, action, artifacts, motion, and sound. Do not assume tutorial results predict the current model picker.
- Audio/silent-video setting: [verify if sound is required]

## Reference instructions

If using Characters, Ingredients, or Frames, add this short reference map and explain how each source should affect the result:

- `@CharacterName`: [identity/appearance/voice to preserve; include stable voice performance and any scene-specific delivery]
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

## Google Flow edit request

For a generated edit, select the exact clip and request one targeted change:

> Keep [identity, action, framing, timing, wardrobe, props, setting, and sound that must remain]. Change only [one requested element] to [desired outcome]. Preserve [continuity details]. Do not change [other fixed elements].

Before generating an AI edit, verify that the selected model supports video-to-video editing in this account/region, identify the segment and current duration limit, and show the displayed credit cost. Wait for explicit approval for that edit. Compare the result against the original in History/asset stack; retain the original and choose the desired version only after review.

For simple cuts, add accepted clips to Scenebuilder, place them in story order, use in/out handles to trim, then preview the whole sequence and inspect every join for cut dialogue, unfinished motion, repeated frames, pacing, and abrupt audio. Check runtime and export the scene. Use a dedicated editor for precise multitrack audio, captions, titles, color work, or frame-accurate finishing that Flow does not currently expose.

Use **Extend** only after checking that the selected Veo model supports it. Describe the continuation from the final visible moment, verify its cost, and obtain clip-specific approval before generation. Extended clips may restrict other edit modes afterward.

## Review checklist

Before approving the final sequence, check:

- The story reads in order and the opening establishes context.
- Character, wardrobe, props, location, and visual style remain consistent.
- Each speaker retains the approved saved character voice, language/accent/pronunciation, register, and baseline performance; scene-specific emotional delivery remains intentional and consistent. Do not switch voices or alter dialogue without approval.
- The key action is clear and not duplicated or incomplete.
- Cuts occur at natural motion points; clips do not start/end mid-action accidentally.
- Framing, aspect ratio, and subject placement fit the destination.
- Dialogue is intelligible and short enough for the clip; ambience/music levels are usable.
- No unwanted text, visual artifacts, extra subjects, or contradictory references remain.
- The sequence export has the right duration and quality; original generations remain available.

Credit discipline: costs apply per generation and one Agent request can create multiple generations. Check the live cost and remaining balance before submitting. Generate one draft first unless a comparison batch is intentional; unused daily/monthly credits and refresh rules depend on the current account terms.

When a specific real person's appearance matters, use an appropriate reference image with permission and keep it as the identity source; descriptive text alone may produce a different face. Keep environment references separate and free of unintended people when character identity must remain clear.

For captions, precise typography, detailed sound mixing, or frame-accurate finishing beyond current Flow controls, download the sequence and finish it in a dedicated video editor.
