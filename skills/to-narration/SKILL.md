---
name: to-narration
description: Use when writing or revising spoken narration from approved video beats, including scripts that must remain open to later visual direction.
---

# To narration

Turn `BEATS.md` into `NARRATION.md`: a production-ready draft whose wording can still be revised by scene direction and animatic evidence.

## Process

1. Read `BEATS.md`, its cited sources, and the user's voice conventions. Preserve each beat's job, claim, and handoff.
2. Write for the ear: one thought per sentence, concrete subjects and verbs, spoken transitions, and terminology explained at first use.
3. Let visuals carry visible structure, comparison, and transformation. The narration supplies meaning the image cannot communicate alone.
4. Mark paragraph-to-beat boundaries without adding visual instructions. Put unresolved pronunciation or factual questions in an `Open checks` section.
5. Write `NARRATION.md`:

```markdown
---
source: BEATS.md
status: draft
target_duration: ...
---

## B01 — Title

<a id="b01-p01"></a>
Spoken paragraph.
```

6. Give every paragraph a stable `<beat-id>-pNN` anchor. Preserve anchors when rewriting that paragraph; assign a new anchor when inserting one.
7. Read it aloud or estimate at the user's known speaking rate. Revise until every beat fits its budget and the full draft fits the target.

The draft is complete when it can be recorded for an animatic, every sentence traces to a beat, and no later visual has been prematurely prescribed. `to-video` owns the final lock after animatic review.
