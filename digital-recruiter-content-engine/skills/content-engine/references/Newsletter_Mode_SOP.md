# Digital Recruiter — Newsletter Mode SOP

**Version:** 1.0
**Purpose:** This SOP produces TWO deliverables from a single source:
1. A **long-form email newsletter** (800+ words) targeting the user's locked ICP
2. A **LinkedIn promo post** designed to drive newsletter signups

Newsletter Mode reuses many of the same anti-AI rules and voice principles as Creation Mode, but adapted for a single long-form output instead of 16 short posts. Same SOP rules, longer format.

---

## CRITICAL OPERATING RULES

Same Rules 1–9 as the system prompt. Specifically relevant to Newsletter Mode:

- One discrete sub-phase per response.
- Every approval gate is blocking.
- The structural rules from `Content_Creation_SOP.md` (no em dashes, max 4 sentences per paragraph, 6th-grade reading level, contractions, anti-AI language) apply to BOTH the newsletter and the promo post.
- The newsletter is NOT a sales pitch. It is a long-form trust deposit. Do not close with a CTA to buy services. Close with a reframe or takeaway.
- Anti-repetition applies: check the Memory Log for prior newsletter topics before proposing one.

---

## PHASE MAP

| Phase | Name | Approval Gate? |
|-------|------|----------------|
| 0 | Source Lock-In | No |
| 1 | ICP Confirmation | YES |
| 2 | Topic Selection | YES |
| 3 | Subject Line Draft | YES |
| 4 | Newsletter Body Draft | No (rolls into 5) |
| 5 | De-AI Pass on Body | YES |
| 6 | LinkedIn Promo Post | YES |
| 7 | Memory Log Update | No (auto-runs) |

Total responses: ~10–12. Less than Creation Mode because there's only ONE deliverable in long form (plus the short promo).

---

## PHASE 0 — SOURCE LOCK-IN

**Discrete sub-phase. Run in its own response.**

**Purpose:** Establish the source material as immutable. Prevent fabricated examples from sneaking in.

**Acceptable sources:**
- Interview transcript (Interview Mode output)
- Sales call or candidate conversation transcript
- Voice memo transcript
- A specific topic from the user's locked Memory Log topic list ("turn this topic into a newsletter")
- Notes the user types or pastes
- An approved post from a prior Creation batch that the user wants to expand

**Prompt to run (internally):**
> Treat the source material as immutable. You may not introduce new concepts, claims, metaphors, examples, numbers, or conclusions not explicitly present. Every sentence in the newsletter must be traceable to something in the source material, even if lightly rephrased. Acknowledge receipt and wait for the next instruction.

**Output:** Acknowledge receipt. Do not summarize. Do not propose topics yet. Wait.

**Approval gate:** None. Continue to Phase 1.

---

## PHASE 1 — ICP CONFIRMATION

**Discrete sub-phase. Run in its own response.**

**Purpose:** Confirm the locked ICP from onboarding is the right target for THIS newsletter. Newsletter audiences are sometimes narrower than LinkedIn audiences.

### Restate the locked ICP from the Memory Log

Output the full ICP document the user approved during onboarding.

### Ask one diagnostic question

> "Is this newsletter for the same ICP as your LinkedIn posts, or is it for a narrower segment? Some users write newsletters for a specific subset of their audience (existing prospects, a specific job title within the buyer pool, etc.). Confirm or refine."

If the user wants to narrow the ICP for this newsletter, update working memory with the narrower target. The narrower target governs only this newsletter; the locked ICP remains in place for everything else.

**APPROVAL GATE:** Wait for `Approved. Lock.` before moving to Phase 2.

---

## PHASE 2 — TOPIC SELECTION

**Discrete sub-phase. Run in its own response.**

**Purpose:** Pick ONE topic that the entire newsletter argues. Unlike Creation Mode (12-16 topics), Newsletter Mode commits to one.

### Topic Constraints

The chosen topic must:
1. Be directly supported by the source material
2. Be relevant to the ICP confirmed in Phase 1
3. Have enough depth to sustain 800+ words of single-thread argument
4. Not duplicate any prior newsletter topic in the Memory Log
5. Lead to a reframe or takeaway, not a sales pitch

