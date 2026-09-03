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

### 2026-09-02 — Director — Does Azrael ever leave Earth / enter Hell?
**Context:** Ch.2's draft had Azrael physically waiting in Hell's throne room and departing for Earth together with Lucifer.
**Options considered:** Keep Azrael's Hell visit as written, or establish that he never leaves Earth.
**Author decision:** Azrael never leaves Earth — he is duty-bound to guide/absorb souls there constantly and cannot be spared even briefly. Fixed: Ch.2 now ends with Lucifer departing Hell alone (Azrael's assignment reaches him remotely, through the bond); Ch.4's orchard landing has Azrael already there waiting rather than traveling with Lucifer. Locked in `bible/story-bible.md` and `bible/tristan_azrael_character_profile.md`.

### 2026-09-02 — Director — Formatting for God's/telepathic speech
**Context:** Ch.2 introduced italics-without-quotation-marks for God's non-audible speech; needed a decision before it recurs in Ch.14, Ch.24, Ch.26, Ch.31, etc.
**Author decision:** Yes — italics without quotation marks for all divine and telepathic speech, going forward. Locked in `bible/style-guide.md` § Dialogue Rules.

### 2026-09-02 — Author — Ch.2 rewritten for urgency, overriding the original Must-NOT
**Context:** The unit plan's original Must-NOT for Ch.2 was "any emotional reaction from Lucifer to Eve's name or escape — purely procedural at this stage," and the breach was a calm after-the-fact discovery with forensic analysis.
**Author decision:** Rewrote the back half of the chapter for real urgency: Lucifer already senses it's Eve before he moves, tears through the mountain rather than using stairs, arrives as the door turns to ash, watches a portal pull Eve through and misses catching her by inches, shouts Lillith's regency orders with no analysis of the door, and is pulled through his own portal by God at the end (a new locked rule: Lucifer cannot send himself to Earth). `bible/unit-plans.md` Ch.2 (and a small note in Ch.4) rewritten to match. Full breakdown in `notes/revision-ch02.md`.

### 2026-09-02 — Director — CLAUDE.md and soul.md are unfilled templates
**Context:** `CLAUDE.md` (project overview header) and `.claude/agents/soul.md` (Core Truths, Voice, etc.) are still the blank template text, not filled in with this project's actual details.
**Options considered:** Block the pipeline until the author fills them in, or proceed using `bible/story-bible.md`, `bible/style-guide.md`, and `bible/unit-plans.md` as the working authority since those are fully written.
**Author decision:** Pending — not blocking in the meantime; both files remain author-only to edit.

### 2026-09-03 — Author — Bare dialogue-verb tags in Ch.5 ("retorted," "joked," "giggled," "laughed")
**Context:** Author's manual edit to Ch.5 added standalone tags like *Elizabeth retorted.* and *Sophie laughed.* to clarify who was speaking in a fast exchange — this conflicts with the locked Attribution Hard Rule, which requires attribution to ride on a physical action beat rather than a bare verb tag.
**Author decision:** Keep them. The verb is doing tone work, not just attribution, and the author used it deliberately after losing track of speakers. Locked as a standing exception in `bible/style-guide.md` § Attribution — Hard Rule: bare dialogue-verb tags (retorted/joked/giggled/laughed, etc.) are allowed sparingly when carrying tone in a busy exchange, not as a default replacement for action-beat attribution.
