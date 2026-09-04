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

### 2026-09-03 — Author — No agent may edit Ch.1 without approval
**Context:** Author instruction, standing: no agent — Director included — may edit `chapters/ch01.md` without getting the author's explicit approval first, for that specific edit. Ch.1 is already the author's own hand-written draft, kept as-is per the 2026-09-02 override logged above; this formalizes it as a hard, permanent protection rather than a one-time note, so it can't be silently overridden later by a revision pass, a continuity finding, or a new agent that isn't aware of the original override.
**Author decision:** Locked. Added as a "Protected Files" section at the top of `bible/style-guide.md` (read before everything else), and as an explicit prohibition in `agent-generic-director.md` and `agent-generic-writer.md`. Any future issue found in Ch.1 gets reported here for author sign-off, never implemented directly.

### 2026-09-03 — Author — 1,000-word floor from Ch.6 onward, and a new Normalcy Agent
**Context:** Author wants no more sub-1,000-word chapters. This directly tensions with the existing "No Writing to a Word Count" rule and the style guide's own praise of Ch.1/Ch.3 for being short on purpose. Flagged before implementing.
**Options considered:** Apply retroactively to all short chapters, apply to Ch.6 onward only, or leave it purely forward-looking from Ch.7.
**Author decision:** Chapters 1–5 stay exactly as published — that was the introduction stage. Starting with Ch.6 (including revising the one just written), no chapter lands under 1,000 words, hit through genuine small talk/action/texture, never padding. Locked in `bible/style-guide.md` § 6. Ch.6 itself was expanded from ~650 to ~1,015 words to comply. Created a new **Normalcy Agent** (`.claude/agents/agent-generic-normalcy.md`), wired into the Director's pipeline right after the writer's draft, whose job is exactly this: find genuine small-talk/action opportunities and flag if a unit can't reach the floor without padding.

### 2026-09-03 — Author — Clarifying "no small talk" for Lucifer and "no banter" for Azrael pre-Calm
**Context:** The Normalcy Agent's mandate collides with two existing rules: "Lucifer does not do small talk" and "no banter with Azrael before Calm unlocks." Needed to know how far those restrictions extend before the new agent could be built safely.
**Author decision:** Lucifer never initiates small talk, but if anyone asks him something directly, he answers — briefly, factually, no warmth — and this applies to anyone asking, not just Elizabeth. Azrael's "doesn't volunteer" rule and the Lucifer/Azrael no-banter restriction stay fully intact between the two of them specifically — but other characters (James, Claire, town extras) can still ask Azrael things and get a real answer; he just never asks anything back. Locked in `bible/style-guide.md` § 3 (Dialogue Rules) and referenced in the Normalcy Agent's definition.

### 2026-09-03 — Author — Split the Ch.6/Ch.7 door-opening beat across both POVs
**Context:** Ch.6's unit plan had an explicit Must NOT: "The door opening — that's Ch.7," reserving the whole beat for Elizabeth's chapter. Author asked to end Ch.6 with Elizabeth opening the door and start Ch.7 with the same moment again.
**Author decision:** Implemented as a deliberate split-scene overlap — Ch.6 (Lucifer POV) now runs through the door opening and Elizabeth's first line, ending on his private, strategic read of her (including the "resemblance to Eve" beat originally slated for Ch.7, which actually fits better here since it requires his interiority and Ch.7 is strict Elizabeth POV). Ch.7 replays the same knock/door/first-line moment from her side before continuing into the rest of the scene. `bible/unit-plans.md` Ch.6 and Ch.7 updated to reflect the new split. Full breakdown in `notes/revision-ch06.md` and `notes/revision-ch07.md`.

### 2026-09-03 — Author — Narrowing the Eve resemblance to Elizabeth's eyes only
**Context:** Every existing bible reference to Elizabeth resembling Eve was generic ("the girl who resembles Eve," "she notices how closely Elizabeth resembles her") without specifying which feature. Ch.6's just-written door-opening scene had described the resemblance as unnameable/no specific feature, which now needed to be reconciled with a more specific lock-in.
**Author decision:** The resemblance is her eyes, specifically and only — personality, body, hair, and face are all different, and this is the entire reason Lucifer is drawn to her at all (the hook, not the whole attraction — everything he comes to love afterward is her own). Locked as a new section in `bible/lucifer_character_profile.md` ("The Eve Resemblance — Locked Detail"). Updated to match: `bible/story-bible.md`'s "What Lucifer Knows," the matching line in `lucifer_character_profile.md` § Lucifer & God, both instances of Eve's own reaction in `bible/unit-plans.md`, and Ch.6's door-opening passage (previously said the resemblance was "not a feature," now specifically the eyes). No conflict with the "No Explicit Physical Description" rule — the eyes are referenced as the site of recognition, never described (no color, no shape), same restriction as everything else.

