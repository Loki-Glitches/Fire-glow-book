# Beneath the Fire's Glow — Project

## Project Overview
**Format:** Novel
**Target length:** 70+ chapters (no fixed word-count target — see `bible/style-guide.md` § "No Writing to a Word Count")
**Genre:** Paranormal romance / contemporary fantasy, character-driven — resists genre-typical tropes on purpose (see `.claude/agents/soul.md` § "What This Story Is NOT")
**Premise (reworked 2026-09-11):** Lucifer, banished from the Garden of Eden and barred from Heaven by his own duties as Hell's warden, comes to Earth centuries later hunting Eve after she escapes Hell's prison. He has power from the start — under strict orders never to reveal his own divinity or his mission, and never to use power where a human can witness it — and hates Earth and humans generally, though not God. Living under the alias "Adrian" in a small town, he meets Elizabeth, who genuinely hates him at first; she stays in his orbit because she's drawn to things she reads as broken and can tell he's lashing out at something. The story follows his slow recovery — from a volatile, caustic baseline toward the joyful, unguarded person he was before the Fall, accelerating once he falls for her — while his brother Azrael ("Tristan"), whose usual death-duty has been temporarily reassigned to another angel, works to contain him instead of evaluating him.
**Setting:** A small, unnamed contemporary American town (present day, summer), with parallel scenes in Hell, and a shared home base — a vacant mansion at the top of the town hill that Lucifer buys.
**Primary characters/voices:** Lucifer / "Adrian" (POV) and Elizabeth (POV) are the two POV characters. Azrael / "Tristan" (Lucifer's brother, no POV chapters of his own) now works to contain Lucifer rather than evaluate the bond — present in every Lucifer scene until Elizabeth knows the truth; the two physically fight over the course of the book (neither can die, both heal within 24 hours). Sam is Elizabeth's older brother and caretaker. Eve is the antagonist, absent from the page until Act Three. James, Claire, and Sophie round out the town's supporting cast.

*(Full detail on the 2026-09-11 rework: `bible/lucifer_character_profile.md`, `bible/tristan_azrael_character_profile.md`, `bible/elizabeth_character_profile.md`, `bible/bond_system_reference.md`, and the raw conversation record in `notes/creative-partner-session.md`.)*

## Authoritative Sources
All agents MUST treat these documents as canonical:

- **Story Bible:** `bible/story-bible.md` — world, characters, timeline, themes
- **Manuscript Order:** `bible/manuscript-order.md` — the ONLY source of truth for chapter sequence. Chapters are identified by title, never by number — no filename, cross-reference, or note may use a chapter number. Read this before resolving any chapter's neighbors (Window Rule) or doing a sequential read.
- **Unit Plans:** `bible/unit-plans.md` — per-unit targets and constraints (chapters, scenes, episodes, etc.), organized by title per the Manuscript Order above
- **Style Guide:** `bible/style-guide.md` — voice samples, sentence rhythm, POV/perspective rules
- **Soul:** `.claude/agents/soul.md` — project voice, identity, and non-negotiable values
- **Synthesis:** `notes/synthesis-current.md` — living summary of every locked decision, chapter status, and open thread. **Read this first in any new session** — it's the fast path to full context without re-reading every note file or the whole prior conversation.

## Starting a New Session
This project spans 70+ chapters — don't run the whole book in one continuous conversation. Start a fresh session per chapter (or small batch): the git branch, bible files, chapters, and notes are the persistent state, not the chat history. A new session should open by reading `notes/synthesis-current.md`, then `bible/unit-plans.md` for the next unwritten chapter's plan, then proceed. Run the Synthesis agent again at the end of each chapter (or small batch) to keep that doc current for the next session.


## Project Structure

### [Part/Section Name]
<!-- Describe each structural section, unit ranges, and length targets -->

## Agent Architecture

### Roles (third pipeline revision, 2026-09-11 — Writer reinstated with a hard narrow-context restriction)
- **Director** (`.claude/agents/agent-generic-director.md`): Orchestrates the pipeline. Does NOT write prose itself and does NOT edit chapters based on review findings. Manages the bible.
- **Writer** (`.claude/agents/agent-generic-writer.md`): Reinstated. Drafts a chapter from the author's short paragraph description. **Sees ONLY that paragraph plus the immediately previous chapter — never the rest of the book, never the bible.** This is a deliberate, hard restriction specific to this project; see that agent file's override note at the top.
- **Creative Partner** (`.claude/agents/agent-creative-partner.md`): A brainstorming/planning collaborator for working out what conversations or beats a chapter needs before the author writes its paragraph — not a drafting agent.
- **Continuity Checker** (`.claude/agents/agent-generic-continuity-checker.md`): Full sequential read, flags drift and seam problems. Findings only, never edits.
- **Story Integrity** (`.claude/agents/agent-generic-story-integrity.md`): Scores fidelity to the project's soul and style guide. Findings only, never edits.
- **Proofreader** (`.claude/agents/agent-generic-proofreader.md`): Fact-checks geography, physics, arithmetic, behavioral consistency. Runs once at the end of the manuscript, not per chapter.
- **Synthesis** (`.claude/agents/agent-generic-synthesis.md`): Distills per-unit notes into a living summary. Run periodically, not per chapter.

**Retired entirely, not just from routine use:** Normalcy, Identity Checker, Line Editor, World Builder, Tonal Calibration, Hedge Remover, Punctuation Checker. Their agent files remain on disk for reference but are not part of this project's pipeline. See `.claude/agents/agent-generic-director.md`'s Standing Rule for the full explanation.

### The Window Rule (CRITICAL — reworked, much narrower than the generic version)
- **Writer's window is deliberately tiny:** the author's paragraph for this chapter + the previous chapter's full text. Nothing else — not the bible, not a unit-plan outline, not the chapter after this one.
- Whoever reviews a chapter after it's drafted (Director, Continuity Checker) can use a wider frame — previous chapter for continuity, the chapter under review — but still doesn't need or use a full-book read for a single-chapter review.

### File Ownership
| Path              | Who Writes         | Who Reads                              |
| ----------------- | ------------------ | -------------------------------------- |
| `chapters/<title>.md` | That chapter's writer only | Director, Continuity, adjacent writers |
| `notes/*`         | Any agent          | Any agent                              |
| `bible/*`         | Director only      | All agents                             |

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
