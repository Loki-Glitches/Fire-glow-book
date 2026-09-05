> ## ⚠ STANDING BLOCKER — READ THIS FIRST, BEFORE ANYTHING ELSE (set 2026-09-05)
>
> **The author has explicitly instructed: do not write anything, do not answer any other request, do not do any other pipeline or agent work — until a full Synthesis agent run has completed.** This is not a same-day task; it holds across however many sessions or days it takes. If you are a new session and this blocker is still here, your only job right now is the Synthesis run below. Do not ask the author clarifying questions about *other* work, do not draft Chapter 11, do not spawn any other agent — the author was explicit that none of that happens until this is done.
>
> **What "done" means:** actually invoke the real Synthesis agent (`subagent_type: synthesis`), not a Director hand-summary — the author specifically wants the dedicated agent to do a full, fresh read of the *entire* project as it currently stands (every chapter in `chapters/`, every file in `bible/`, every file in `notes/`) and produce a genuinely complete `synthesis-current.md`, replacing the patched-together version below (which was built incrementally by the Director across a long session and may have redundancy or drift the agent should clean up). No other chapters or bible files should be skipped for scope — this is meant to be exhaustive, not a quick pass.
>
> **If the Synthesis agent has clarifying questions or hits a genuine ambiguity while reading:** relay them to the author directly and get an answer before proceeding — that's the one exception to "no other interaction," since it's part of finishing the Synthesis job, not a separate task.
>
> **Once the Synthesis agent's run is actually complete** (this note's replacement, or a fresh top section written by the agent itself, confirms it): delete this blocker section, and normal work (including Chapter 11) resumes.

---

# Synthesis — Current State
*Last updated after: full exhaustive Synthesis Agent run, 2026-09-05 — complete fresh read of CLAUDE.md, soul.md, every file in `bible/`, chapters 1–10 in full, every file in `notes/`, and every agent definition in `.claude/agents/`. This document supersedes and replaces the prior patched-together version in its entirety. Nothing from the prior document's history was dropped without being carried forward below or explicitly logged as superseded.*
*Previous updates: initial synthesis after Ch.9; Director self-review patch after Ch.10 (2026-09-05, pre-blocker).*

**This document is long because it is meant to be a complete substitute for re-reading the raw sources — not a teaser that sends you back to them. A new session should be able to read this file alone and start Ch.11 (once the blocker above is lifted) without opening `bible/unit-plans.md` for anything except that chapter's own entry.**

**Exception while the blocker above is active: do not proceed to Ch.11 or any other pipeline work. This document exists to make the eventual resumption cheap — it does not itself lift the blocker.**

---

## 0. How the Pipeline Currently Works (read this before assigning any unit)

The pipeline changed materially on 2026-09-05. A session that still thinks the pipeline is "writer → hedge remover → punctuation checker → ... " is working from a stale picture. Current state, per `.claude/agents/agent-generic-director.md`:

**Retired from routine use:** Hedge Remover and Punctuation Checker. Grammar/punctuation/hedge-phrase catches are now the author's own job, done by hand (including direct GitHub edits), not a pipeline step. Both agent files remain on disk for an occasional author-requested full-manuscript sweep only. Their historical `notes/hedge-pass-ch*.md` and `notes/punctuation-pass-ch*.md` files (Ch.2–10) are kept as record but are not generated going forward as a matter of course.

**Checked directly by the Director, no subagent spawned:** Lucifer/Adrian and Azrael/Tristan name correctness (though see § 9 below — an Identity Checker subagent has in practice also been run every chapter so far), mechanical line-editor rules, normalcy/texture gaps.

**Still run as real subagents:** Continuity Checker, Story Integrity, Tonal Calibration (replaces the old "Comedy Pass" — broader charter: tonal weight + emotional-ladder consistency for every unit, comedy mechanics only when a unit actually has comedic material). World Builder (now also owns the sensory rendering of supernatural effects, not just mundane world texture) — spawn when a chapter adds meaningful new physical/world detail or a supernatural effect worth cataloging; skip otherwise. Proofreader runs once, at the end of the manuscript (or a large batch), not per chapter — **this is why no `notes/proofing-ch*.md` files exist yet for any of Ch.1–10; that is expected, not a gap.**

**Current documented pipeline sequence** (`agent-generic-director.md`):
1. Writer draft
2. Normalcy Agent (small talk/action/length floor, Ch.6+)
3. Identity Checker (finds AND directly fixes Lucifer/Adrian, Azrael/Tristan mismatches)
4. Line Editor (mechanical craft: attribution, banned constructs, scene completeness)
5. World Builder (when triggered)
6. Tonal Calibration (every unit)
7. Continuity Checker
8. Story Integrity
9. Director reviews all findings, writes revision notes if needed → writer revises → re-check
10. Proofreader (end of manuscript/batch only)
11. Assemble final manuscript

**In practice, Ch.1–10 were not all run through this exact sequence** — see § 9 ("Pipeline Coverage Actually Received, Per Chapter") for the real, chapter-by-chapter record, including one live gap in Ch.10 that has not yet been closed.

---

## 1. Where the Manuscript Stands

- **Chapters 1–10 are written.** Files: `chapters/ch01.md` through `chapters/ch10.md`.
- **`chapters/ch01.md` is permanently protected.** No agent, Director included, may edit it without the author's explicit in-the-moment approval for that specific edit (`bible/style-guide.md` § "Protected Files"; `notes/author-questions.md`, 2026-09-02 and 2026-09-03). It is the author's own hand-written draft and deviates from the unit plan on purpose (no Sam, no house-leaving beat — accepted as-is, permanently).
- **Act One is closed as of the end of Ch.8** (not Ch.7 — resolved 2026-09-04). Ch.8 is where the Travel Bond between Lucifer and Elizabeth actually forms and where Elizabeth learns "Adrian" and "Tristan" are angels.
- **Ch.9 has two POV sections** separated by a scene break (`---`), both canonical: Elizabeth's original park/porch/Sam-introduction section, then a Lucifer/Azrael-POV filler scene (added 2026-09-04, author-directed) that establishes the Travel Bond's ~20-foot range mechanic. Chapter header correctly reads "Chapter 9 — Elizabeth / Lucifer."
- **Ch.10 ("Dinner") is written, Lucifer POV.** Sam has his first full sit-down meeting with Lucifer; Elizabeth protects the cover on her own initiative for the first time on-page; Lucifer makes his first unstrategic true observation (that she minimizes things to Sam) on the porch afterward — a deliberate pre-Calm "bump," not an unlock. **This chapter has an unresolved pipeline gap — see § 9.4 below before treating it as fully closed.**
- **Chapter 11 ("The Roof" — Calm unlocks) does not exist yet.** It is the next chapter to write once the blocker is lifted. Full entry: `bible/unit-plans.md`, Elizabeth POV.
- **Approximate word counts** (Ch.1–5 exempt from the floor by design — see § 8): Ch.1 short/protected (~230 words); Ch.2 ~1,095; Ch.3 short/exempt (~700); Ch.4 ~1,050–1,150 (grew slightly after the Ch.4 disclosure-reaction intensification pass); Ch.5 ~695 (exempt); Ch.6 ~1,100–1,180 (revision note is internally inconsistent between ~1,015 and ~1,180 — treat "past the 1,000 floor" as the load-bearing fact, not the exact number); Ch.7 ~1,005; Ch.8 ~2,469+ (grew further after Update 12's Azrael-discloses rework — exact final count not logged, treat as "~2,470+"); Ch.9 ~2,540 (both sections combined, per the most recent Normalcy Agent pass); Ch.10 ~1,157.
- **70+ chapters are planned in the project's own framing (CLAUDE.md, prior sessions), but `bible/unit-plans.md` as it currently exists only contains fully-outlined entries through Ch.69 ("Gone" — Lucifer's departure). Author-confirmed 2026-09-05: this is deliberate, not a gap.** See § 12.3 — the author does not want a placeholder Ch.70 outlined pre-emptively; the ending stays intentionally open past Ch.69.
- This project runs one fresh Claude Code session per chapter (or small batch) going forward — see § 13.

