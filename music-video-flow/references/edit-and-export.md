# Editing, Stabilization, and Export

## Timeline assembly

- Use exact lyric cue times to cut and arrange footage. Keep text already embedded in a source clip. If lyrics are provided only for mapping, do not add another text overlay.
- Use every scene and source clip the user requested. A scene with no lyric line may still be an intentional visual beat; retain it if it appears in the storyboard.
- Trim duplicate words or unusable lead-in/tail only when they are repeated or visibly defective. Use clean cuts or brief transitions that preserve the intended scene order.
- Avoid filling short sources with a frozen last frame. Prefer a suitable alternate take, a restrained slow-down with motion interpolation, or a disclosed duration adjustment. Do not loop a shot unless looping is intentional and visually clean.
- Preserve audio/video sync. Use the original song file; apply intro/outro fades or sound effects only as requested or clearly included in the brief.
- When a source generator returns a longer clip than its assigned timeline window (for example, a 10-second Meta render for a 4-second beat), inspect the entire source clip before trimming. Select the strongest interval by action, face/wardrobe continuity, framing, motion pace, and fit to the lyric/music cue; record the source in/out timecodes and the destination timecode.
- Do not automatically take the first seconds. Compare candidate portions across the full source and prefer the interval where the intended action reads clearly, the camera move has useful energy, and the character remains stable. If no interval works, minimally revise the prompt or source reference and generate another take; preserve rejected source files for comparison.
- For every Meta-generated clip, review every decoded frame before selecting an interval. Use normal-speed playback plus sequential frame stepping or complete, overlapping contact sheets that include every frame at readable size; do not omit intervals. Apply the same full-frame review to other sources when the user requests it or when identity continuity/artifact detection requires it. A sparse sample can be useful for a quick scan but is not proof of a full-frame review. Log detected issues and the selected clean interval.
- During that frame review, check whether the performer’s face changes inside a clip, not only between clips. Compare the beginning, middle, and end at full size and inspect any transition/morph interval frame by frame. If an identity shift is visible, mark its exact in/out range and cut before it, use a clean alternate angle or environmental insert, or request a new take when it materially harms the story. Do not assume a source-image reference guarantees a stable face, and do not imply it did.
- Maintain character continuity through edit choices as well as generation: establish the performer with a chosen reference, repeat stable wardrobe/silhouette cues, favor back/profile/wide/POV/hand shots where face drift is likely, and avoid consecutive mismatched close-ups. If some drift remains but the story reads and the selected footage looks acceptable, preserve the usable shot and disclose the limitation briefly in delivery notes.
- Transitions are available and should be chosen for the relationship between adjacent shots: match action or composition, cut on a music accent, use a motivated whip/pan continuation, or apply a brief dissolve when a dreamlike temporal blend helps. Keep cuts clean when they have more impact, avoid one repeated transition between every scene, and verify the transition does not create a face blend, freeze, black gap, or timing drift.

## Reducing shake and judder

- When the user asks for stable footage, stabilize the source clips before arranging them, then inspect for border warping, crop loss, and residual shake. Choose the least destructive available stabilization that visibly improves the clip.
- Do not imply that frame interpolation removes camera shake; it only creates smoother intermediate motion. Stabilization and slow motion are separate edits.
- Do not create a still-image substitute for a requested video clip. When motion is too short for the assigned lyric window, try a longer available take or gentle interpolation-based slow motion. Tell the user if the source has unavoidable shake or generated-motion artifacts.
- Inspect user-identified problem intervals and representative frames at the start, middle, and end of every affected scene. Check adjacent cuts for frozen frames, duplicated tails, flashes, black gaps, and abrupt timing changes.

## Export checks

- Export a broadly compatible MP4 (H.264 video, AAC audio) at the requested aspect ratio and resolution. When unspecified, use the source's intended delivery format; a standard landscape lyric video is typically 1920×1080.
- Verify the rendered file with a media probe: duration, video dimensions/codec, audio codec/sample rate, and successful decode. Check that opening and closing cards are present and that the ending is not cut off by a shorter stream.
- Review the opening, ending, reported trouble spots, and a sample from every scene. Compare consecutive frames inside clips when checking for frozen motion; a single screenshot cannot establish that a clip moves.
- Keep the final export separate from intermediate segments. Provide a direct local file link and a concise summary of the edits and checks.
