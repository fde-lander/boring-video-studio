# Video Skills Pipeline Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the legacy video skills with five artifact-driven transformations and a new Boring Video planning orchestrator.

**Architecture:** Each `to-*` skill owns one conversion and one durable artifact. `boring-video` routes through the planning chain and hands its outputs to HyperFrames. `to-video` is a thin handoff with optional ListenHub support; `verysmallwoods-video` remains unchanged.

**Tech Stack:** Agent Skills Markdown, HyperFrames workflows, repository shell validation.

## Global Constraints

- Delete `skills_v2/` and `skills_legacy/`.
- Use `general-video` for custom, longer, or multi-scene VerySmallWoods videos.
- Ask whether the user wants a faceless presentation before choosing the HyperFrames workflow.
- Keep `verysmallwoods-video` unchanged.
- Keep every meaning in one source of truth.

---

### Task 1: Artifact conversion skills

**Files:**
- Create: `skills/to-spec-beats/SKILL.md`
- Create: `skills/to-narration/SKILL.md`
- Create: `skills/to-scenes/SKILL.md`
- Create: `skills/to-storyboard/SKILL.md`
- Create: `skills/to-video/SKILL.md`
- Create: `skills/to-scenes/references/scene-format.md`

- [ ] Define one input, output, revision loop, and completion criterion for each conversion.
- [ ] Validate frontmatter, pointers, and absence of duplicated production knowledge.

### Task 2: Boring Video router

**Files:**
- Create: `skills/boring-video/SKILL.md`

- [ ] Orchestrate the five-skill chain without reproducing HyperFrames production instructions.
- [ ] Ask the presentation question and route custom or longer videos to `general-video`.
- [ ] Add ListenHub as an explicit optional voice branch.

### Task 3: Remove historical implementations and verify

**Files:**
- Delete: `skills_v2/`
- Delete: `skills_legacy/`

- [ ] Confirm only the current skills remain.
- [ ] Check every skill frontmatter and every local context pointer.
- [ ] Search for stale legacy and default-faceless routing language.
