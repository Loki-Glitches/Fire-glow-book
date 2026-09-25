CHAPTER: Rundown
VERDICT: ISSUES FOUND (all MINOR/VERIFY — nothing plot-affecting; no CRITICAL or MODERATE findings)

FINDINGS
──────────────────────────────────────────────

CATEGORY: Fact-Check
SEVERITY: MINOR
LOCATION: Chapter title, line 1 — `# Rundown`
ISSUE: Every other chapter file in `chapters/` uses the `# Title — POV` header format (`# Hell — Lucifer`, `# Breakfast — Elizabeth`, `# Introductions Are In Order — Lucifer`, etc.). "Rundown" is missing the `— Elizabeth` suffix, breaking the manuscript-wide format convention.
SUGGESTED FIX: Change the header to `# Rundown — Elizabeth`.

CATEGORY: Fact-Check
SEVERITY: MINOR
LOCATION: "Niether of them wanted to trade numbers."
ISSUE: Typo — "Niether" should be "Neither."
SUGGESTED FIX: Correct the spelling.

CATEGORY: Fact-Check
SEVERITY: MINOR
LOCATION: "...since before four people ended up on two benches talking about a woman neither she or Sophie had ever seen."
ISSUE: Grammar — "neither...or" should be "neither...nor," or the clause should be rephrased ("...a woman she and Sophie had never seen").
SUGGESTED FIX: Correct to "neither she nor Sophie" or rephrase.

CATEGORY: Fact-Check
SEVERITY: MINOR
LOCATION: "Probably, yeah. Don’t worry, we will be careful."
ISSUE: This is the only apostrophe in the entire chapter set as a curly/smart quote (’) rather than the straight apostrophe (') used everywhere else in the file (Niether, didn't, wasn't, isn't, etc.) — a stray character-encoding inconsistency, likely from pasting in an edit.
SUGGESTED FIX: Normalize to a straight apostrophe for consistency with the rest of the file.

CATEGORY: Soul/Style
SEVERITY: MINOR
LOCATION: `"So what's the plan," she said. "We just wait around and hope they walk past us again?"`
ISSUE: Per the style guide's locked comma-vs-question-mark rule (§3, locked 2026-09-04): "So what's the plan" is a genuine, complete question, and the rule is explicit that a real question never gets flattened to a comma just because more of the character's speech follows the tag ("Where are we even going?" Elizabeth asked, over Claire's shoulder. "Is there a plan...")). This one instance uses a comma where a question mark is called for. Flagging this single instance only — not treating it as grounds for a full punctuation sweep, which isn't this pass's job.
SUGGESTED FIX: "So what's the plan?" she said.

CATEGORY: Continuity
SEVERITY: MINOR / VERIFY
LOCATION: "We spent an hour with them and neither one thought of it."
ISSUE: A specific elapsed-time figure ("an hour"). The standing project rule locked 2026-09-27 in `notes/character-synopsis.md` prohibits specific elapsed-time markers so the author can control the book's overall timeline without having to reconcile invented numbers later. This rule postdates this chapter (synopsis entry for "Rundown" is dated 2026-09-25, and this is the author's own hand-edited final text), and the example durations the rule targets ("it's been three days," "the past week") read as macro-timeline bookkeeping rather than this line's much smaller-scale estimate of how long the immediately preceding scene lasted — so this likely doesn't need to change. Flagging only so the author can confirm it's not the kind of instance the newer rule meant to catch.
SUGGESTED FIX: None required unless the author wants strict retroactive compliance — could be softened to "We spent all that time with them" if so.

CATEGORY: Continuity
SEVERITY: MINOR / VERIFY
LOCATION: "Sophie dropped onto the couch and put her feet up on the coffee table." ... later: "Sophie pulled her knees up, resting her chin on them."
ISSUE: Small physical-continuity nit — feet planted on the coffee table and knees pulled up to rest her chin on them are two different postures with no repositioning beat shown between them. Physically possible if she moved her feet off the table first, but that shift isn't on the page.
SUGGESTED FIX: A half-beat showing the shift (or dropping one of the two posture details) would close the gap, though a careful reader may not even snag on this.

CATEGORY: Continuity
SEVERITY: VERIFY
LOCATION: "a bag of peaches she'd grabbed on impulse" / the Higgins family-money-for-extras arrangement paragraph
ISSUE: Both of these are new details invented by the Writer and already self-flagged in `notes/character-synopsis.md`'s "After Rundown" entry as unreconciled against the bible — the peach bag wasn't in "My Usual"'s established grocery list (milk, eggs, bread only), and the Higgins arrangement (family money funding specialty stock) isn't previously documented anywhere Revision could find in the bible. Neither contradicts anything locked, but both are exactly the kind of small worldbuilding fact that should get folded into `bible/world-bible.md` or the Higgins entry so a later chapter doesn't accidentally contradict it.
SUGGESTED FIX: Director should reconcile both into the bible (or explicitly bless them as one-off color) rather than leave them floating only in the synopsis.

