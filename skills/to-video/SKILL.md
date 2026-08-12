---
name: to-video
description: Use when approved video-planning artifacts must be handed to HyperFrames for production, with optional ListenHub narration.
---

# To video

Hand approved planning to HyperFrames. HyperFrames owns animatic or review passes, timing, media assembly, animation, verification, approval, and rendering.

## Process

1. Confirm `BEATS.md`, `NARRATION.md`, `SCENES.md`, and `STORYBOARD.md` agree on stable beat and narration IDs. Return a conflict to the skill that owns that artifact.
2. Read `/hyperframes` and select the workflow by its current routing contract. Use `/general-video` for custom, longer, or multi-scene work; use a specialized workflow only when its contract fits.
3. Give the selected workflow the four planning artifacts, source material, design constraints, presentation choice, collaboration preference, and voice choice. Treat them as project truth while allowing HyperFrames' own review loop to revise them.
4. When the user chooses ListenHub, wait for the selected HyperFrames workflow's voice gate, then use `/listenhub-tts` on that narration version. Give its audio and SRT back through `/media-use`. If the workflow later revises the narration, treat those outputs as stale and regenerate them at the next voice gate.
5. Leave production inside the selected HyperFrames workflow through its own completion criterion.

The handoff is complete when HyperFrames has accepted the planning artifacts and any requested ListenHub outputs into its project state.