### Topic Generation Process

Propose **3–5 candidate topics** drawn from the source material. For each:

```
Topic [N]: [Working title]
Primary focus: [Problem / Process / Proof / Market Intelligence / Pattern Recognition]
One-sentence argument: [What the newsletter will assert]
Supporting material in source: [List the specific stories, numbers, examples that will sustain the argument]
Why this matters to the ICP right now: [One sentence]
```

### Anti-repetition cross-check

Scan the uploaded Memory Log for any prior newsletter that overlaps. If there's overlap, flag the candidate and propose a different angle on the same theme.

### Role-Specific Topic Focus

#### If Role = Business Owner / BD

Topics should position the user as the expert operator in their niche. Candidates that work:
- Patterns the user sees across dozens of engagements
- Mistakes [ICP company type] make in [the area you serve]
- Market shifts the ICP needs to know about
- Deep-dives into how great companies operate differently in the user's area
- Insider regulatory, comp, or operational knowledge that ICP doesn't see

The reader should finish thinking: *"this person sees things I don't."*

#### If Role = Recruiter / IC

Topics should share insider knowledge from the trenches. Candidates that work:
- What top candidates in the niche actually want
- How the best hiring processes work (vs. what most companies do)
- Market intelligence (comp trends, candidate availability, regional dynamics)
- Real stories that illustrate bigger trends
- Interview tips and process advice with mechanical detail

The reader should finish thinking: *"this person really knows this market."*

### Output

Present the 3–5 candidates in the format above and ask the user to pick one (or request a different angle).

**APPROVAL GATE:** Wait for the user to pick a topic and type `Approved. Lock.`

---

## PHASE 3 — SUBJECT LINE DRAFT

**Discrete sub-phase. Run in its own response.**

**Purpose:** Subject lines determine open rates. They're worth their own dedicated phase.

### Subject Line Rules

- **Specific and curiosity-driven.** Challenges a common belief or teases a counterintuitive insight.
- **Recognizable to the ICP.** A [ICP title] should read it and think "I need to open this."
- **No clickbait.** The newsletter must deliver on the subject line's promise.
- **Avoid generic openers** like "Quick thoughts on…" or "What I've been thinking about…"
- **Avoid the banned phrases list** from `Content_Creation_SOP.md` Appendix A — applies to subject lines too.

### Subject Line Examples

Good:
- "The hiring mistake that costs Series B companies $2M"
- "Why your best recruiter just quit (and what it actually means)"
- "3 things I learned from 47 failed VP searches"
- "The post-COVID program rebuild nobody is talking about"

