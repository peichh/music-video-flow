# Scene Planning and Generation

## Choose a format from the prompt

Infer the deliverable from the user's wording and creative brief. Common choices:

| Prompt intent | Planning approach | Text treatment |
| --- | --- | --- |
| Narrative or performance MV | Build a beginning, progression, and ending around the song; use recurring character(s) only when asked or clearly implied | Lyrics are optional; add only if requested |
| MV with a lead character | Define a compact character reference (appearance, wardrobe, age range, key props, mannerisms) and repeat it in every relevant scene prompt; plan emotional/action continuity | Do not assume on-screen lyrics |
| MV without a lead character | Use settings, objects, environmental action, symbolic motifs, light, and camera movement as the visual thread | Do not invent a protagonist |
| Lyric video / visualizer | Map exact lyric lines to LRC/audio timestamps and create visual beats that support them | Ask/derive whether text is already in the footage, will be overlaid, or is only for mapping |
| Prompt-led scene montage | Break the prompt into an ordered sequence of distinct shots; use music timing if audio was provided | No lyric text unless requested |

If the prompt names a format, follow it. If it implies one (for example, “story with the same woman throughout”), use that inference and state it in the proposed treatment. If the format or presence of a lead character remains ambiguous and would change the whole storyboard, ask one focused question before expensive generation. Do not make the user choose among format labels when the prompt already makes their intent clear.

## Treatment and scene plan

- Distill the prompt into a one-paragraph concept, mood, visual style, and continuity rules before drafting individual scenes.
- For an open-ended MV brief, compare a few meaningfully different plot premises before choosing one. Prefer a plot with a concrete visual engine, progression, turn, and payoff that tracks the song's emotional arc; do not settle for a sequence of attractive but interchangeable portraits.
- Order scenes to form a clear visual arc, whether that arc comes from a story, changing visual motifs, lyric progression, or the prompt's sequence.
- Keep the plan flexible to the project: use exact lyric cues for lyric videos, musical sections for narrative MVs, and prompt logic for short scene montages.
- Give each section a distinct dramatic action or visual development. Change location, blocking, composition, and camera grammar when the story calls for it; repeat a shot only as a deliberate visual motif.
- Track each scene's ID, lyric/music cue, intended timeline duration, expected generated duration, source/generation state, action, location, character presence, shot size/angle, camera move and pace, transition, and generation prompt. For lyric work also track exact lyric text and cue times.

## Director-level shot design

- Build a usable coverage plan, not only a prompt paragraph. Mix establishing wides, close-ups, inserts, overhead or low angles, POV, over-the-shoulder views, tracking/panning shots, and environment-only beats as appropriate to the story. The lead character does not need to appear in every shot.
- Specify what changes inside the shot. For time-coded generators, write a compact motion arc (for example, opening composition, subject action, camera move, reveal or turn, end pose) with approximate time ranges. Avoid relying on generic directions such as “slow cinematic movement” or “slow push-in” alone.
- Choose camera speed and movement to serve the beat: define the beginning and end framing, direction, and whether the camera accelerates, settles, follows, or stops. Keep each generated clip to one coherent shot unless a multi-shot generation is explicitly requested.
- If a service has a fixed or longer output duration than the timeline beat, design a complete source-clip arc for that duration. Plan to select the best subrange during editing rather than expecting the generator to obey a shorter requested duration.

## Inputs and timeline

- Inventory the audio, lyric text/LRC, existing scenes, and prompts before making a storyboard. Keep source files unchanged.
- Parse LRC timestamps as the primary cue points. Check that cues are ordered and fall within the song. Preserve the lyric wording exactly; if the LRC seems wrong against the audio, flag the line and ask before changing it.
- Build a scene map with: cue start, cue end, exact lyric, scene/source ID, visual intent, and generation prompt. Ensure every lyric cue has coverage and every requested source scene is accounted for.
- Map each chorus occurrence to its own supplied visuals when available. Reuse a scene only when it is an intentional repeated visual or the user asks for reuse.
- Plan a short opening and ending card only when requested or when they are part of the supplied brief. Keep the full song audio and handle fades separately from video transitions.

## Writing visual prompts

- Derive prompts from the selected video mode and source prompt. For lyric videos, use the lyric's meaning and mood without altering the lyric; for narrative MV, specify action and story continuity; for a no-character MV, focus on places, objects, atmosphere, and visual motifs.
- State the subject, setting, composition, lighting, motion, camera behavior, aspect ratio, and continuity details that matter. Keep adjacent shots visually coherent without making them identical.
- When a recurring character is part of the brief, repeat the defining traits and wardrobe in every image/video prompt; use a character reference image where the service supports it. Do not assume identity/wardrobe continuity will persist automatically between generations.
- Plan continuity across generated clips with robust visual anchors (silhouette, hair length/color, wardrobe palette, signature prop, movement, and environment) as well as face description. A reference image can help, but image-to-video may still alter facial features within a clip. Avoid making a sequence of close face shots the only way the audience can follow the story; use motivated wides, rear/profile views, POV, hands, shadows, and location details as narrative coverage.
- Treat face-match as a review criterion, not a promise. When the face changes between clips, decide whether it is noticeable at the intended playback size and whether it breaks the story. If it does, replace or shorten that interval, cover it with a different angle/insert, or regenerate the affected scene; retain the best usable motion when the difference is minor and be candid about the limitation. Do not use a dissolve or morph to conceal a visible identity error.
- When a lead character is excluded, explicitly say no visible protagonist/lead character and describe the environmental or symbolic subject instead.
- For a motion prompt, describe movement within the shot rather than asking the model to render a whole sequence of unrelated scenes.
- For image-to-video references sent to Meta, use only the actual local image file created outside Meta by the image-generation tool. Upload that file to the target Meta chat and retain the source path and scene ID. Do not attach or select a Meta-generated still as a reference frame.
- If Meta rejects an image or prompt, identify the smallest detail likely causing rejection and revise only that detail. Keep the plot beat, character, setting, and remaining visual direction intact when they are allowed. Do not evade the service's content rules; if a compliant edit is uncertain, ask the user which story element to adjust.
- If the user provides finished footage, do not generate replacement imagery unless they request it. If the user asks for images, generate only the needed images and preserve their scene IDs and order.

## Browser generation workflow

- Use the current Chrome tab and service identified by the user. Confirm the visible workspace is the right one before uploading.
- Attach only user-authorized source images generated outside Meta from their local files. Maintain a clear scene-to-source-file-to-prompt mapping. Do not use a Meta-created image as a source even if the interface offers a “Use as reference” control.
- If the service supports selecting multiple eligible images in one batch, batch the requested set. Maintain a clear scene-to-source-file-to-prompt mapping.
- Generate each scene as a distinct result unless the user explicitly asks for a montage or multi-scene clip. Keep the lyric content unchanged and use prompts only to guide visual interpretation.
- Observe the service's actual limits and wait for generation completion. If the site changes a prompt, substitutes a still, omits a source, or asks for an unexpected permission/choice, stop before accepting that material change.
- Download completed clips to the project folder and name them with ordered scene IDs. Verify each downloaded clip opens and matches its intended scene before editing.
