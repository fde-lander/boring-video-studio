---
name: to-storyboard
description: Use when approved video scenes need to be translated into shots, key frames, compositions, camera moves, transitions, and timing estimates before production.
---

# To storyboard

Turn `SCENES.md` and `NARRATION.md` into HyperFrames `STORYBOARD.md`. Scenes define events; the storyboard defines how the viewer sees them.

## Process

1. Load `/hyperframes-core`, then read its current `references/storyboard-format.md`. That canonical contract is authoritative for `STORYBOARD.md`.
2. Choose the HyperFrames frame boundary:
   - start a new frame for a hard edit, independent transition, new visual world, materially different media source, or independently buildable unit;
   - keep continuous camera movement and shared object state in one frame, describing its internal shot moments.
3. Treat each HyperFrames frame as one buildable block. Within its narrative body, write an ordered `Shot moments` list at changes in viewpoint, shot scale, subject action, or information focus. Each moment declares:
   - moment ID and approximate offset;
   - initial state → action → final state;
   - camera and attention path;
   - narration anchors, or `silent`;
   - handoff to the next moment or frame.
4. Use canonical metadata wherever the current contract already carries the meaning. Put only missing workflow data in extras prefixed `boring_`, such as `boring_scene_id`.
5. Use the scene's world, hero, event, continuity, rhythm, and feasibility as constraints. Preserve the cognitive job from `BEATS.md`.
6. Treat canonical HyperFrames fields as authoritative. A `boring_*` extra supplements the contract; it never restates a canonical field.
7. Audit the sequence: every narration anchor is covered by one or more shot moments, intentionally silent moments carry no anchor, frame boundaries follow the rules above, the action is legible without reading the narration, and estimated duration accommodates both speech and action.

The storyboard is complete when every frame is an independently buildable block, its shot moments fully describe the scene event, and every transition connects actual end and start states. HyperFrames owns sketching and storyboard review after handoff.