CATEGORY: Soul/Style
SEVERITY: MINOR
LOCATION: "...his usual tone whenever the store account came up, the extra cases of things Higgins kept in the back for them, the specialty stuff nobody else in town bothered stocking, all of it running on the same standing arrangement that predated Elizabeth caring enough to ask about it."
ISSUE: This single sentence compresses a fair amount of new backstory (the family-money/Higgins arrangement) into a narrated summary rather than dramatizing it. It's brief and filtered through Sam's unconcerned tone rather than delivered as a flat info-dump, so it doesn't rise to a hard Show-Don't-Tell violation — but it's the one spot in the chapter that leans toward telling rather than showing.
SUGGESTED FIX: No urgent fix needed; if revisited, could be trimmed or split so it reads more like something Elizabeth already half-knows rather than a compressed explainer.

CATEGORY: Fact-Check (POV)
SEVERITY: MINOR / VERIFY
LOCATION: "Sam didn't say anything to that for a second, just looked at her, clearly deciding how much of an argument was worth having, then picked his fork back up."
ISSUE: The style guide's locked 2026-09-25/27 rule restricts "reading" other people's interior state/tells to two specific cases: Elizabeth reading dishonesty, and Lucifer/Azrael reading each other. This line has Elizabeth's narration attribute a specific interior calculation to Sam ("deciding how much of an argument was worth having") rather than just describing his outward behavior. It's a small, plausible inference about a brother she knows intimately rather than a "clocked tell" in the analytical-reading sense the rule is really aimed at, so this reads more like ordinary close-sibling familiarity than a violation — flagging as a borderline case rather than a clear one.
SUGGESTED FIX: If the author wants to be strict about the rule, this could be pulled back to a purely external beat (e.g., "just looked at her a second, then picked his fork back up").

WHAT'S WORKING
──────────────────────────────────────────────

- **Outline fidelity is excellent.** Checked line-by-line against the author's own paragraph for this chapter in `bible/manuscript-order.md` #7 — every beat is present in order (car conversation about no numbers exchanged, unloading the ruined groceries, Sam's hello kiss to Sophie, the Higgins message and "good, that's done," Sam cooking while Sophie stays, the Eve discussion, the head twinge, Elizabeth's dislike of Adrian, the "I don't have a father"/apple-crush relay, the plan to check the park, Sam's protective reaction) — nothing skipped, nothing added that contradicts it.
- **Seam quality is clean.** Opens directly inside the car right where "Introductions Are In Order" left off (no numbers exchanged, on the sidewalk), matching `notes/character-synopsis.md`'s Plot Points log for that chapter exactly — no unexplained gap, no reset of emotional state.
- **The locked "genuine dislike, not chemistry" standing habit is executed precisely,** including keeping the one simile about Adrian ("like talking to a wall that occasionally talks back") correctly inside dialogue, where the no-similes rule doesn't apply, rather than letting it leak into narration.
- **The concussion thread is handled exactly to spec:** the ache is a plant, not a mystery — Elizabeth is confident about what caused the original injury, mildly puzzled only by *how much less it should hurt*, and dismisses it via heat/tiredness without any memory fog, matching `bible/elizabeth_character_profile.md`'s locked correction precisely.
- **Sam's scene is a strong, specific piece of character work** — *"He won't. He'll just make a face,"* and *"I appreciate the effort regardless"* land his established warm/teasing register, while his protectiveness ("That's not strange, Liz, that's a red flag") escalates believably without tipping into melodrama or forbidding her outright, matching his profile's "genuine, well-intentioned, not malice" note.
- **The corrected "I don't have a father" line is reproduced accurately** (not the earlier, retired "my father and I don't speak much" misquote flagged in the synopsis) — good evidence the Writer/author cross-checked the corrected continuity note rather than an earlier draft.

SCOPE NOTE: Per the narrow-context rule, this review read the chapter in full plus `bible/manuscript-order.md`, `bible/story-bible.md`, `bible/style-guide.md`, `bible/elizabeth_character_profile.md`, `bible/sam_character_profile.md`, `bible/sophie_character_profile.md`, and `bible/tristan_azrael_character_profile.md`, and both subsections of `notes/character-synopsis.md` — not the full text of "Introductions Are In Order." Nothing about the seam genuinely required going back to that chapter's full text; the Plot Points log was sufficient.
