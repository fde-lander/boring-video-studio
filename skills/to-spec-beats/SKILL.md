---
name: to-spec-beats
description: Use when turning a topic, article, research bundle, or existing draft into the content architecture for a narrated video.
---

# To spec beats

Turn source material into `BEATS.md`: the video's factual and narrative spine. This pass decides what the viewer learns and in what order; later passes decide wording and visuals.

## Process

1. Read every supplied source and existing fact-check. Resolve material factual uncertainty before treating a claim as a beat.
2. Define the audience, prior knowledge, one-sentence thesis, desired change in understanding, target duration, and scope boundary.
3. Build the reverse-iceberg arc: hook in viewer language, value or answer by beat two, then evidence, mechanism, implications, and close.
4. Give every beat one cognitive job. Split beats that require two independent realizations; remove beats whose job does not trace to the thesis.
5. Write `BEATS.md` beside the source material using this shape:

```markdown
---
audience: ...
thesis: ...
viewer_shift: ... → ...
target_duration: ...
---

## B01 — Title
- job: What changes in the viewer's understanding
- claim: The factual statement this beat establishes
- evidence: Source or observation supporting it
- setup: Prior beat knowledge this depends on
- handoff: Question or tension passed forward
- duration: Rough narration budget

Notes needed to write this beat accurately.
```

6. Audit the complete file: every claim has support, every dependency points backward, the thesis lands by beat two, and the duration budgets fit the target.

Beat IDs are stable interfaces. Preserve them through revisions and assign a new ID when inserting a beat.

`BEATS.md` is complete when another writer can draft the narration without inventing the argument, claims, order, or scope.
