# Writer Room Template

A reusable multi-agent writing room for Claude Code. Works across formats: novels, screenplays, audio drama, stage plays, podcasts, and more.

---

## Quick Start

1. Clone this repo
2. Fill in the bible files (see **Files to Complete** below)
3. Fill in [CLAUDE.md](CLAUDE.md) with your project details
4. Fill in [.claude/agents/soul.md](.claude/agents/soul.md) with your project's voice and identity
5. Rename the `chapters/` directory to match your format (see **Format Setup**)
6. Start writing with the Director agent

---

## Project Structure

```
├── CLAUDE.md                          # Project config — agents read this first
├── bible/
│   ├── story-bible.md                 # World, characters, timeline, themes
│   ├── style-guide.md                 # Voice, rhythm, POV rules, craft guidelines
│   └── unit-plans.md                  # Per-unit targets and constraints
├── chapters/                          # Content output directory (rename per format)
│   └── .gitkeep
├── notes/
│   └── author-questions.md            # Agent questions needing author decisions
└── .claude/
    ├── settings.json                  # Agent permissions
    └── agents/
        ├── soul.md                    # Project voice & identity
        ├── agent-generic-director.md
        ├── agent-generic-writer.md
        ├── agent-generic-comedy-pass.md
        ├── agent-generic-continuity-checker.md
        ├── agent-generic-proofreader.md
        ├── agent-generic-story-integrity.md
        └── agent-generic-synthesis.md
```

---

## Files to Complete Before Writing

These files are blank templates. Fill them in before starting your first writing cycle.

| File | Purpose | Who Reads It |
|------|---------|-------------|
| [CLAUDE.md](CLAUDE.md) | Project format, genre, structure, workflow | All agents (first file read) |
| [bible/story-bible.md](bible/story-bible.md) | World, characters, timeline, themes | All agents |
| [bible/style-guide.md](bible/style-guide.md) | Voice samples, rhythm, POV rules | All agents |
| [bible/unit-plans.md](bible/unit-plans.md) | Per-unit targets and constraints | Writers, Director, Continuity, Proofreader |
| [.claude/agents/soul.md](.claude/agents/soul.md) | Project voice, identity, values | All agents |

---

## Format Setup

The template uses generic "unit" language. Rename to match your format:

| Format | Rename `chapters/` to | Rename files to | Update `unit-plans.md` references to |
|--------|----------------------|-----------------|--------------------------------------|
| Novel | `chapters/` (keep as-is) | `ch01.md`, `ch02.md` | "Chapter 1", "Chapter 2" |
| Screenplay | `scenes/` | `sc01.md`, `sc02.md` | "Scene 1", "Scene 2" |
| Audio Drama | `episodes/` | `ep01.md`, `ep02.md` | "Episode 1", "Episode 2" |
| Podcast | `episodes/` | `ep01.md`, `ep02.md` | "Episode 1", "Episode 2" |
| Stage Play | `acts/` | `act01.md`, `act02.md` | "Act 1", "Act 2" |

After renaming, update the File Ownership table in [CLAUDE.md](CLAUDE.md) to match.

---

## Files Generated During Writing

These are created by agents as they work — do not create them manually:

| File Pattern | Created By | Purpose |
|-------------|-----------|---------|
| `notes/revision-*.md` | Director | Revision notes per unit |
| `notes/continuity-*.md` | Continuity Checker | Continuity findings per unit |
| `notes/integrity-*.md` | Story Integrity | Fidelity scores per unit |
| `notes/proofing-*.md` | Proofreader | Fact-check findings per unit |
| `notes/comedy-*.md` | Comedy Pass | Comedy notes per unit (if used) |
| `notes/from-*-to-*.md` | Writers | Handoff notes to adjacent units |
| `notes/synthesis-current.md` | Synthesis | Living summary of all notes |
| `notes/continuity-summary.md` | Continuity Checker | Full-project continuity report |
| `notes/integrity-summary.md` | Story Integrity | Full-project integrity report |
| `beats/beats_*_draft*.md` | Writers | Optional pre-write beat plans |

---

## Agent Roles

| Agent | What It Does | When to Use |
|-------|-------------|-------------|
| **Director** | Orchestrates workflow, reviews output, assigns revisions | Every project — runs the room |
| **Writer** | Writes one unit at a time | Every project — the workhorse |
| **Continuity Checker** | Sequential read for drift, timeline errors, seam problems | After units are drafted |
| **Proofreader** | Fact-checks geography, physics, arithmetic, behavior | After continuity pass |
| **Story Integrity** | Scores fidelity to soul and style guide | After continuity pass |
| **Synthesis** | Distills all notes into one living summary | After each writing cycle |
| **Comedy Pass** | Evaluates joke mechanics, escalation, character fit | Comedy projects only |

---

## Agent Customization Guide

Most agents are generic and work out of the box. Customization happens in the bible files and soul.md, not in the agents themselves. However, some agents may need edits for specific project types:

### Agents That May Need Customization

| Agent | When to Customize | What to Change |
|-------|------------------|----------------|
| [agent-generic-writer.md](.claude/agents/agent-generic-writer.md) | Format-specific craft rules | Add format-specific instructions (e.g., screenplay formatting rules, audio cue conventions) |
| [agent-generic-director.md](.claude/agents/agent-generic-director.md) | Custom workflow phases | Adjust phase definitions if your project doesn't follow the standard draft-review-revise cycle |
| [agent-generic-comedy-pass.md](.claude/agents/agent-generic-comedy-pass.md) | Comedy projects | Define your project's comedy rules in the style guide; the agent reads them from there |
| [agent-generic-synthesis.md](.claude/agents/agent-generic-synthesis.md) | Non-standard bible naming | References `bible/show-bible.md` as an alternative to `bible/story-bible.md` — verify the path matches your file |

### Agents That Should NOT Need Customization

| Agent | Why It's Already Generic |
|-------|------------------------|
| [agent-generic-continuity-checker.md](.claude/agents/agent-generic-continuity-checker.md) | Reads structure from CLAUDE.md and bible files; works across all formats |
| [agent-generic-proofreader.md](.claude/agents/agent-generic-proofreader.md) | Checks facts and consistency against bible files; format-agnostic |
| [agent-generic-story-integrity.md](.claude/agents/agent-generic-story-integrity.md) | Scores against style guide and soul.md; format-agnostic |

---

## The Window Rule

Every writer agent receives exactly three things:

1. **Unit n-1** (read only) — the preceding unit, for tone and timeline continuity
2. **Unit n** (read/write) — the unit they are writing, their ONLY writable file
3. **Unit n+1 outline** (read only) — the next unit's plan from unit-plans.md

This constraint prevents writers from making changes that conflict with adjacent units. The Director enforces this by controlling what each writer instance can access.

---

## File Ownership

| Path | Who Writes | Who Reads |
|------|-----------|-----------|
| Content units | Unit N writer only | Director, Continuity, adjacent writers |
| `notes/*` | Any agent | Any agent |
| `bible/*` | Director only | All agents |
| `CLAUDE.md` | Author only | All agents |
| `.claude/agents/soul.md` | Author only | All agents |
