# Author Questions

<!--
Agents log questions here when they encounter ambiguity that only the author can resolve.
The author reviews this file and adds decisions. Once decided, the Director updates
the story bible or style guide accordingly.
-->

---

<!-- Format:
### [Date] — [Agent] — [Question]
**Context:** Why this came up
**Options considered:** What the agent thinks the choices are
**Author decision:** [filled in by author]
-->

### 2026-09-02 — Author — Ch.1 deviates from unit-plans.md
**Context:** `bible/unit-plans.md` specifies Ch.1 ("Elizabeth's Morning") must include Sam's presence as caretaker and must end with Elizabeth and Sam leaving the house together. The author-supplied draft of Ch.1 covers only the alarm/fall sequence and Elizabeth getting ready — it does not include Sam or the house-leaving beat.
**Options considered:** Ask the writer to extend the chapter to hit the unit plan's beats, or accept the author's draft as-is and treat the unit plan as needing revision.
**Author decision:** Overriding the unit plan for now — using the author's draft as Chapter 1 as written. This may change; unit-plans.md has not been edited to match yet, so downstream agents should treat Ch.1 as ending after Elizabeth heads to shower, with Sam's introduction and the "leaving the house" beat deferred (either folded into Ch.1 later or pushed to Ch.2/Ch.3).

### 2026-09-02 — Director — CLAUDE.md and soul.md are unfilled templates
**Context:** `CLAUDE.md` (project overview header) and `.claude/agents/soul.md` (Core Truths, Voice, etc.) are still the blank template text, not filled in with this project's actual details.
**Options considered:** Block the pipeline until the author fills them in, or proceed using `bible/story-bible.md`, `bible/style-guide.md`, and `bible/unit-plans.md` as the working authority since those are fully written.
**Author decision:** Pending — not blocking in the meantime; both files remain author-only to edit.