Bad (don't produce these):
- "My thoughts on hiring this week" (vague)
- "🔥 You won't BELIEVE this hiring story 🔥" (clickbait)
- "Newsletter #14: Hiring trends" (no curiosity)
- "Let's discuss recruiting" (no specificity)

### Output

Generate **3 subject line candidates** for the user to choose from. For each, include:
- The subject line itself
- One sentence on what curiosity it leverages
- Estimated specificity score: would only the right ICP find this interesting? (Yes/Mostly/No)

**APPROVAL GATE:** Wait for the user to pick a subject line. Allow tweaks. Lock the chosen line before drafting the body.

---

## PHASE 4 — NEWSLETTER BODY DRAFT

**Discrete sub-phase. Run in its own response.**

**Purpose:** Draft the full 800+ word newsletter body. This is messy first draft territory — Phase 5 will clean it up.

### Length and Structure Rules

- **800+ words.** This is the floor, not the ceiling. If the topic supports it, 1,200 words is fine.
- **Single narrative thread.** Build ONE argument progressively from start to finish. Do not bounce between unrelated points.
- **Same whitespace formatting as LinkedIn posts:**
  - 1–3 sentences per cluster, then a line break
  - Single-sentence paragraphs allowed for emphasis
  - Vary the rhythm — never uniform cluster length
  - Max 4 sentences per paragraph
  - No em dashes, ever
- **No bullet points in the body.** All flowing prose. The newsletter reads like a well-structured conversation, not a listicle.
- **Use real numbers, specific examples, named situations.** Avoid abstract generalities.

### Newsletter Skeleton

This is the default structure for most newsletters. Adapt as needed.

1. **Open with a specific story or observation** that hooks the reader within the first 100 words. The story should be drawn from the source material. Don't start with throat-clearing ("In today's market…") — start with the scene.

2. **Build the argument through 3–4 supporting points.** Each point uses real examples or numbers from the source. Each point connects to the next. The reader should feel like they're being walked through a single coherent line of reasoning, not given a list of disconnected observations.

3. **Close with a reframe or takeaway** that shifts how the reader thinks about the topic. The close is NOT a sales pitch. It is NOT a CTA to buy services. It IS a single sentence or short paragraph that leaves the reader with a different mental model than they had at the start.

### Tone Enforcement

Apply the user's selected tone from the Memory Log (Punchy, Conversational, Strategic, Raw, or Custom) per `Content_Creation_SOP.md` Appendix C. The tone affects word choice and rhythm. The structural rules above are unchanged regardless of tone.

### Source Discipline

- Every claim is traceable to the source material.
- Every number is from the source.
- Every named example is from the source.
- If the body would be stronger with a story or stat that isn't in the source, leave a placeholder `[NEED FROM USER: specific example of X]` and flag it at the end of the draft. Do NOT invent.

### Output

The full newsletter draft, top to bottom. Subject line at the top. Body below. Any `[NEED FROM USER]` flags listed at the end.

**Approval gate:** None. Continue to Phase 5.

---

## PHASE 5 — DE-AI PASS ON BODY

**Discrete sub-phase. Run in its own response.**

**Purpose:** Run the newsletter body through the same anti-AI scrub that Creation Mode runs on individual posts. The newsletter is longer, so AI tells have more room to hide. This pass catches them.

### Compressed De-AI Sequence (specific to Newsletter)

Newsletter is one long document, not 16 posts in batches. So instead of running 6 separate sub-passes (5.0 through 5.3 in Creation), run the following compressed sequence in this single phase. Apply ALL of these in order:

#### 1. Audience Calibration

- Cut explanations of terms the ICP knows cold
- Cut over-explained consequences
- Cut translated jargon
- Convert third-person speaker references to first person
- Replace banned terms (`hiring manager`, `candidate`, `client`) with the ICP titles from Phase 1

#### 2. Structural De-Packaging

- Rewrite any sentence that wraps things up cleanly, sounds quotable, or feels like a slide takeaway. Replace with continued explanation.
- Kill balanced contrast structures ("It's not X. It's Y.")
- For every abstract noun (`value`, `leverage`, `alignment`, `positioning`, `friction`, etc.), confirm the next sentence explains what physically happens. If not, rewrite.
- Delete motivational filler ("That moment matters", "Patterns don't fix themselves")

#### 3. LLM Throat Clearing

Apply the 11-section sweep from `Content_Creation_SOP.md` Phase 5.1b:
1. Mirrored Antithesis — kill
2. Performed Directness (`real`, `actual`, `clean`, `surface`, etc.) — replace with what specifically happened
3. Hedging Frames (`there's a version of`, `there's a world where`) — direct claim
4. Earned Pivots (`Here's the thing`, `What most people miss`) — delete, just say the thing
5. Specificity Costume (invented examples) — flag, don't invent
6. Empathy Preload (`I get it`, `That makes sense on paper`) — delete
7. Telescoping Restatement (same idea three times) — keep version three only
8. Authority Aside (`In my experience`) — delete, add concrete detail instead
9. Graceful Concession (`That's not always wrong`) — delete unless from source
10. Reframe Label (`This is really about`) — delete, talk about the thing directly
11. Resonance Close — replace with continued explanation

#### 4. Spoken American Realism

- Contractions everywhere natural
- Break formal sentences (>20 words, multiple commas, sounds composed)
- 6th-grade reading level
- Allow fragments
- Replace meaning ("That creates burnout") with what happened ("You're working 60 hours by Thursday")
- Allow repetition if the source repeated it

#### 5. Grade Level Audit

Final structural simplification. Break compound sentences. Eliminate subordinate clauses. Keep industry jargon, simplify sentence architecture.

#### 6. Cadence Audit (newsletter-specific)

Read the newsletter end to end, out loud (mentally). Check:
- Does it have one continuous thread, or does it feel like 4 separate posts strung together?
- Does any paragraph end with a "land" — a quotable, satisfying fragment? Rewrite as continued explanation.
- Is the close a reframe or a CTA? If CTA, rewrite.
- Does any sentence sound like a LinkedIn influencer or a corporate brochure? Rewrite or cut.

### Banned Phrases Sweep

Run the full banned-phrases list from `Content_Creation_SOP.md` Appendix A across the newsletter. Replace every instance.

### Output

The final newsletter body, fully de-AI'd. Same length or longer than the Phase 4 draft (the de-AI pass should not shorten the document).

**APPROVAL GATE:** Wait for `Approved. Lock.` before moving to Phase 6.

---

## PHASE 6 — LINKEDIN PROMO POST

**Discrete sub-phase. Run in its own response.**

**Purpose:** Generate a LinkedIn post that drives signups to the newsletter. Short, curiosity-driven, points to the newsletter without giving away the full insight.

### Promo Post Rules

- **Length:** 5–6 sentence clusters. Roughly 100–200 words. Same whitespace rules as any LinkedIn post.
- **Teases the newsletter topic.** Creates curiosity without giving away the reframe or takeaway.
- **References ONE specific detail or stat from the newsletter** to hook the right reader.
- **Ends with a clear CTA.** Examples:
  - "I write about this every week in my newsletter. Link in comments."
  - "Wrote the full breakdown in this week's newsletter. Drop a comment if you want the link."
  - "Full piece is in this week's newsletter — link in my bio."

### What NOT to do in the promo post

- Don't summarize the entire newsletter. The promo should make the reader want to read the full thing.
- Don't use a generic opener ("New newsletter dropped today!"). The post must work as a standalone LinkedIn post — meaning, even if the reader never clicks through, they got something useful.
- Don't violate the Phase 3 hook rules from Creation Mode. The first 1–2 lines must identify the right reader, pass the Dentist Office test, and avoid banned words.
- Don't use the same hook structure as the newsletter's opening sentence. The promo post is a different on-ramp, not a copy of the first line.

### Tone Enforcement

Same tone selection from the Memory Log applies. Same banned phrases list applies. Same anti-AI rules apply.

### Output

The full promo post, ready to copy-paste to LinkedIn.

**APPROVAL GATE:** Wait for `Approved. Lock.` before moving to Phase 7.

---

## PHASE 7 — MEMORY LOG UPDATE

**Discrete sub-phase. Run in its own response.** Auto-runs after Phase 6 approval.

**Purpose:** Generate the updated Memory Log so the next session knows about this newsletter and doesn't duplicate the topic.

### Required additions to the Memory Log

In addition to the standard Memory Log contents (per `Memory_Log_Template.md`), add:

```
NEWSLETTERS CREATED TO DATE:

Newsletter [N] — [Date]
Subject line: [Subject line]
Topic: [One-sentence summary]
Reframe / takeaway: [One sentence — the close]
Promo post first line: [First 1-2 sentences of the LinkedIn promo]
```

### Output

A Claude Artifact of type `text/markdown` titled `Client_Memory_Log.md`. Per the standard end-of-session flow, do NOT paste the Memory Log inline.

Tell the user to download the artifact and upload it to Project Knowledge before the next session.

Then display the Strategy Reminder per the system prompt.

---

## NOTES FOR THE AGENT

- Newsletter Mode is heavier per-deliverable than Creation Mode. The user is choosing depth over breadth. Don't rush.
- If the source material is genuinely thin (e.g., a 5-minute conversation or 200 words of notes), tell the user: "There's not enough source material here for a full newsletter without inventing things. Want to do a quick interview to expand the source, or pick a different topic?"
- The newsletter and the promo post are tightly coupled. Don't write them independently — the promo post should reference a specific detail from the newsletter.
- If the user wants to repurpose an existing newsletter as a series of LinkedIn posts (the reverse direction), that's not Newsletter Mode — switch to Creation Mode and use the newsletter as source material.

## END OF NEWSLETTER MODE SOP
