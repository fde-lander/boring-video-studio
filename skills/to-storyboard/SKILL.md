---
name: to-storyboard
description: Use when approved video scenes need to be translated into shots, key frames, compositions, camera moves, transitions, and timing estimates before production.
---

# To storyboard

Turn `SCENES.md` and `NARRATION.md` into HyperFrames `STORYBOARD.md`. Scenes define events; the storyboard defines how the viewer sees them.

## Process

1. Read the scene source and the canonical `/hyperframes-core` storyboard format and review loop.
2. Break each scene at changes in viewpoint, shot scale, subject action, information focus, or edit. A continuous camera move may remain one shot with multiple key moments.
3. For every frame, include the canonical metadata plus these workflow fields:
   - `scene_id`: parent scene
   - `shot`: shot number within that scene
   - `start_frame`: initial composition and subject state
   - `end_frame`: final composition and changed state
   - `camera`: shot scale, angle, and movement
   - `action`: subject choreography
   - `focus`: attention path
   - `transition_out`: visual handoff
   - `narration_ref`: stable paragraph anchor from `NARRATION.md`
4. Use the scene's world, hero, event, continuity, and rhythm as constraints. Preserve the cognitive job from `BEATS.md`.
5. Produce key-frame sketches when `storyboard: yes`, then run the shared HyperFrames storyboard review loop.
6. Treat canonical HyperFrames fields as authoritative. Store the workflow fields above as preserved extra metadata; choose names that do not shadow a canonical field.
7. Audit the sequence: every narration anchor is covered once, the action is legible without reading the narration, shot-scale and rhythm vary intentionally, every transition connects actual end and start states, and estimated duration accommodates both speech and action.

The storyboard is complete when every shot is buildable from its block, every scene event is fully covered, and the user has approved the review surface when review was requested.