### 2026-09-04 — Author — Reversed: the eye-recognition is delayed, not the initial hook
**Context:** One day after locking the above, the author scratched Ch.6's actual ending (an instant recognition of the eye-resemblance at the door), left as a note in the chapter file itself.
**Author decision:** Lucifer should get to know Elizabeth as herself over the next several chapters first — no resemblance registering at all during first contact. The eye-resemblance still exists and is still the only point of similarity to Eve, but it's now recognized later, once a real relationship already exists for the discovery to complicate, rather than being the reason he's drawn to her in the first place. Ch.6 rewritten to end clean, with no hint anything is unusual about her. `bible/lucifer_character_profile.md` § "The Eve Resemblance — Locked Detail" and `bible/unit-plans.md` Ch.6 updated to match. **Open item:** which specific later chapter carries the recognition beat has not been decided — flag to the Director before writing it whenever that chapter comes up.

### 2026-09-04 — Author — Concrete test for cutting a simile: word reuse
**Context:** Asked whether the two "like"-similes in Ch.1 (protected, author's own draft) needed fixing. Author confirmed both are fine and used the reasoning to specify an exact, checkable rule.
**Author decision:** A simile must be cut if either test fails: (1) **word reuse** — a word or root from the first half of the sentence reappears in the comparison half (e.g., "thrown... the way sand throws," "arrived... arrives when") — this is circular, explaining the thing by restating it; or (2) it's simply **obvious/cliché**, even with no word reuse. A simile that passes both tests is fine and should be left alone — the project isn't simile-free, only hedge-free and cliché-free. Ch.1's two similes ("for what seemed like an eternity," "hair splayed out like a mess of forgotten thoughts") pass both tests and stay untouched. Locked in `bible/style-guide.md` § "No Mechanism Similes," and built into the new Hedge Remover agent's detection logic (`.claude/agents/agent-generic-hedge-remover.md`).

### 2026-09-04 — Author — The porch light stays dead until an Act Three gesture
**Context:** The porch light has been an unresolved running detail since Ch.3 (burns out) and Ch.5 (Elizabeth buys the bulb but never installs it, still sitting on the porch step as of Ch.7). Author wants this to pay off specifically, not just get quietly fixed off-page.
**Author decision:** Nobody fixes the porch light until Lucifer does, in Act Three, as a deliberate romantic gesture — choosing every small, ordinary moment of a life with Elizabeth, not just the big dramatic ones. Locked as a new section in `bible/story-bible.md` § 5 ("The Porch Light," parallel to "The Ring"), and flagged as a hard continuity guard in `bible/world-bible.md`'s house entry: no chapter before the payoff may have anyone casually fix it. **Open item:** the exact chapter is not yet decided beyond "Act Three" — whoever eventually writes it must flag the Director first, since correct timing and an untouched bulb in every prior chapter are both load-bearing for the gesture to land.

### 2026-09-04 — Author — Act One closes after Ch.8, not Ch.7; Tristan always challenges Lucifer's bonds
**Context:** Flagged an internal contradiction in `bible/unit-plans.md` itself: Ch.7's entry claimed both "A Travel Bond forming" and "Act One closes," while Ch.8's entry (never touched this session, pre-existing) independently claimed the same two things at its own end. `bible/story-bible.md`'s older chapter-summary table agreed with the Ch.8 version. Ch.7 as actually written never named a completed bond, just ambiguous tension, so no prose needed to change either way — only the bookkeeping.
**Author decision:** Act One ends after Ch.8. Ch.7 plants the seed (a held look, unexplained tension Tristan reacts to) without the bond forming; Ch.8 is where it actually forms and Act One actually closes. `bible/unit-plans.md` Ch.7 and Ch.8 updated to remove the duplicate claim. Alongside this, locked a new standing rule: **Tristan challenges every one of Lucifer's bonds, every time they're truly alone together** — telepathically if a human is present (silent, per the Divine & Telepathic Speech formatting rule), aloud only when no human is around at all. This is a recurring texture beat starting with Ch.8, not just the eventual "breaking point" confrontation already planned later. Locked in `bible/tristan_azrael_character_profile.md`. Ch.8 itself gets new specific content: James and Claire split off about halfway through; Elizabeth presses with persistent questions about her "task"; Lucifer works around straight answers and gets visibly annoyed at the effort, compounded by Tristan's simultaneous telepathic pestering.

**Craft precedent discovered while writing Ch.8 (worth remembering for every future chapter):** The telepathic bond-challenge above cannot be rendered as direct italicized dialogue in a chapter whose POV isn't Lucifer's — a non-Lucifer POV character has no access to a silent exchange between two other people, so writing it out directly breaks POV discipline. First draft of Ch.8 made exactly this mistake. Fixed by converting the challenge into external tells the POV character can actually notice (a cut glance, an unreadable jaw, an unexplained pause) — the challenge still happens in-universe, the reader just doesn't get the words unless they're in Lucifer's own head that chapter. Apply this pattern to every future chapter needing this beat that isn't Lucifer's POV.