---

## 2. POV Assignments — Full Table, Ch.1–69

`bible/unit-plans.md` is the authoritative source for any chapter's POV; this table is a convenience mirror, current as of this synthesis. POV rebalancing has been an active, ongoing effort this project (not a one-time fix) — do not assume any chapter's POV from memory or from `bible/story-bible.md`'s older inline chapter table (§13 of that file), which only covers Ch.1–36 and has at least one already-caught staleness issue (Ch.20, synced 2026-09-04). If a future session needs a chapter's POV, check `bible/unit-plans.md`'s own per-chapter entry directly — this table is a cache, not a replacement.

| Ch | Title | POV | Notes |
|----|-------|-----|-------|
| 1 | Elizabeth's Morning | Elizabeth | Protected file. |
| 2 | Hell and the First Breach | Lucifer | |
| 3 | Normal Life Continues | Elizabeth | |
| 4 | Arrival on Earth | Lucifer | |
| 5 | Near Miss in Town | Elizabeth | |
| 6 | Convergence at Home | Lucifer | |
| 7 | First Contact and Bond | Elizabeth | |
| 8 | The Park (Act One closes) | **Lucifer** | Changed from Elizabeth, 2026-09-04 executive decision. |
| 9 | The Park, Continued | Elizabeth | (+ Lucifer/Azrael filler scene, same chapter file) |
| 10 | Dinner | **Lucifer** | Changed from Elizabeth, 2026-09-04. |
| 11 | The Roof (Calm unlocks) | Elizabeth | **Next chapter to write.** |
| 12 | The Dress | Lucifer | |
| 13 | Coffee Run | Elizabeth | |
| 14 | The Painting Class | Lucifer | |
| 15 | Getting Ready | Elizabeth | |
| 16 | The Painting (Beauty/Desire deepens) | Elizabeth | |
| 17 | The Morning After | Elizabeth | **[OPEN/BLOCKED]** — see § 12.1. |
| 18 | Overheard | Lucifer | |
| 19 | The Door | Lucifer | |
| 20 | The Apology | **Lucifer** | Story-bible's summary table was stale (said Elizabeth); synced 2026-09-04 to match unit-plans.md, which was already correct. |
| 21 | After the Apology | Elizabeth | |
| 22 | Settle the Score | Lucifer | |
| 23 | Karaoke Night (Joy unlocks) | Elizabeth | |
| 24 | The Wedding Ring (Generosity surfaces) | Lucifer | |
| 25 | Connecting Dots | Elizabeth | |
| 26 | The Rose | Lucifer | |
| 27 | The Delivery (Generosity deepens) | Elizabeth | |
| 28 | The Flower (Generosity unlocks) | Lucifer | |
| 29 | Too Nice | Elizabeth | |
| 30 | Not Yet (Love begins to stir) | Lucifer | |
| 31 | Who Are You Really | **Lucifer** | Changed from Elizabeth, 2026-09-04. |
| 32 | Q&A (Full Bond forms) | **Lucifer** | Changed from Elizabeth, 2026-09-04. |
| 33 | Rehearsal Dinner (Love deepens) | Elizabeth | |
| 34 | The Wedding (Love unlocks / Act Two closes) | Elizabeth | |
| 35 | The Watcher (Act Three opens) | Eve | Memoir-register voice, per style guide § 9. |
| 36 | Spectacular | Elizabeth | |
| 37 | Terrified | Lucifer | |
| 38 | The Square | Elizabeth | |
| 39 | The Phone (Tristan's Take) | Lucifer | |
| 40 | The Phone | Elizabeth | |
| 41 | Exhausted | Elizabeth | |
| 42 | The Orchard | Lucifer | |
| 43 | The Porch | Elizabeth | |
| 44 | Girls Day | Elizabeth | |
| 45 | Loosen Up | Lucifer | |
| 46 | Dinner | Elizabeth | |
| 47 | Informants | Lucifer | |
| 48 | Honeymoon | Elizabeth | |
| 49 | Dinner At Home | Lucifer | |
| 50 | The Couch | Elizabeth | |
| 51 | Morning | Lucifer | Elizabeth's coffee (mocha) locked here. |
| 52 | You Better Wow Me | Elizabeth | |
| 53 | Storming Out | Lucifer | |
| 54 | The Figure | Elizabeth | |
| 55 | Stone Cold | Elizabeth | |
| 56 | Clear The Crowd | Lucifer | |
| 57 | What's Going On | Lucifer | |
| 58 | The Painting Of Eve | Elizabeth | |
| 59 | I Am Lucifer | Elizabeth | |
| 60 | Coming Back | Split: Elizabeth then Lucifer | Author-flagged as the emotional peak of the book — do not underwrite. |
| 61 | Eve Took Him | Elizabeth | |
| 62 | The Letter | Lucifer | |
| 63 | The Plan | Elizabeth | Vincent named here — see `bible/story-bible.md` § 13. |
| 64 | The Storehouse | Lucifer | |
| 65 | No | Elizabeth | Bond breaks. |
| 66 | Wrath | Lucifer | |
| 67 | Old Testament | Elizabeth | |
| 68 | Wings | **Lucifer** | Changed from Elizabeth, 2026-09-04 — see craft-tension flag below. |
| 69 | Gone | Elizabeth | Currently the last outlined chapter, deliberately — see § 12.3. |

**Ch.68 craft tension (carry this forward to whoever writes it):** the non-kiss was originally designed to devastate specifically because it played out from *outside* Lucifer's head. Now his interiority is directly available to the reader. Preserve the same ambiguity deliberately — show the retreat, not the reasoning behind it. Do not let narration spell out what he's bracing for.

**Ch.17 POV resolved 2026-09-05** — stays Elizabeth POV, no restructuring; see § 12.1 for the closed-out history.

---

## 3. Locked Canon

Facts and mechanics established and confirmed across the pipeline. Treat as immutable unless a future author decision explicitly supersedes one (in which case, mark it superseded here, don't delete it).

### Bond System (full detail: `bible/bond_system_reference.md`)
- **Stage 1 (No Bond):** zero ability, ever, around an unbonded person. A forming suspicion in an unbonded human's mind dissolves automatically at distance — no dramatic intervention needed.
- **Stage 2 (Travel Bond):** unlocks *nothing* — Lucifer is a regular person, no power, no strength. Formed by genuine friendship (personality + small details known), self-initiated, no divine disclosure required. Tristan doesn't oversee formation of these.
  - **Travel Bond Range (established Ch.9 filler scene):** ~20-foot radius around a bonded human anchor (a full circle, not a line-of-sight cone — empirically tested from multiple directions in Ch.9). Exceeding 20 feet of *every* currently-active Travel-Bonded human pulls Lucifer involuntarily to Azrael's current location — violent, disorienting, always ends in a hard landing/impact, never a clean stop. Not a "bond break" — no permanent consequence, no Memory Rule trigger; use "pulled/thrown/recalled," never "broke." **Multi-anchor:** with several Travel Bonds active, Lucifer can range between any of them — the pull only fires when he's outside 20 feet of *all* of them at once, which is why this doesn't hard-lock every future scene once his town network grows. **[NARROWED 2026-09-05, per Ch.10]:** the constraint is confirmed constant/always-active whenever it's the relevant condition (not conditional/occasional) — Ch.10 shows it firing every night he visits Elizabeth, with Azrael escorting him back into range each time. Lucifer has since learned to manage it proactively (leaves early enough to clear the distance out of sight). **Still genuinely open:** whether this fades in narrative relevance once the town-wide Travel Bond network is large enough that he's rarely outside every anchor's radius at once — flag to Director if a later chapter needs that shift stated explicitly.
- **Stage 3 (Power Bond):** unlocks superhuman strength + small Hell conjuring (pulling small items through from Hell). Requires Lucifer to disclose BOTH that he's divine AND his mission (looking for someone) — both pieces required, not either alone.
- **Stage 4 (Full Anchor):** unlocks full transfiguration + all Hell mechanics. Requires all five: (1) genuine belief he is Lucifer specifically, (2) explicit agreement to see what he can do, (3) passing Tristan's formal evaluation, (4) some positive emotional connection to him, (5) no prior broken bond with him. God's approval only required when *re*-bonding after a break — not for a clean first bond.
- **What breaks a bond (personal failure, PERMANENT):** any of — explicit statement of no longer wanting it; genuine sustained hatred; misuse/idolization (Anti-Idolatry Rule). All three require sustained intent, not a momentary reaction.
- **Memory Rule on break:** the person does not lose all memory of Lucifer — they lose the *Lucifer* layer (divine truth, full history, Genesis story, everything disclosed post-Full-Anchor). What remains is *Adrian* — the person, the ordinary moments, the love itself. She loves an incomplete version of him. A broken bond can be restored to Travel Bond at most (even with God's help) — never Full Anchor again.
- **Institutional Revocation:** Tristan/God can suspend a bond directly — reversible, not the same as a break.
- **Eve's Prison Escape — Earth Routing Rule:** brute-force escape from Hell's prison auto-routes to Earth, same mechanic as CPR revival, over a longer timeframe. God (not the escape itself) controls when Eve actually arrives (delayed to Ch.35).

### Divine Mechanics / Cosmology (full detail: `bible/story-bible.md` §§2, 19-stub; `bible/lucifer_character_profile.md`; `bible/tristan_azrael_character_profile.md`)
- **Telepathic bonds exist only within the same alignment** (light-to-light, dark-to-dark) — except Lucifer, who straddles both as Hell's warden and can bond across the divide (his bond to Lillith, dark; his bond to Azrael, light). No one else can do this. Lillith and Azrael cannot bond with each other.
- **Lucifer cannot lie, in any form — no tenth-commandment exception, unlike every other angel.** He works entirely in technically-true, incomplete framing — finding the true angle that serves the same purpose as a lie would, never actually deceiving. This is mechanically why he needs Azrael as cover for cornering questions.
- **Azrael's one permitted sin is lying** ("death is a lie to life" — his function is itself an interruption of what should continue). He steps in to answer/deflect a question that would corner Lucifer into an unwanted disclosure, because he can shade an answer and Lucifer cannot. **On-page precedent: Ch.8's "We're angels" is spoken by Azrael, not Lucifer** — specifically because Lucifer answering "Who are you, really?" himself would force him toward more than he's ready to give (his no-lying constraint doesn't let a partial truth stop where he wants it to).
- **Azrael never leaves Earth, never enters Hell — not even briefly, not even for Lucifer.** His death-duty (absorbing the "idea of" every human's pain at the moment of death, universally, continuously, reduced by God's reinforcement to something that registers as a "flick") cannot be paused. Any Hell-side scene needing him reaches him remotely (bond or God), never in person.
- **Lucifer cannot transport himself between realms — only God can move him.** Locked in Ch.2's rewrite; God pulls him through a portal against his own volition at the end of Ch.2.
- **Divine/telepathic speech formatting:** *italics, without quotation marks*, for God's voice and any Lucifer↔Azrael / Lucifer↔Lillith telepathic traffic. Locked since Ch.2.
- **Aliases:** Lucifer → Adrian, Azrael → Tristan. Assigned by God at the end of Ch.2, top-down, not improvised. Used in ALL human-facing scenes without exception, spoken or narrated (see § 9 for the full, non-intuitive rule governing exactly when each name is used).
- **Tristan challenges every one of Lucifer's bonds, every time they are truly alone together — no exceptions, starting Ch.8.** "Alone" includes telepathically with an unaware human physically present (silent, per formatting rule) — aloud only with zero unaware humans present. This is permanent recurring texture, not an occasional confrontation beat (the eventual "breaking point" argument, later in the outline, is the escalation of this pattern, not its only instance).
- **The Eve resemblance is Elizabeth's eyes, and only her eyes.** Nothing else about her resembles Eve — personality, body, hair, face are all her own. **This does NOT register at first contact** (deliberately scratched from Ch.6, 2026-09-04) — recognized only later, once a real relationship already exists to complicate. **Exact chapter for this recognition beat remains [OPEN]** — see § 12.2.
- **Lucifer is not all-knowing — this is the single most-repeated correction in the project's history.** Zero abilities before any bond (see Stage 1/2 above); does not get to be right about anything he hasn't actually observed, been told, or unlocked the ability to know. Concrete banned failure modes, all previously caught and fixed in shipped chapters, listed in full in `bible/lucifer_character_profile.md` § "He Is Not All-Knowing" — worth reading before writing any Lucifer-POV chapter, not just summarizing here: (1) correctly diagnosing something mechanical he has no way of knowing (cut from Ch.6's fountain); (2) tracking conversational details with unnatural precision — "she's mentioned it four times" is wrong, "more than once" is fine (cut from Ch.8); (3) asserting a fact not yet established for him to know (cut from Ch.8 — "we're looking for someone who looks like you," which also violated the Eve-eyes rule above); (4) **worst variant — predicting a fact before it's even been established in the story itself**, not just before he'd have plausibly learned it (cut from Ch.8 — he referenced the florist's deadline two full exchanges before Claire ever mentioned it to anyone).
- **The divine language (Eve's Genesis-tongue) appears exactly once in the entire book** — at the climax (Ch.64), spoken once by Eve, to unsettle Lucifer. Lucifer's response ("You can speak English, so you better") closes the door immediately. Hard rule, no exceptions, no flashbacks, no other exchange.

### POV / Craft Mechanics
- **Telepathic dialogue can only be rendered directly (italics) in a chapter that is that character's own POV.** A non-Lucifer/non-Azrael-POV chapter has no access to a silent Lucifer↔Azrael exchange — render it as external tells only (a cut glance, a tightened jaw, "something passed between them," an unexplained pause). Ch.8 (original Elizabeth draft, later reworked) and Ch.9's Elizabeth section both demonstrate the external-tells pattern cleanly.
- **Identity-name rule (full detail and failure modes: `.claude/agents/agent-generic-identity-checker.md`) — the intuitive version is wrong.** It is NOT "alias whenever a human is in the scene." Two independent rules:
  1. **Narration** (including dialogue tags/attribution) always matches the POV character's own knowledge, regardless of who else is present. A Lucifer/Azrael-POV chapter uses "Lucifer"/"Azrael" in narration even with unaware humans fully present and talking (Ch.4's whole picnic, Ch.8, Ch.10 are the canonical evidence). An unaware-human-POV chapter (Elizabeth, pre-disclosure) uses the alias in narration even when the two angels are alone together off to the side.
  2. **Quoted dialogue** matches the speaker's own knowledge plus earshot: an unaware human always says the alias; Lucifer/Azrael speaking aloud with an unaware human in earshot use the alias too (cover); Lucifer/Azrael speaking to each other with zero unaware humans in earshot use real names aloud; telepathic speech is inaudible to humans by definition, so real names are fine there regardless of who's standing nearby (inferred, not yet directly tested on-page).
  - This has already produced two real shipped errors (Ch.9's filler-scene first draft, Ch.10's "Tristan called it evaluation") — both caught and fixed. Chapters 1–10 are all currently CLEAN per the Identity Checker's per-chapter passes (see § 9 for the chapter-by-chapter record).
- **3+ Speaker Rule (hard, stricter than general attribution):** once a scene has 3+ people physically present, a name or action beat must anchor the speaker at least every other line — never two consecutive unattributed lines. Applies going forward from 2026-09-04 and to Ch.8 specifically (Ch.4/6/7 were not retroactively swept and stay as published).
- **Word-reuse simile test:** cut any simile where a word/root from the first half reappears in the comparison half (e.g., "thrown...the way sand throws"). Second, independent test: cut if simply obvious/cliché even without word reuse. A simile passing both tests is fine — project isn't simile-free, only hedge-free/cliché-free.
- **Bare dialogue-verb tags** (retorted, joked, giggled, laughed) are a locked, standing exception to the Attribution Hard Rule — allowed sparingly when the verb carries tone in a fast/busy exchange, not a default.
- **Comma vs. question mark before a tag (locked 2026-09-04):** the mark right before the closing quote depends on that clause's own grammatical mood, never on whether more speech follows. A genuine complete question always gets a "?" even if the character keeps talking after the tag. Separate from, and not to be confused with, the Flat-Delivery Exception (below).
- **Flat-Delivery Exception:** a short, clipped, grammatically-interrogative echo delivered flat, closed with a period on purpose (e.g., "Was it.", "Which part.", "What."). **Live, unresolved contradiction found this synthesis pass — see § 12.5.**

### Continuity Threads (Locked)
- **The porch light stays dead until Lucifer fixes it, deliberately, in Act Three** — a romantic gesture (choosing the smallest, most ordinary act of care), not a repair. Exact chapter is **[OPEN]**, beyond "Act Three" — see § 12.2.
- **Ch.9's garden-reminiscence timeline:** the warm creation-era material (oceans, siblings, animals) is scoped to *before* Adam and Eve exist. Lucifer's actual wound is specifically the day he gave Eve the Tree of Knowledge and what followed — not Adam's existence (personal dislike of Adam, unrelated to the Fall) and not Eve's existence either. Neutral/dry about Adam, warm about pre-Adam/Eve creation, only the tree/betrayal event itself triggers the shutdown.
- **Genesis deflection pattern:** first instance Ch.9 ("She came later" — clean, unescalated, no pressing). Must recur and escalate through Act Two, costing Lucifer more each time as his walls come down, with its last instance in Ch.33 (right before the wedding) and its correction in Ch.34.
- **Lucifer's scanning-for-Eve motif:** heavy Ch.4 and first half of Ch.8, fades unremarked partway through Ch.9 (Azrael is the one who visibly clocks the shift). From Ch.11 onward, per the unit plan's own continuity flag, Lucifer is no longer using Elizabeth to track Eve at all — track this fade-out consistently.
- **Elizabeth's forehead bump:** introduced Ch.1, referenced Ch.3, paid off as a callback in Ch.8 (Lucifer's first non-strategic question). Thread essentially resolved/closed.
- **Ch.5's near-miss sightings** (two unrecognized men with James/Claire): intentionally subtle, confirmed closed/paid off by Ch.7/8. No further action needed.
- **Sam and Elizabeth's mutual non-disclosure:** previously bible-only background, **now live on-page as of Ch.10** — see § 5 (Character State) and § 6 (Continuity Ledger) below.

---

## 4. Hard Style Rules Checklist (do not violate)

- [ ] **1,000-word floor from Ch.6 onward** (Ch.1–5 exempt, stay as published). Hit through genuine content, never padding. If a scene genuinely can't clear it, flag to the Director rather than pad.
- [ ] **No explicit physical description** of any character, ever (no hair, eyes, build, skin, height). Only outfit and in-the-moment facial expression are fair game. This extends to the World Builder's domain too — it renders everything physical EXCEPT character bodies.
- [ ] **No hedge phrases** ("as if," "as though," "in a way," "like X" standing in for a direct claim) in narration. Dialogue is exempt — hedge phrases in a character's own speech are natural and untouched.
- [ ] **No mechanism similes** — no "the way [X] does [Y] when [Z]" explaining a mechanism via an unrelated scenario. Run the word-reuse test plus the cliché test on every simile candidate (§3 above).
- [ ] **No overwritten posture/expression/action** — state the plain beat, don't add a clause explaining what it means.
- [ ] **Attribution Hard Rule:** no standalone "he said/she said" unless necessary; prefer action-beat attribution. **3+ Speaker Rule** is stricter — anchor the speaker at least every other line once 3+ people are present.
- [ ] **Divine & Telepathic Speech formatting:** italics, no quotation marks. Only directly renderable in that character's own POV chapter.
- [ ] **No banter between Lucifer and Azrael before Calm unlocks** (Ch.11). One pushback at most, then disengage — brooding, not witty. Azrael's annoyance can show physically (tight jaw, flat voice) but stays unremarked-on by both. Restriction is specific to the two of them; other characters can still get real (if brief, unprompted-by-him) answers from either.
- [ ] **Lucifer never initiates small talk, but always answers if asked directly** — briefly, factually, no warmth pre-Calm — by anyone, not just Elizabeth.
- [ ] **"He is not all-knowing"** — check every factual assertion against what's actually established on-page by that point (see § 3 above for the four concrete failure modes already caught).
- [ ] **Azrael's permitted sin is lying** — the mechanic to reach for whenever a scene needs Lucifer protected from an unwanted disclosure.
- [ ] **No smile from Lucifer before Ch.11** (the roof scene — his first real, unguarded smile, eyes closed). Ch.9 uses "not quite a smile" and Ch.10's near-laugh ("A short breath went through him — not quite a laugh") both stop short deliberately — don't cross the line early.
- [ ] **The sky-glance — no fixed cap as of 2026-09-04.** Recurring beat, genuine annoyance (not shared amusement) — Lucifer is irritated God is making a joke of the timing at all, especially in a serious/crisis moment. Comedy is for the reader only. Stays Lucifer-exclusive (never shared/noticed by another character); each instance must be a specific, earned reaction to a specific too-convenient thing, never a tic. **Used so far:** Ch.4 (orchard landing), Ch.9 filler scene (right after the first involuntary pull to Azrael). **Live craft flag from Story Integrity (Ch.9):** that second use was scored as a slightly weaker instance of the device — a reaction to generic physical pain from a newly-discovered bond glitch, not a clearly legible "God's joke" — worth protecting the device's precision more carefully in future instances now that its cap is lifted.
- [ ] **The divine language appears exactly once in the entire book** — climax only, Eve only. No exceptions.
- [ ] **Eve is not on Earth at all until Ch.35** (Act Three opener). Do not manufacture tension from her direction, however passively, before then.
- [ ] **No word-count writing-to-a-target** — length is a byproduct of covering what's needed, never a goal (applies both directions).
- [ ] **Every chapter does two things:** introduces or changes a character AND advances plot. "Breathing chapter" labels affect scale/tone only, never waive these two requirements.
- [ ] **Scene Completeness:** props/errands/destinations a scene's premise implies must actually be shown, not left vague or skipped to the aftermath. Attribution in busy/3+ scenes must be unambiguous as written.

---

## 5. Character State as of End of Ch.10

- **Lucifer/"Adrian":** Still in the **Numbness phase** — no emotion has unlocked (Calm is Ch.11). Procedural, flat, monosyllabic by default, but showing the first cracks: asked Elizabeth an unstrategic question (the forehead bump, Ch.8), and in Ch.10 volunteered an unstrategic true *observation* to her for the first time (that she minimizes things to Sam) — offered nothing to his function, cost him something small, and he said it anyway. His effort to maintain technically-true evasions is visibly costing him (annoyance at the *position*, never at her) — Sam's "what do you actually do all day" nearly cornered him in Ch.10 and he had to recalibrate. Stopped actively scanning for Eve as of partway through Ch.9 (unremarked shift). Has now: (a) formed a Travel Bond with Elizabeth (Ch.8, unnamed on page), (b) disclosed via Azrael's line that he and Tristan are angels (Ch.8), (c) shared warm, real memories of pre-Adam/Eve creation with her (Ch.9), then shut down completely the instant Eve came up ("She came later" — unescalated so far), (d) met Sam twice — the brief doorstep meeting (Ch.9) and a full sit-down dinner (Ch.10), where he watched the sibling dynamic closely and clocked the "performance of fine" both Sam and Elizabeth run on each other, (e) discovered (Ch.9 filler scene) and is now managing proactively (Ch.10) the Travel Bond's ~20-foot range constraint — leaves early enough each night to clear the distance out of Elizabeth's/Sam's sight before the pull can trigger visibly.
- **Elizabeth:** Knows: Adrian and Tristan are angels (told end of Ch.8). Knows they're looking for an unnamed, undescribed young woman (does not know it's Eve, no name for the target). Does NOT know: Lucifer's real identity, Tristan's real identity (Azrael), the Genesis backstory beyond the pre-Adam/Eve warmth, anything about bond mechanics/tiers, or that a Travel Bond formed with her specifically. Has a Travel Bond with Lucifer (Ch.8) — no visible change for her. Has been filing away small unexplained things all along (Tristan's unreadable stillness/tells, Lucifer's evasions) without pressing — consistent with her established "notice, don't chase" pattern. **New in Ch.10:** protected Lucifer's cover with Sam on her own initiative, unprompted, for the first time on-page (deflected a question getting too close: "It's a family thing... complicated. Long story, boring in the middle"). Also new: when Lucifer named her habit of minimizing things to Sam, she didn't deny it and gave a small honest admission ("It's easier this way... He worries enough already") — the first on-page dramatization of the Sam/Elizabeth mutual-non-disclosure thread (previously bible-only).
- **Sam:** Has now met "Adrian" twice — the brief doorstep meeting (Ch.9) and a full dinner (Ch.10). His skepticism has real texture: precise, protective, unconvinced but not confrontational. Tested Lucifer directly ("what do you actually do all day") and let the deflection go without pushing further. Also caught, and let go of, Elizabeth downplaying how she's doing ("I'm good, Sam") — consistent with his profile (catches the edge of things, puts them down, too stretched thin to pursue).
- **Azrael/"Tristan":** Granted Elizabeth's Travel Bond (Ch.8, his own procedural decision after watching Lucifer listen to her). Has begun the standing "challenge every bond" pattern (visible in Ch.8's telepathic exchanges, now renderable directly since Ch.8 became Lucifer's own POV). No banter with Lucifer yet (pre-Calm restriction fully intact through Ch.10 — Story Integrity flagged the Ch.9 filler scene's dry one-liners as leaning slightly more verbal than the style guide's "shows physically" language technically describes, though the one-sidedness rule itself — never traded back — was honored; worth watching in future filler-style scenes so Azrael doesn't drift into being "the funny one" by default). Did not appear on-page in Ch.10 — referenced only ("Tristan's waiting?" / "Something like that," a small dramatic-irony beat mirroring Elizabeth's own deflection with Sam moments earlier). Discovered the Travel Bond range mechanic alongside Lucifer in Ch.9 and has been escorting him back into range nightly since (Ch.10), visibly more annoyed each time, unremarked-on by either.
- **Sophie, James, Claire:** Sophie has not appeared since Ch.5 (near-miss) — not yet properly introduced to Lucifer/Tristan (Ch.13–14 territory). James and Claire are engaged (proposed Ch.4) and hold Power Bonds (know he's divine + his mission) as of Ch.4; Elizabeth learned of their engagement in Ch.7.
- **Eve:** Not on Earth. Escaped Hell's prison in Ch.2; God is holding her in transit so she doesn't arrive until Ch.35 (Act Three opener). No activity from her anywhere in Ch.1–10.

---

## 6. Continuity Ledger (Objects, Locations, Threads to Track Forward)

| Item | Established | Current State | Last Referenced |
|------|------------|----------------|------------------|
| Porch light / dead bulb | Ch.3 (burns out), Ch.5 (bulb bought, never installed) | Still dead, bulb still unused in its **cardboard** sleeve on the porch step. Locked to stay this way until an [OPEN] Act Three chapter — Lucifer fixes it as a deliberate small-gesture romantic beat. No chapter before that payoff may have anyone casually fix it. | Ch.10 (referenced once, briefly, untouched) |
| Sam/Elizabeth mutual non-disclosure | Bible-only until Ch.10 | Now live on-page: Ch.10 porch scene ("It's easier this way"). Future chapters can build on this rather than starting cold; Sam's off-page arc eventually has Tristan seek him out to evaluate the relationship through the person who knows Elizabeth best — this Ch.10 beat is a natural seed, not a resolution. | Ch.10 |
| James's ring / wedding planning | Ring repaired Ch.4 (Power Bond disclosure moment) | Wedding: **August 2nd, the town park** (Ch.27 in the outline — not yet reached in written chapters). Wedding ring commissioned from Lillith Ch.24, delivered via rose-through-Hell-mechanics Ch.26, physically handed to James Ch.27. None of this has happened on-page yet as of Ch.10 — nothing to track yet in written material, just noting it's coming and exactly where. | N/A yet |
| Genesis deflection pattern | Ch.9 ("She came later") | First instance only, clean and unescalated. Must recur/escalate through Act Two; last instance Ch.33, corrected Ch.34. | Ch.9 |
| Scanning-for-Eve motif | Heavy Ch.4/early Ch.8 | Faded, unremarked, partway through Ch.9. Per Ch.11's own continuity flag, should read as fully gone from Ch.11 onward. | Ch.9 |
| Elizabeth's forehead bump | Ch.1 | Closed/resolved — paid off Ch.8. No further tracking needed unless a much later chapter wants a deliberate callback. | Ch.8 |
| Ch.5 near-miss sightings | Ch.5 | Closed/paid off by Ch.7/8. No further action needed. | Ch.7/8 |
| Sam's dish towel | Ch.9 (door), Ch.10 (stove/whole meal) | Small recurring visual anchor for "Sam mid-cooking." Keep present/consistent in future kitchen/dinner scenes he cooks. | Ch.10 |
| Street geography outside Elizabeth's house | Ch.9 filler scene | Mailbox at end of walk, fire hydrant two houses down, neighbor's fence w/ audible gate, a dog two yards over (settles once repetition stops surprising it). Reusable geography for future exterior-house scenes. | Ch.9 |
| Postcard on the fridge (absent parents) | Ch.3 | Ch.10 added: corners now soft from being taken down/put back repeatedly. Additive, not contradictory. A load-bearing quiet-grief detail — do not resolve/explain it, just let it keep accumulating wear. | Ch.10 |
| Kitchen counter/stools | Ch.10 | Built to seat two (Elizabeth + Sam); spares stored underneath, pulled out for a guest — three crowded in for Lucifer's first dinner. | Ch.10 |
| Eve-eyes recognition beat | [OPEN] | See § 12.2. | — |
| Vincent (Travel Bond acquaintance) | Named/detailed in `bible/story-bible.md` §13 | Activated on-page much later (Ch.63). No action needed until then; treat with the dignity the bible specifies (not "expendable," just free of anyone who'd be put at risk or grieve him). | — |
| Sky-glance uses so far | Ch.4, Ch.9 filler | Uncapped as of 2026-09-04, but each instance should still be a specific, earned "God's joke" reaction — see the live Story Integrity flag on the Ch.9 instance in § 3/§4 above. | Ch.9 |

---

## 7. Open Author Questions (Director loads this before assigning new units)

All resolved decisions live in full in `notes/author-questions.md`; this section surfaces only what's still genuinely open, plus a pointer to anything a future writer must actively flag before proceeding.

- [ ] **Eve-eyes recognition — which chapter?** Not decided beyond "later, once a relationship already exists." *Blocking: no* (not needed until well past Ch.11). Whoever writes the chapter that surfaces this must flag the Director first.
- [ ] **Porch light Act Three fix — which chapter?** Not decided beyond "Act Three." *Blocking: no* (Act Three doesn't start until Ch.35). Flag the Director before drafting whichever chapter carries it — depends on precise timing and an untouched bulb in every prior chapter.
- [x] **Ch.17 POV — RESOLVED 2026-09-05.** Ch.17 is a Sam/Sophie/Elizabeth-only household scene with zero Lucifer presence in its Must Include list — mechanically impossible to convert to his POV without fabricating his presence or restructuring the chapter. Author confirmed this chapter was never actually part of the POV-rebalancing ask: it stays Elizabeth POV, no content changes, no restructuring. Accepted as the one exception to the broader rebalancing effort. No further flag needed when Ch.17 is eventually drafted.
- [ ] **Travel Bond range's long-term relevance** — confirmed constant/always-active as of Ch.10, but whether it fades once Lucifer's town-wide network is large is still open. *Blocking: no.* Flag the Director if a later chapter needs that transition stated explicitly.
- [x] **CLAUDE.md / soul.md unfilled templates** — **partially resolved, worth re-flagging.** `soul.md` has since been fully written (this synthesis read it in full — it is the real, populated project soul document). **`CLAUDE.md` remains the unfilled generic template as of this synthesis** — confirmed by direct read: the Project Overview section still literally reads `**Format:** <!-- Novel | Screenplay | ... -->`, `**Genre:**`, etc., with no project-specific content anywhere in the file. Since a new session's own onboarding instructions (inside `CLAUDE.md` itself) tell it to read `CLAUDE.md` first, a fresh session currently gets zero project-specific orientation from the one document designed to provide it — everything actually useful lives in `bible/story-bible.md`, `bible/style-guide.md`, and this synthesis file instead. *Blocking: no, by original author decision (2026-09-02) — CLAUDE.md is author-only to edit and the project has functioned without it being filled in.* Still worth surfacing again since a full year/many chapters into the project, the gap is now more consequential than it was at the time of the original decision. See § 12.4 for the exact discrepancy.
- [ ] **`bible/story-bible.md` § 19 ("Divine Nature — Purity, Truth & the Commandment System") is a header with no content underneath it — the file ends immediately after that heading.** See § 12.6. *Blocking: no* — the substantive content this section's title promises (purity/truth mechanics, the commandment system) already exists in full in `bible/lucifer_character_profile.md` § "Divine Purity & Truth" and `bible/tristan_azrael_character_profile.md` § "Permitted Sin — Lying," so nothing is actually missing from the *bible as a whole* — just from this one file's own structure. Worth a cleanup pass (either fill the section in with a cross-reference, or delete the dangling header) but not urgent.
- [ ] **`bible/unit-plans.md`'s own file structure has a duplication artifact across all of Act Three** — see § 12.7. *Blocking: no* — content is consistent between the duplicated passes everywhere spot-checked, but the file should be cleaned up before it's used as a hand-off document to a writer who might get confused reading it top-to-bottom rather than jumping to a specific chapter.
- [x] **Whether a Ch.70+ epilogue exists for Lillith's sequel-hook contact — RESOLVED 2026-09-05.** Author's explicit call: leave it unknown/open on purpose. No placeholder chapter gets outlined ahead of time. This keeps the ending malleable and avoids an artificial cap — if something later needs a chapter to happen in, one gets added then, without having to un-plan a placeholder first. See § 12.3.
- [ ] **Flat-Delivery Exception contradiction on one specific Ch.9 line** — see § 12.5. *Blocking: no* (cosmetic, one line), but it's a real, live contradiction between an agent definition file's hardcoded canonical example and the actual shipped chapter text, worth a deliberate one-line resolution rather than leaving it to drift.
- [ ] **Ch.10's Line Editor attribution findings were not fully implemented** — see § 9.4/§12.8. *Blocking: recommend yes*, in the narrow sense that Ch.10 should not be treated as "fully passed" until the Director either implements or explicitly waives these four findings — the old synthesis document already flagged Ch.10 as pipeline-incomplete for a different reason (self-review vs. full pipeline); this is the same underlying gap, now specifically identified.

---

## 8. Soul Flags (Patterns Noticed Across Multiple Units — Not Per-Unit Findings)

- **Tonal breadth expanding faster than the norm-setting has caught up to.** The Ch.9 filler scene's repeated-pratfall sequence was flagged by its own Story Integrity pass as "the most tonally broad beat in the manuscript so far" — comedically successful and correctly escalating (mailbox → hydrant → across the street → parked car, each step adding new information rather than just volume), and it stays inside the project's soul because the delivery itself stays dry/procedural rather than narrated for laughs. But it's a genuine widening of the book's register (toward overt physical comedy) relative to the drier, conversational comedy established elsewhere (James/Claire's banter). *First noted Ch.9. Worth watching if a second scene in this register appears — that would be the point to decide deliberately whether physical farce is now a standing tool in the kit or a one-off.*
- **Azrael's pre-Calm restraint is holding on the letter of the rule (never trades wit back) but drifting slightly on its spirit (the style guide describes his annoyance as primarily physical — a tightened jaw, a flattened voice — and it has twice now shown up instead as dry verbal one-liners).** *First noted Ch.4 (self-caught and corrected in that chapter's own revision pass), recurred as a softer note in Ch.9's Story Integrity review.* Not a violation either time — but a pattern worth the Director's attention before it hardens into "Azrael's dry one-liner" as his default pre-Calm voice, which would blur the one-sidedness the no-banter rule is actually protecting.
- **Self-review vs. independent pipeline coverage has been uneven across the ten written chapters**, and that unevenness is exactly what produced the one real outstanding gap in this manuscript (Ch.10 — see § 9.4). *Noted once, directly, rather than repeated across findings*, since it's a process pattern rather than a prose pattern: the Director wrote and self-reviewed several early chapters directly before dedicated writer sub-agents became the norm starting Ch.9, and Ch.10 in particular was drafted and self-reviewed by the Director rather than by a writer sub-agent, then run through most-but-not-all of the review pipeline after the fact rather than before. The current Standing Rule in `agent-generic-director.md` (revised 2026-09-05) formalizes a leaner but still-real pipeline going forward; the risk this flag names is specifically about *retroactively* verifying that leftover gaps from the earlier, less consistent period get closed, not about the new process itself.

---

## 9. Pipeline Coverage Actually Received, Per Chapter (Ch.1–10)

This section exists because the file-presence pattern in `notes/` is uneven across chapters, and a future session needs to know what that unevenness means rather than assume every chapter got the same treatment.

- **Ch.1:** Protected, author's own draft. No pipeline review of any kind, by design — this is a hard exception, not a gap.
- **Ch.2:** Director self-review only (`revision-ch02.md`, multiple same-day rounds) + a Hedge Remover pass (`hedge-pass-ch02.md`) + a Punctuation Checker pass (`punctuation-pass-ch02.md`, clean). No Identity Checker pass exists as a separate file, but `identity-pass-ch02.md` does exist and reports CLEAN. No Continuity Checker, Story Integrity, Line Editor, World Builder, Normalcy, or Tonal Calibration pass exists for this chapter specifically — it predates most of those agents' creation this session. Treat as **passed by author-era standards at the time**, not by the current, fuller pipeline.
- **Ch.3:** Director self-review implied (no `revision-ch03.md` exists — likely reviewed together with Ch.2/Ch.4 and needed no changes). `punctuation-pass-ch03.md` (clean) and `identity-pass-ch03.md` (clean, no relevant names appear) exist. No other agent passes exist.
- **Ch.4:** `revision-ch04.md` (Director self-review, several author-directed changes, later a disclosure-intensity update), `hedge-pass-ch04.md`, `punctuation-pass-ch04.md`, `identity-pass-ch04.md` (clean — this chapter is the canonical evidence example for the identity rule's Rule 1). No Continuity/Integrity/Line Editor/World Builder/Normalcy/Tonal passes.
- **Ch.5:** `revision-ch05.md`, `punctuation-pass-ch05.md`, `identity-pass-ch05.md` (clean, no relevant names appear). No other agent passes.
- **Ch.6:** `revision-ch06.md` (extensive, multiple same-day author-directed reversals on the Eve-resemblance beat), `punctuation-pass-ch06.md` (clean), `identity-pass-ch06.md` (2 real fixes made — narration using "Tristan" instead of "Azrael"). No Continuity/Integrity/Line Editor/World Builder/Normalcy/Tonal passes.
- **Ch.7:** `revision-ch07.md`, `punctuation-pass-ch07.md` (2 fixes), `identity-pass-ch07.md` (clean). No other agent passes.
- **Ch.8:** `revision-ch08.md` (the largest revision file in the project — 12 numbered same-day update rounds, including the full Elizabeth→Lucifer POV rework and the Azrael-discloses-instead-of-Lucifer change), `punctuation-pass-ch08.md` (6 fixes), `identity-pass-ch08.md` (clean). **This is the first chapter with genuinely deep, iterative revision — treat its revision note as a case study in what "caught late" looks like (the James-already-knows-the-story logic error, the omniscience violations) more than as a template for how much churn to expect going forward.** No Continuity/Integrity/Line Editor/World Builder/Normalcy/Tonal passes exist for Ch.8 specifically — it was fully vetted through the Director's own self-review plus the two narrow single-purpose agents active at the time, not the fuller pipeline that exists now.
- **Ch.9:** The first chapter drafted by a dedicated writer sub-agent rather than Director self-review (`revision-ch09.md`). Received the fullest pipeline coverage of any chapter to date: `hedge-pass-ch09.md` (2 fixes), `identity-pass-ch09.md` (clean, verified across both POV sections), `world-notes-09.md` (suggestions — flagged then-current "plastic sleeve" vs. locked "cardboard sleeve," since resolved back to cardboard), `normalcy-09.md` (one suggestion, implemented — the porch-light-clicking neighbor beat), `integrity-ch09.md` (86/100, PASS, with the sky-glance precision flag and chapter-header flag both noted and both since fixed), `line-edit-ch09.md` (several attribution/punctuation findings — **see below, mostly but not entirely resolved**), `continuity-ch09.md` (issues found, all addressed same session per its own status line), `punctuation-pass-ch09.md` (clean, with the Flat-Delivery contradiction noted in § 12.5). **Verified during this synthesis:** the hedge fixes, the normalcy suggestion, the chapter-header fix, and the "cardboard sleeve" correction are all present in the current shipped file text. The line-edit's flagged question-mark fix ("or is that also a version of an answer?") is also present in the current text — but this directly contradicts the punctuation-checker agent's own hardcoded canonical example, which still cites that exact line as an intentional period. **This is the one live, unresolved documentation-vs-text contradiction in the project — see § 12.5.**
- **Ch.10:** Drafted and self-reviewed directly by the Director (no writer sub-agent), per the prior synthesis document's own process note. No `revision-ch10.md` exists. Subsequently run through: `hedge-pass-ch10.md` (1 fix, applied), `punctuation-pass-ch10.md` (1 fix, applied), `identity-pass-ch10.md` (clean), `world-notes-10.md` (no issues, catalog additions only), `normalcy-10.md` (one suggestion — the "oregano/basil" small-talk beat — **verified present in the current shipped text**, so this was implemented), `integrity-ch10.md` (92/100, PASS, with one open craft note about a compressed-time-summary opening reading slightly like a montage — advisory only, not required), `continuity-ch10.md` (issues found and addressed, per its own status line — the bond-range "always vs. conditional" resolution and the "leaves early to avoid a second near-miss" line), and `line-edit-ch10.md` (**4 findings — 2 confirmed fixed on direct re-read of the current chapter text; 2 attribution findings NOT fixed as of this synthesis's direct read of `chapters/ch10.md`**). **§ 12.8 below has the specific unresolved lines.** No `revision-ch10.md` was ever written to consolidate these fixes or explicitly waive the remainder, which is itself the gap: unlike every other chapter 2–9, Ch.10 has no single document confirming the Director actually closed the loop on its own pipeline's findings.

**Net read for a new session:** Ch.1–9 can be treated as fully closed out per the standards that were active at the time each was written. **Ch.10 cannot yet be treated as fully closed — it has two specific, still-open Line Editor findings (§ 12.8) that should be resolved (fixed or explicitly waived by the Director/author) before or alongside Ch.11's drafting**, since Ch.11 will read Ch.10 as its n-1 unit under the Window Rule.

---

## 10. What's Locked vs. In Motion vs. Unresolved

**Locked (do not contradict):**
- Everything in § 3 (Locked Canon) and § 4 (Hard Style Rules Checklist).
- Ch.1 is permanently protected and stays exactly as published.
- Act One ends at Ch.8, not Ch.7.
- POV table in § 2, as currently synced to `bible/unit-plans.md`.
- Character states as of end of Ch.10, § 5.

**In Motion (check before writing):**
- Genesis deflection escalation (next instance due sometime in Act Two, must feel costlier than Ch.9's).
- Scanning-for-Eve fade-out (should read as fully gone from Ch.11 on).
- Sam/Elizabeth mutual non-disclosure thread (now live, building toward Tristan's off-page conversation with Sam later in the outline).
- Travel Bond range mechanic (constant/active per Ch.10, long-term relevance still open per § 7).
- Sky-glance precision (uncapped, but each use should be an earned, legible "God's joke" — the Ch.9 instance is the softer precedent to improve on, not repeat).

**Resolved 2026-09-05 (all closed same day the Synthesis run surfaced them):** Ch.10's two Line Editor attribution findings (fixed directly), the Flat-Delivery Exception contradiction on the Ch.9 "or is that also a version of an answer" line (agent file corrected), Ch.17's POV (confirmed staying Elizabeth POV, no restructuring — see § 12.1), and the Ch.70+ Lillith-epilogue question (author's explicit call: leave it open/unknown on purpose, no placeholder chapter — see § 12.3).

**Still unresolved (needs author decision before proceeding, in priority order for how soon they'll actually bite):**
1. Eve-eyes recognition chapter placement.
2. Porch light Act Three chapter placement.
3. `bible/story-bible.md` § 19's empty header and `bible/unit-plans.md`'s Act Three duplication — both cosmetic cleanup, no urgency.
4. CLAUDE.md remaining an unfilled template — long-standing, non-blocking, but flagged again given how much more consequential the gap now is than when first raised.

---

## 11. Process Notes for a New Session

- **Director** orchestrates and reviews; does not write chapters itself. Per the Standing Rule locked 2026-09-05 in `agent-generic-director.md`: Hedge Remover and Punctuation Checker are retired from routine use (author does this by hand now); Identity Checker, Line Editor, Tonal Calibration, Continuity Checker, and Story Integrity are still real pipeline steps (some director-direct, some subagent, per § 0 above); World Builder is triggered conditionally; Proofreader runs once at the very end, not per chapter.
- **Writer sub-agents** draft one chapter at a time under the Window Rule: unit n-1 (read-only), unit n (read/write, their only writable file), unit n+1's outline (read-only) — never the full manuscript.
- **Before assigning Ch.11:** resolve or explicitly waive Ch.10's two remaining Line Editor findings (§ 12.8) first, since Ch.11's writer will read Ch.10 as-is for continuity of tone.
- **Keep revision notes terse** — 1–2 sentences per change is the target. Ch.8's revision note (12 numbered updates) is a historical record of a genuinely difficult chapter, not the pattern to replicate.
- **Commit and push after meaningful changes.** Trust the local git push as source of truth.
- **Run the Synthesis agent again after each future chapter (or small batch)** to keep this document current. Given how much cheaper a fresh session became once this exhaustive version existed, a lighter incremental update (not a full re-read of every bible/chapter/notes file) should suffice for most future runs — reserve another full exhaustive pass for a moment when the author again suspects real drift has accumulated.
- When a chapter's writer/reviewer discovers an ambiguity only the author can resolve, log it to `notes/author-questions.md` (context, options, space for the decision) rather than guessing.
- Two supporting per-chapter note types remain fine to keep producing: handoff notes (`from-NN-to-MM.md`) and, if the author ever requests a one-off sweep, hedge-pass/punctuation-pass notes (otherwise retired from routine use).

---

## 12. Ambiguities, Gaps, and Contradictions Found During This Synthesis Pass

*Everything in this section is also cross-referenced from § 7 and § 10 above where it affects a live decision. This section exists as the single consolidated list the Director should relay to the author, per this session's explicit instructions — none of these block Ch.11 in the narrow sense of "the next chapter cannot be written," except where marked.*

### 12.1 Ch.17 POV — RESOLVED 2026-09-05
Every other POV rebalancing this session resolved as either "already correct, just sync the table" or "swap it, content unaffected." Ch.17 couldn't resolve that way: it has zero Lucifer presence in its Must Include list by design (a Sam/Sophie/Elizabeth household argument while he isn't there) — mechanically impossible to convert without fabricating his presence or restructuring the chapter. **Author confirmed directly: Ch.17 was never actually part of the POV-rebalancing ask.** It stays Elizabeth POV, no content changes, no restructuring — the one accepted exception to the broader rebalancing effort. Nothing further to flag when Ch.17 is eventually drafted.

### 12.2 Two placement decisions left open since early September, still open
The Eve-eyes recognition beat and the porch-light Act Three fix were both deliberately left unplaced pending "the right chapter." Neither is remotely due yet (Ch.11 is next; these are Act Two/Three items), but both require the same kind of care when their moment comes — flagging again here only so a future session scanning this document doesn't assume they were quietly decided somewhere in the meantime. They weren't.

### 12.3 `bible/unit-plans.md` has no chapter past Ch.69 — RESOLVED 2026-09-05, deliberate
`CLAUDE.md` and this project's own prior synthesis documents describe "70+ chapters planned total." A full read of `bible/unit-plans.md` (all 2,410 lines, confirmed via direct read plus a targeted search for "Ch.70," "Epilogue," "Book Two," and "sequel hook") turns up nothing past Ch.69 ("Gone" — Lucifer's departure, ending on Tristan's line to Elizabeth about having saved his life). Meanwhile, `bible/story-bible.md` § 12 (Lillith) and `bible/lillith_character_profile.md` both describe a specific, load-bearing beat: Lillith contacting Lucifer via their telepathic bond "at the very end of the book" about a new Hell crisis, explicitly framed as "the sequel hook." There is currently no chapter in the outline where this happens.

**Author's explicit decision:** leave this unknown, on purpose. No Ch.70 or epilogue gets pre-emptively outlined. Two reasons given: (1) the author dislikes placeholder chapters and doesn't want the ending pinned down before it needs to be, and (2) leaving it open avoids an artificial cap — if something needs to happen after Ch.69 later, a chapter can be added then without first having to un-plan a placeholder. Treat "the book currently ends at Ch.69, with the Lillith beat's exact placement (inside Ch.69 or a later addition) still open" as the stable, intentional state — not a gap to keep re-flagging.

### 12.4 CLAUDE.md vs. soul.md — one got filled in, the other didn't
Direct read confirms `.claude/agents/soul.md` is fully populated with real, specific project content (this is the document quoted throughout this synthesis and the rest of the bible). `CLAUDE.md`, by contrast, is still the literal unfilled template — every bracketed placeholder (`**Format:** <!-- Novel | Screenplay... -->`, `**Genre:**`, `**Setting:**`, the entire "Project Structure," "Voice," "Pacing by Section," "What This Project Is NOT," and "Workflow" sections) remains exactly as generated, with zero project-specific text anywhere in the file except the two paragraphs about the standing blocker and the synthesis-first instruction that were added later. The original 2026-09-02 author decision on this ("Pending — not blocking... both files remain author-only to edit") predates most of the project's actual content existing. Given `CLAUDE.md` is the document every agent (writer, Director, and this Synthesis agent itself) is instructed to read *first*, and it currently provides no actual project orientation, this gap is more consequential now than it was when first logged. Not blocking Ch.11, but worth a fresh look given how much has been built since the original "pending" call.

### 12.5 A hardcoded canonical example in an agent definition file no longer matches the manuscript
`.claude/agents/agent-generic-punctuation-checker.md` § "The Flat-Delivery Exception" explicitly lists, as one of only two canonical examples of the project's intentional flat-delivery voice device: `"Is he actually going somewhere, or is that also a version of an answer."` (Ch.9 — Elizabeth). A direct read of the current `chapters/ch09.md` shows this exact line now ends with a question mark: `"Is he actually going somewhere, or is that also a version of an answer?"`. This fix traces to `notes/line-edit-ch09.md`, which independently judged the same line as a genuine mismatch requiring a question mark, explicitly disagreeing with the flat-delivery reading (its own words: "it doesn't qualify for the separate Flat-Delivery Exception... it's a full, original interrogative sentence, not a short deadpan echo"). Both agents did their jobs correctly by their own stated logic; they simply reached opposite conclusions about the same line, and the Line Editor's fix is the one that's actually in the manuscript now. This leaves the Punctuation Checker's own definition file citing a "canonical example" that the shipped text has since overridden. This needs one deliberate resolution — either revert the line to a period and update `line-edit-ch09.md`'s finding as overruled, or leave the question mark and update the agent definition file's example list — rather than being left to silently drift further any time either agent is run again in a future full-manuscript sweep.

### 12.6 `bible/story-bible.md` ends mid-structure
The file's final line is a bare section header — `## 19. DIVINE NATURE — PURITY, TRUTH & THE COMMANDMENT SYSTEM` — with the file terminating immediately after it, zero content underneath. This is not a missing-information problem (the actual material — Lucifer's absolute purity/no-lying constraint, the nine-of-ten-commandments system, Azrael's specific tenth-commandment exception — is fully and correctly documented in `bible/lucifer_character_profile.md` § "Divine Purity & Truth" and `bible/tristan_azrael_character_profile.md` § "Permitted Sin — Lying," both of which this synthesis draws on directly in § 3 above). It is a structural loose end in one specific file: either this section should be filled with the actual content (consolidating what's currently split across two character-profile files) or the dangling header should be deleted so the file doesn't read as unfinished. Purely a housekeeping item, zero effect on any locked decision.

### 12.7 `bible/unit-plans.md` contains a large duplication artifact across all of Act Three
A full sequential read of the file (all 2,410 lines) shows the entire Act Three content (Ch.35 through Ch.69) appearing twice: once in the expected form (chapter headers, POV, Must Include/Must NOT, craft notes, in ascending chapter order, lines ~861–1646), and a second time immediately after (lines ~1651–2410) with the same beats — in some cases slightly more elaborated wording — but with no chapter-number headers at all, running in *descending* chapter order (Ch.69 down to Ch.35). Spot-checking several chapters between the two passes (Ch.55, Ch.60's split section, Ch.65, Ch.40) found the substantive content consistent between them — this reads as an accidental duplication from an editing/merge step, not two genuinely different versions in tension with each other. No content contradiction was found in the sampling done for this synthesis, but the file was not diffed word-for-word in its entirety, so a full author/Director cleanup pass should still verify no meaningful drift exists between the two copies before deleting the redundant one. Zero effect on any decision needed for Ch.11 — flagging purely so a future session reading `unit-plans.md` top-to-bottom (rather than jumping straight to one chapter's entry, which is the normal use pattern and unaffected by this) isn't confused by what looks at first glance like a second, unheadered outline.

### 12.8 Ch.10's two unresolved Line Editor attribution findings (the one item on this list closest to actually blocking something)
Direct comparison of `notes/line-edit-ch10.md` against the current `chapters/ch10.md` text shows two of its four findings already fixed (the "because there was more worth checking" overwritten-action clause is gone; the "It served no version of the assignment" explanatory sentence after the porch observation is gone) and two still present exactly as originally flagged:
- `"It's not something I explain well," he said. "I'm still working on the short version."` — bare "he said" tag with no attached action beat, in a three-person dinner scene where action beats are used correctly elsewhere in the same exchange.
- `"He worries enough already," she said finally. "About things that are actually his to worry about. I'm not going to hand him one more."` — same issue; "said finally" describes timing, not action, and doesn't meet the "necessary for clarity after a long passage" carve-out.

(Two lower-priority instances the same note flagged — `"You're staying," she said. Not a question.` and `"You do that a lot," he said.` — are also still present as originally written; the note itself called these lower-priority.)

No `notes/revision-ch10.md` exists to show these were seen and deliberately deferred versus simply missed. Since no chapter before Ch.10 has been left in this half-fixed state without an explicit revision note closing the loop, this reads as an oversight rather than a decision — recommend the Director either apply the two remaining fixes directly (they're small, mechanical, and the note already describes the fix direction) or write a short `revision-ch10.md` explicitly waiving them, before Ch.11 is assigned.
