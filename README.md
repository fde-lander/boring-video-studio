# Boring Video Studio

Boring Video Studio is a collection of [Agent Skills](https://agentskills.io) for planning high-quality videos before production.

The main `boring-video` skill turns a topic, article, research bundle, or draft into four durable planning artifacts:

```text
BEATS.md → NARRATION.md → SCENES.md → STORYBOARD.md
```

It then hands the approved plan to [HyperFrames](https://www.hyperframes.dev), which owns video production, review, timing, animation, verification, and rendering. Optional [ListenHub](https://listenhub.ai) TTS support can provide narration audio and subtitles through the `listenhub-tts` skill.

The existing `verysmallwoods-video` skill remains available as the complete VerySmallWoods publishing workflow for videos, covers, platform copy, blog posts, and social posts.

## Installation

Install the skills from this repository:

```bash
npx skills add sugarforever/boring-video-studio
```

Video production requires HyperFrames and its local dependencies. Check the environment with:

```bash
npx hyperframes doctor
```

## Usage

Ask your agent to use `boring-video` with a topic or source document:

```text
Use boring-video to turn this article into a planned eight-minute faceless explainer.
```

The skill asks for any missing presentation, collaboration, voice, and design choices, then runs the planning chain:

1. `to-spec-beats` defines the argument and learning progression.
2. `to-narration` writes the spoken draft.
3. `to-scenes` designs visual events, worlds, action, and continuity.
4. `to-storyboard` translates the scenes into buildable shots.
5. `to-video` hands the complete plan and optional ListenHub narration to the appropriate HyperFrames workflow.

You can also invoke an individual stage when you already have its input:

```text
Use to-scenes to redesign the visual direction for this narration.
```

```text
Use to-storyboard to turn SCENES.md into a HyperFrames storyboard.
```
