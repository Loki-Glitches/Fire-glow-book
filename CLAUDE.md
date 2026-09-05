# Beneath the Fire's Glow — Project

## Project Overview
**Format:** Novel
**Target length:** 70+ chapters (no fixed word-count target — see `bible/style-guide.md` § "No Writing to a Word Count")
**Genre:** Paranormal romance / contemporary fantasy, character-driven — resists genre-typical tropes on purpose (see `.claude/agents/soul.md` § "What This Story Is NOT")
**Premise:** Lucifer, cast out of Heaven for giving Eve the Tree of Knowledge, comes to Earth centuries later hunting Eve after she escapes Hell's prison. Living under the alias "Adrian" in a small town, he meets Elizabeth, an ordinary woman, and the story follows his slow, non-linear recovery of everything the Fall took from him — emotion, lightness, the capacity to love and be loved — while his brother Azrael ("Tristan") evaluates whether Lucifer is fit to bond with a human at all.
**Setting:** A small, unnamed contemporary American town (present day, summer), with parallel scenes in Hell.
**Primary characters/voices:** Lucifer / "Adrian" (POV) and Elizabeth (POV) are the two POV characters. Azrael / "Tristan" (Lucifer's brother, no POV chapters of his own) evaluates the bond throughout. Sam is Elizabeth's older brother and caretaker. Eve is the antagonist, absent from the page until Act Three. James, Claire, and Sophie round out the town's supporting cast.

## Authoritative Sources
All agents MUST treat these documents as canonical:

- **Story Bible:** `bible/story-bible.md` — world, characters, timeline, themes
- **Unit Plans:** `bible/unit-plans.md` — per-unit targets and constraints (chapters, scenes, episodes, etc.)
- **Style Guide:** `bible/style-guide.md` — voice samples, sentence rhythm, POV/perspective rules
- **Soul:** `.claude/agents/soul.md` — project voice, identity, and non-negotiable values
- **Synthesis:** `notes/synthesis-current.md` — living summary of every locked decision, chapter status, and open thread. **Read this first in any new session** — it's the fast path to full context without re-reading every note file or the whole prior conversation.

## Starting a New Session
This project spans 70+ chapters — don't run the whole book in one continuous conversation. Start a fresh session per chapter (or small batch): the git branch, bible files, chapters, and notes are the persistent state, not the chat history. A new session should open by reading `notes/synthesis-current.md`, then `bible/unit-plans.md` for the next unwritten chapter's plan, then proceed. Run the Synthesis agent again at the end of each chapter (or small batch) to keep that doc current for the next session.

**Check `notes/synthesis-current.md` for a standing blocker note before doing anything else.** As of 2026-09-05 the author has a pending instruction there that overrides the normal flow above — read its top section first, every session, until it says the blocker is cleared.

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
