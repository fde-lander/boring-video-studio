---
name: to-video
description: Use when approved beats, narration, scenes, and storyboard must become a timed HyperFrames production, including animatic, narration lock, voice, retiming, animation, verification, and render.
---

# To video

Turn the four planning artifacts into an approved video. This skill owns the production state machine; the selected HyperFrames workflow owns implementation.

## Required inputs

- `BEATS.md`
- `NARRATION.md`
- `SCENES.md`
- `STORYBOARD.md`
- the project's design truth and `BRIEF.md`

## Process

1. **Preflight.** Confirm all four artifacts agree on thesis, beat order, scene coverage, shot order, and narration references. Return contradictions to their owning artifact.
2. **Animatic.** Assemble storyboard frames against scratch narration or timed text at `animatic/animatic.mp4`. Write `ANIMATIC.md` with `status: draft`, the source artifact revisions, duration, review findings, and output path. Include cuts, holds, camera intent, and provisional transitions. Review comprehension, action time, shot variation, and total rhythm on playback.
3. **Lock.** Apply animatic findings upstream and regenerate every dependent artifact. Set `NARRATION.md` to `status: locked` only when wording and shot timing support each other. Set `ANIMATIC.md` to `status: approved` and record the approved artifact revisions.
4. **Voice.** Use `/media-use` for narration media. Follow the confirmed branch: user recording plus SRT, or the selected TTS skill. The resulting audio and cue timings become temporal truth.
5. **Retime.** Align shots, actions, focus changes, and transitions to real cues. Preserve the approved scene events while allowing the real voice duration to replace estimates. Record the timing map at `audio/audio_meta.json` using the selected HyperFrames workflow's current schema.
6. **Build.** Use `/general-video` as the owning HyperFrames workflow for custom, longer, or multi-scene production. Load `/hyperframes-core`, `/hyperframes-creative`, `/hyperframes-animation`, and `/hyperframes-cli` when their matching stage begins. Build from storyboard blocks and inspected design truth.
7. **Verify and approve.** Complete the owning workflow's checks, snapshots, animation-map review, design-adherence review, final Studio approval, and requested render verification.

Production is complete when the locked narration and real audio match the cut, every storyboard shot realizes its parent scene event, HyperFrames checks pass, the user approves the final preview, and every requested render is verified.
