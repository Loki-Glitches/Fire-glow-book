# [Project Title] — Project

## Project Overview
<!--
Describe the project: genre/format, length or duration target, core premise, setting, primary characters or voices.
This is what the Director agent reads first to understand the project.

Supported formats: Novel, Screenplay, Audio Drama, Stage Play, Podcast, Short Fiction, etc.
-->

**Format:** <!-- Novel | Screenplay | Audio Drama | Stage Play | Podcast | Other -->
**Target length:** <!-- word count, page count, episode count, runtime — whatever fits your format -->
**Genre:**
**Setting:**
**Primary characters/voices:**

## Authoritative Sources
All agents MUST treat these documents as canonical:

- **Story Bible:** `bible/story-bible.md` — world, characters, timeline, themes
- **Unit Plans:** `bible/unit-plans.md` — per-unit targets and constraints (chapters, scenes, episodes, etc.)
- **Style Guide:** `bible/style-guide.md` — voice samples, sentence rhythm, POV/perspective rules
- **Soul:** `.claude/agents/soul.md` — project voice, identity, and non-negotiable values

## Project Structure

### [Part/Section Name]
<!-- Describe each structural section, unit ranges, and length targets -->

## Agent Architecture

### Roles
- **Director** (`.claude/agents/director.md`): Orchestrates, reviews, assigns revision notes. Does NOT write units.
- **Writers** (`.claude/agents/agent-generic-writer.md`): Each instance writes ONE assigned unit (chapter, scene, episode, etc.).
- **Continuity Checker** (`.claude/agents/agent-generic-continuity-checker.md`): Full sequential read, flags drift and seam problems.
- **Proofreader** (`.claude/agents/agent-generic-proofreader.md`): Fact-checks geography, physics, arithmetic, behavioral consistency.
- **Story Integrity** (`.claude/agents/agent-generic-story-integrity.md`): Scores fidelity to the project's soul and style guide.
- **Synthesis** (`.claude/agents/agent-generic-synthesis.md`): Distills per-unit notes into a living summary for all agents.

### The Window Rule (CRITICAL)
Each writer receives:
- **Unit n-1** (READ ONLY) — preceding unit, for continuity of tone and timeline
- **Unit n** (READ/WRITE) — the unit they are writing. Their ONLY writable file.
- **Unit n+1 outline** (READ ONLY) — next unit's plan, so they know where the story is going

### File Ownership
| Path              | Who Writes         | Who Reads                              |
| ----------------- | ------------------ | -------------------------------------- |
| `units/unitNN.md` | Unit N writer only | Director, Continuity, adjacent writers |
| `notes/*`         | Any agent          | Any agent                              |
| `bible/*`         | Director only      | All agents                             |

<!--
Rename the `units/` directory and file naming convention to match your format:
- Novel: `chapters/ch01.md`
- Screenplay: `scenes/sc01.md`
- Audio Drama: `episodes/ep01.md`
- Podcast: `episodes/ep01.md`
-->

## Writing Rules

### Voice
<!-- Define the voice for each character or narrator. Reference bible/style-guide.md for samples. -->

### Show, Don't Tell (NON-NEGOTIABLE)
- NEVER explain thematic connections in narration or dialogue
- NEVER have characters speechify about the project's themes
- NEVER write exposition dumps — filter information through character experience or action

### Pacing by Section
<!-- Define pacing expectations per part/section -->

### What This Project Is NOT
<!-- Define what this project should NOT become — genre drift, tonal drift, format drift, etc. -->

## Workflow

### Phase 1: Proof of Concept
<!-- Which units can be written independently to validate the pipeline? -->

### Phase 2 onward
<!-- Sequential phases respecting the n-1 dependency chain -->

## Decision Authority
- The story bible is law
- The author has final authority
- Disputed items go to `notes/author-questions.md`
