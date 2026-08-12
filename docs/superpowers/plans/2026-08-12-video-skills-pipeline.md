# Video Skills Pipeline Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the legacy video skills with five artifact-driven transformations and a thin VerySmallWoods delivery orchestrator.

**Architecture:** Each `to-*` skill owns one conversion and one durable artifact. `verysmallwoods-video` routes into the chain, asks whether the requested video is faceless, delegates custom or longer work to `general-video`, and retains only the publishing bundle.

**Tech Stack:** Agent Skills Markdown, HyperFrames workflows, repository shell validation.

## Global Constraints

- Delete `skills_v2/` and `skills_legacy/`.
- Use `general-video` for custom, longer, or multi-scene VerySmallWoods videos.
- Ask whether the user wants a faceless video before choosing the visual workflow.
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

### Task 2: VerySmallWoods router

**Files:**
- Modify: `skills/verysmallwoods-video/SKILL.md`
- Modify: `skills/verysmallwoods-video/references/video.md`
- Modify: `skills/verysmallwoods-video/references/audio.md`

- [ ] Replace the monolithic video path with the five-skill chain.
- [ ] Add the faceless question and route custom or longer videos to `general-video`.
- [ ] Keep publishing artifacts and final delivery checks in the orchestrator.

### Task 3: Remove historical implementations and verify

**Files:**
- Delete: `skills_v2/`
- Delete: `skills_legacy/`

- [ ] Confirm only the current skills remain.
- [ ] Check every skill frontmatter and every local context pointer.
- [ ] Search for stale legacy and default-faceless routing language.
