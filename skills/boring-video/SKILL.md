---
name: boring-video
description: Use when developing a topic, article, research bundle, or draft into a planned video and then handing it to HyperFrames for production.
---

# Boring video

Orchestrate video pre-production as a chain of durable artifacts, then hand the approved plan to HyperFrames. Each `to-*` skill owns one conversion.

## Intake

Resolve existing decisions from the request and project files. Ask one compact question for the missing choices:

1. **Presentation:** faceless, footage, screen capture, talking head, or mixed media?
2. **Collaboration:** storyboard reviews or agent-executed production with final preview?
3. **Voice:** HyperFrames voice, ListenHub TTS, user recording, or no narration?
4. **Design:** existing design truth, named direction, or agent-proposed direction?

Record the answers in the HyperFrames `BRIEF.md`. In agent-executed work, propose and record a design direction when the user leaves it open.

## Chain

Start at the first missing or explicitly revised artifact:

1. `/to-spec-beats` → `BEATS.md`
2. `/to-narration` → `NARRATION.md`
3. `/to-scenes` → `SCENES.md`
4. `/to-storyboard` → `STORYBOARD.md`
5. `/to-video` → HyperFrames handoff

Finish each skill's completion criterion before advancing. A downstream finding returns to the artifact that owns the decision, then propagates forward.

## Handoff

Presentation and workflow are separate decisions. Collect the presentation intent without selecting a workflow from memory. `/to-video` reads the current `/hyperframes` contract and performs the route.

## Done

Pre-production is complete when the four planning artifacts agree and satisfy their owners. The wrapper run is complete when `/to-video` has transferred that truth, plus the confirmed voice branch, into the selected HyperFrames project.
