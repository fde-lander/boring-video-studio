---
name: verysmallwoods-video
description: Use when producing a complete VerySmallWoods episode or publishing bundle from a topic, article, research, narration, or existing video-planning artifact.
---

# VerySmallWoods video

Orchestrate one publishable episode. The five `to-*` skills own video planning and production; this skill owns intake, routing, publishing assets, and delivery completeness.

## Intake

Resolve known choices from the request and existing project files. Ask one compact question for the remaining choices:

1. **Presentation:** faceless explainer, or another form such as footage, screen capture, talking head, or mixed media?
2. **Collaboration:** co-direct with storyboard reviews, or let the agent execute and present the final preview?
3. **Voice:** user recording or TTS?
4. **Design:** existing design truth, named preset, or a new direction? In agent-executed work, choose a concept-led direction when the user has not constrained it and record the choice for final review.

Record the answers in `BRIEF.md`. A supplied project artifact is resumable state: begin at the first missing or explicitly revised conversion.

## Video chain

Run each missing conversion in order:

1. `/to-spec-beats` → `BEATS.md`
2. `/to-narration` → `NARRATION.md`
3. `/to-scenes` → `SCENES.md`
4. `/to-storyboard` → `STORYBOARD.md`
5. `/to-video` → approved preview and requested renders

Each artifact is the next skill's interface. Finish its completion criterion before moving forward; when a later pass exposes a real conflict, revise the artifact that owns that decision and propagate the change.

## HyperFrames route

Use `/hyperframes` to establish the project contract. For a custom, longer, or multi-scene VerySmallWoods episode, set `workflow: general-video`; `/general-video` owns the HyperFrames implementation while `/to-video` owns the production state machine.

When the user confirms faceless and the requested duration fits the current `/faceless-explainer` contract, that specialized workflow may own production. Faceless presentation and workflow selection are separate decisions: a faceless eight-minute technical essay still routes to `/general-video` when the specialized workflow's duration contract does not fit.

Read [`references/video.md`](references/video.md) when selecting the route or starting the five-stage chain. Read [`references/audio.md`](references/audio.md) when the voice branch begins.

## Publishing bundle

After the final visual direction and locked narration are stable:

- five covers: 16:9, 16:10, 4:3, 3:4, and 9:16;
- `youtube.md` and `bilibili.md`;
- `blog.md`;
- one concise social post.

Use the existing references for these outputs: `covers.md`, `platform-copy.md`, and `blog-and-tweet.md`.

## Done

The episode is complete when the five video artifacts satisfy their owners, requested renders are verified, all publishing items exist, and their titles, claims, terminology, and links agree with the locked narration.
