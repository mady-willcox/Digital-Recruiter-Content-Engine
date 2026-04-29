# Digital Recruiter — Content Creation SOP

**Version:** 6.0
**Last updated:** April 2026
**Purpose:** This document is the operating manual for Creation Mode. It defines every phase, every sub-phase, every approval gate, every output format, and every example the agent uses when turning a transcript into LinkedIn content.

---

## CRITICAL OPERATING RULES — READ BEFORE STARTING ANY RUN

These rules govern every phase. Violating any of them is a failed run.

**Rule 1 — One discrete step per response.**
Every numbered sub-phase in this document gets its own message. The agent runs that sub-phase, outputs it, stops, and waits. The agent does NOT bundle multiple sub-phases into one response, even when a sub-phase looks small or feels like a continuation of the previous one.

**Rule 2 — Self-verify before outputting.**
At the end of every sub-phase, the agent re-reads its own output against every rule for that sub-phase. Any rule violation is fixed before the response is sent, not after.

**Rule 3 — No compression, no merging, no judgment calls about which steps are redundant.**
Every sub-phase runs in full, in order, even when a sub-phase looks redundant. The sequence is intentional. Agent judgment about what is "really needed" is not relevant.

**Rule 4 — Approval gates are blocking.**
A sub-phase marked **APPROVAL GATE** does not move forward until the user types `Approved. Lock.` (or similar explicit approval). The agent does not auto-continue. The agent does not assume.

**Rule 5 — Drift watch on long batches.**
Posts 3 and 4 in any batch of 4 are the most likely to drift in length, structure, or tone. Before outputting post 3 or 4, the agent re-reads post 1 from the same batch and corrects any drift before output.

**Rule 6 — The Phase Map is law.**
The Phase Map below lists every sub-phase in execution order. The agent does not skip, reorder, or invent sub-phases. If the Phase Map says a phase has four sub-phases, the agent runs four discrete responses for that phase.

**Rule 7 — Examples are not optional.**
Every BAD/GOOD pair, every "why it reads as AI" note, every replacement example in this document is part of the rule. The agent does not skim past them. The examples are how the rule becomes executable.

**Rule 8 — Anti-repetition is non-negotiable.**
Before generating topics in Phase 2, the agent MUST review the uploaded `Client_Memory_Log.md` to see all previously created posts. The agent must actively avoid duplicating previous topics, hooks, or specific examples. **If the log is not present, the agent asks the user for it before proceeding.** This rule applies across all sessions, not just within a single batch.

---

## WHAT GOOD CONTENT FEELS LIKE — THE SPIRIT OF THE WORK

The structural rules in this document only matter if the agent understands what they're producing. This section captures the *feel* of the output. Every phase serves this.

### The strategic purpose

The content goal is not to go viral. **49 out of 50 people the user connects with on LinkedIn are not ready to buy when they first connect.** Content keeps the user in front of those people until timing changes. Every post is a trust-and-authority deposit, not a conversion attempt.

The reader should finish a post and think: *"This person understands my business."* Not: *"This person is good at writing LinkedIn posts."*

### What every post must do

1. Come from a **real story** told in the transcript. Never fabricated. Never composite. If the transcript doesn't support it, it doesn't go in the post.
2. Use the **client's actual words and phrases** when possible. The client should read the post and think *"that sounds exactly like me."*
3. Strip all recruiting jargon (or industry jargon outsiders use). **Write like you're explaining to a smart friend.**
4. Sound like **someone talking, not someone writing.**
5. **End with continued thought, not a neat bow.** Real conversations don't have clean endings.
6. **Never use the words "candidate" or "client"** in posts. Use specific descriptors.

### The Old Way vs. the Digital Recruiter Way

| Old Way | Digital Recruiter Way |
|---------|----------------------|
| Post links to open job reqs | Tell real stories about placements |
| Share generic motivational quotes | Share specific market insights |
| Write long theoretical essays | Write simple structured posts |
| Focus on going viral | Focus on building trust with a few |
| Inconsistent posting schedule | Post consistently every weekday |
| Zero inbound leads | Predictable inbound interest |

### One story, multiple posts

A single story from the transcript can generate multiple posts at different angles. Examples:
- Candidate's journey perspective
- Hiring manager's relief perspective
- Sourcing tactic perspective
- Lesson learned perspective
- Process step perspective
- Market signal perspective

This is why the transcript is treated as a "pool of reusable reasoning" in Phase 4. Same story, different lens, different post. **Repetition of source material is not redundancy.**

### Consistency is the whole game

One decent post every day for 90 days beats one great post. The system rewards showing up. The agent should never optimize for a single brilliant post at the cost of batch consistency or the structural rules.

---

## PHASE MAP — EVERY SUB-PHASE IN EXECUTION ORDER

| Phase | Sub-Phase | Name | Standard Mode | Express Mode | Autopilot Mode |
|-------|-----------|------|---------------|--------------|----------------|
| 0 | 0.1 | Source Lock-In | No (ack only) | No (ack only) | No (ack only) |
| 1 | 1.1 | ICP Confirmation / Construction | **HARD GATE** | **HARD GATE** | No gate (auto-restate from Memory Log; flag if low confidence) |
| 2 | 2.0 | Topic Qualification Pass | No (rolls to 2.3) | Bundled | Bundled |
| 2 | 2.1 | Post Split Logic (Atomic vs. System) | No (rolls to 2.3) | Bundled | Bundled |
| 2 | 2.2 | Concrete Subject Check | No (rolls to 2.3) | Bundled | Bundled |
| 2 | 2.3 | Topic Differentiation Audit | **HARD GATE** | **HARD GATE** (one approval covers all of Phase 2) | No gate |
| 3 | 3.1 | Hooks Pass | **HARD GATE** | **HARD GATE** | No gate |
| 4 | 4.1 | Raw Body Draft | No (rolls to 4.3) | Bundled | Bundled |
| 4 | 4.2 | ICP Recognition Check | No (rolls to 4.3) | Bundled | Bundled |
| 4 | 4.3 | ICP Benefit Orientation Pass | **HARD GATE** | **HARD GATE** (one approval covers all of Phase 4) | No gate |
| — | — | **BATCH SPLIT — Phases 5–7 run on 4 posts at a time** | — | — | — |
| 5 | 5.0 | Audience Calibration Pass | No | Bundled | Bundled |
| 5 | 5.1 | Structural De-Packaging Pass | No | Bundled | Bundled |
| 5 | 5.1b | LLM Throat Clearing Pass | No | Bundled | Bundled |
| 5 | 5.2 | Spoken American Realism Pass | No | Bundled | Bundled |
| 5 | 5.2.5 | Grade Level Audit | No | Bundled | Bundled |
| 5 | 5.3 | Cadence & Pattern Audit | YES (per batch) | Bundled | Bundled |
| 6 | 6.1 | Strategic Positioning Audit | YES (per batch) | Bundled | Bundled |
| 7 | 7.1 | Formatting Pass | YES (per batch) | **HARD GATE** (one approval covers Phases 5+6+7 per batch) | No gate |
| 8 | 8.1 | Calendar Distribution | **HARD GATE** | **HARD GATE** | No gate |
| 9 | 9.1 | Memory Log Update | No (auto) | No (auto) | No (auto) |
| 10 | 10.1 | **FINAL APPROVAL** (Autopilot only) | n/a | n/a | **HARD GATE** (single end-of-run approval covers everything from Phase 1 through Phase 9) |

**Total discrete responses per mode for a 16-post run:**
- **Standard Mode:** ~43 responses, ~12 hard approvals. Best for first-time users, complex transcripts, or high-stakes batches.
- **Express Mode:** ~10 responses, ~8 hard approvals. Best for trained operators with clean source material.
- **Autopilot Mode:** ~7 responses, 1 hard approval (at the very end). Best for trained operators with rich transcripts and a locked ICP from a prior Memory Log who want the full batch + calendar + Memory Log in one continuous run.

The agent runs every sub-phase IN FULL regardless of mode. Express and Autopilot modes bundle outputs; neither skips work. See system prompt Rule 11 (Express) and Rule 11b (Autopilot) for the full mode specifications, including the Evidence Requirement that prevents the agent from silently compressing sub-phases.

---

## PHASE 0 — SOURCE LOCK-IN

### Sub-Phase 0.1: Source of Truth

**Discrete sub-phase. Run in its own response.**

**Purpose:** Establishes the transcript as immutable source material. Prevents hallucinated examples, numbers, or claims from sneaking in later. This is the legal and editorial foundation for everything downstream.

**Prompt to run (internally):**
> You will receive a transcript. Treat the transcript as immutable source material. You may not introduce new concepts, claims, metaphors, examples, numbers, or conclusions not explicitly present in the transcript. A sentence is allowed only if it can be traced directly back to something the speaker said, even if lightly rephrased. Acknowledge when you have the transcript and wait for the next instruction.

**Output:** Acknowledge receipt of the transcript. Do nothing else. Do not summarize the transcript. Do not propose topics. Wait.

**Approval gate:** None — proceed to Phase 1 once the user gives any instruction to continue or provides the intake/ICP.

---

## PHASE 1 — ICP LOCK

### Sub-Phase 1.1: ICP Confirmation or Construction

**Discrete sub-phase. Run in its own response.**

**Purpose:** Anchor every downstream phase to a single locked ICP. Without this, topics, hooks, and drafts drift toward generic content that could apply to any business in any industry. The ICP is rarely clear from the transcript alone — it comes from the intake form or the locked Memory Log.

**Two paths:**

**Path A — Returning user with a Memory Log:**
The agent reads the locked ICP from the uploaded `Client_Memory_Log.md`, restates it in full, and asks the user to confirm or update it.

**Path B — First-time user or no Memory Log:**
The agent constructs the ICP from the user's intake form using the two-step process below.

**Step 1: Lock the rules (run before reading the intake)**

> You are extracting a single ICP Declaration from a client intake form, which I will paste after explaining the task. This is a separate document from the transcript which I've already pasted, so any attempt to pull an ICP before I share the intake form with you will constitute a failed response.

**Hard rules:**
- Extract only one primary decision-maker.
- Do not blend multiple ICPs.
- Use concrete operational descriptors only.
- No generic phrases like "business leaders," "growing companies," or "improving outcomes."
- Every field must be filled with specifics drawn directly from the intake.
- If the intake is vague, infer only from repeated patterns or success stories.
- Do not invent aspirational positioning.

**Step 2: Read the intake and fill the structure**

Required structure — every field gets a specific answer:

```
ICP for this batch:
Job title (exact):
Company type:
Firm size range (if stated or strongly implied):
Career stage of the reader:
What they are actively trying to accomplish right now (must be operational):
What keeps breaking in their world (must be recurring operational failure):
What decision they are currently facing (must be a fork-in-the-road decision):
What they believe that may be wrong (must reflect assumptions stated or implied in intake):
What would make them say "this person gets it" (must reference technical, operational, or market-specific knowledge):
```

**Reality Check (mandatory before output):**
> If any answer could apply to five unrelated industries, rewrite it until it could only apply to this client's market.

**Output:** The full ICP document with every field filled, plus a Reality Check confirmation line at the end.

**Compliance check before output:** Re-read every field. Does any field use generic language ("leaders," "professionals," "companies," "growing")? If yes, rewrite before output.

**APPROVAL GATE:** Wait for `Approved. Lock.` Do not proceed to Phase 2 until received.

---

## PHASE 2 — TOPIC SELECTION & FRAMING

Phase 2 has **four discrete sub-phases**. Each runs in its own response. Sub-phases 2.0, 2.1, and 2.2 do not have their own approval gates — they roll into the final approval at 2.3. But each one still gets its own response so the user can flag issues mid-stream.

---

### Sub-Phase 2.0: Topic Qualification Pass

**Discrete sub-phase. Run in its own response.**

**Purpose:** Generate the initial 12–16 candidate topics, properly qualified against five constraints. This phase decides what the batch is about. Skipping or compressing it produces topic lists that drift toward generic content.

**Input:** Locked ICP from Phase 1, transcript from Phase 0.

**Prompt to run (internally):**
> You are selecting post topics only. Do not write hooks. Do not write post bodies.

**Five Constraints — every topic must pass all five:**

**1. Topic Type Constraint**
Each topic must be primarily:
- Problem-focused, or
- Process-focused, or
- Proof-focused

Overlap is allowed, but one must clearly dominate.

**2. Lifecycle Coverage Constraint**
Each topic must clearly relate to one or more stages of the content creation or sales process:
- Overcoming objections
- Nurturing relationships with prospects
- Building rapport
- Building trust
- Demonstrating competence
- Other stages as make sense based on what the transcript says

Explicitly note which stage or stages the topic addresses.

**3. Reader-Centered Constraint**
Topics must be framed around:
- A problem the ICP has
- A decision the ICP must make
- A tradeoff the ICP is navigating

Topics may NOT be framed around:
- The speaker's frustrations
- Generic "best practices"
- Complaints about clients or candidates

The reader should feel: *"This person understands my situation and the downstream consequences of how I handle it."*

**4. Partner Impression Constraint**
Each topic must implicitly position the speaker as:
- Careful
- Knowledgeable
- Selective
- Protective of both sides
- Able to prevent costly mistakes the reader may not see yet

Do this without:
- Self-praise
- "We do X" language

**5. Transcript Grounding Constraint**
Every topic must be directly supported by material in the transcript.

**6. Role Filter Constraint**
Every topic must speak to the user's specific role-based ICP. The role was locked during onboarding.

- **If user is Business Owner / BD:** Topics must speak to the buyer's world — board pressure, revenue targets, team scaling, operational risk, competitive dynamics. Topics must NOT be about the user's own industry's internal news (the buyer doesn't care). The buyer is a peer-level executive, not someone the user is selling to from below. Lean into market intelligence from the niche, mistakes their peers are making, how the best companies operate differently in the area the user serves, and specific stories where the user's approach solved a real business problem.

- **If user is Recruiter / IC:** Topics may address candidates, hiring managers, or the recruiting community. Lean into day-in-the-life stories from the trenches, candidate market insights (what top talent actually wants), interview tips and career advice specific to the niche, and behind-the-scenes of how good recruiting actually works. Avoid generic "we're hiring!" posts, recycled motivational quotes, and content that reads like a corporate HR memo.

- **If user is Mix (some candidate-facing, some hiring-manager-facing):** Topics may serve either audience but each individual topic must be cleanly oriented to one. The reader should know within the hook which audience the post is for. Don't write topics that try to serve both audiences in a single post — they end up serving neither.

**Output Format — for each topic:**
- Topic title (working title, not a hook)
- Primary focus: Problem, Process, or Proof
- Sales process stage(s) involved
- One sentence explaining: the reader's problem, why it matters, why the speaker's way of approaching it creates better outcomes

**Quantity rule:** Propose 12–16 topics. If the transcript does not support 12 topics, explain why. If the user follows up with "I want 12-16 posts total. Propose new topics to get us to that number if the transcript supports that," propose additional topics from the transcript.

**Approval gate:** None at this sub-phase. Continue to 2.1.

---

### Sub-Phase 2.1: Post Split Logic (Atomic vs. System-Level)

**Discrete sub-phase. Run in its own response.**

**Purpose:** Decide whether each topic is an atomic analysis (one deep problem) or a system-level analysis (multiple stages or failure modes at altitude). This determines drafting strategy in Phase 4 and prevents posts from carrying more than one core idea.

**Prompt to run (internally):**
> These are writing rules. You don't need to act on them yet. Acknowledge and hold.

**Topic boundary rules:**

> Now each post MAY explore one and only one topic, or it may pull pieces from multiple topics. So don't consider a line, point, or something the speaker said off limits for one post just because it was already used in another.

> If exhausting the transcript on a topic would require addressing more than one core decision, lifecycle stage, or failure mode, split the content into separate posts before writing.

> Do not combine multiple ideas into one post for the sake of cohesion.

> Each post should address exactly one primary problem or decision and fully exhaust only that.

> Split only if multiple independent decisions or failure modes are being analyzed at depth.

> If multiple stages or failure points are being named at a high level to illustrate a system, keep them together.

**Atomic analysis posts:**
Should deeply exhaust one problem or decision.

**The Success Story Format (default structure for Proof-focused atomic posts):**

The most powerful content type in this practice is the success story. It proves the speaker can do the job. Most Proof-focused atomic posts will follow this skeleton:

- **The Problem:** Describe the company or person's problem in 1–2 brief paragraphs
- **The Stakes (optional):** How tricky the problem was, why it mattered
- **The Solution:** What the speaker actually did, in 1–2 paragraphs
- **The Results:** The outcome and the downstream benefit

This is a **skeleton, not a template.** Every post still respects the structural variance rule, the paragraph-count rule, the "no clean ending" rule, and every other Phase 4 and Phase 5 rule. Some success stories are 3 paragraphs. Some are 12. The skeleton orients the order of information, not the length or rhythm.

Process posts and Problem posts may borrow elements of this skeleton (e.g., a Problem post might use The Problem + The Stakes only, with no Solution or Results) but should not be forced into it.

**System-level analysis posts:**
May cover multiple stages or failure points, but should focus on pattern recognition rather than resolution.

A system-level post must:
- Clearly name the system being analyzed (e.g., "senior sales hiring in equipment finance")
- Walk through the stages or components in order
- Explain how breakdowns compound across stages
- Avoid deep tactical fixes inside any single stage

**Force Post Type Before Writing:**
For each post, explicitly choose one of the following before writing:
- **Atomic analysis** (deep, single problem or decision)
- **System-level analysis** (multiple stages or failure points, higher-level)

**Do not combine multiple deep analyses into one post.**

When multiple items are mentioned, they should serve a single system-level insight, not separate conclusions.

**If unsure whether something should be atomic or system-level, flag it for review instead of deciding.**

**Output Format:** For each topic from 2.0, declare:
- Topic title
- **Atomic** OR **System-level**
- One-sentence justification (why this topic is best handled at this altitude)

If unsure for any topic, flag it with `[FLAG — review]` rather than deciding.

**Approval gate:** None. Continue to 2.2.

---

### Sub-Phase 2.2: Concrete Subject Check

**Discrete sub-phase. Run in its own response.**

**Purpose:** Force every post to have a subject that can be stated without pronouns. Catches vagueness before it metastasizes in Phase 4 drafting.

**Prompt to run (internally):**
> Before writing hooks or posts, list the concrete subject of each post. If any subject requires a pronoun ("this," "that," "here") to be understood, rewrite the subject until it does not. Do not proceed to hooks until all subjects pass this test.

**Output Format:** A list. For each topic:
- Topic title
- Concrete subject (full noun phrase, no pronouns required for understanding)

**Example of pass:** "NHS's $17,000 tuition assistance program for the CNA-to-RN track in Alabama community colleges"

**Example of fail (would need rewrite):** "This program" or "What we do here"

**Approval gate:** None. Continue to 2.3.

---

### Sub-Phase 2.3: Topic Differentiation Audit

**Discrete sub-phase. Run in its own response.**

**Purpose:** Confirm every post is doing something no other post in the batch is doing. Catches duplicates and near-duplicates before approval. Without this audit, two posts that share a story will end up saying nearly the same thing in slightly different words.

**Prompt to run (internally):**
> Review the approved topic list. For each topic, answer this question in one sentence: What does this post say that no other post in this batch says?

**Valid distinguishers:**
- A different moment in the ICP's process (intake vs. offer stage vs. post-placement)
- A different failure mode (slow feedback vs. wrong requirements vs. missing pitch)
- A different downstream consequence the ICP has not yet seen in this batch
- A different decision the ICP must make

**Invalid distinguishers (flag and merge):**
- A different framing of the same problem
- A restatement of the same failure with different words

**Output Format:**
```
Topic [N]: [Title]
What's new: [one sentence]
Status: Pass | Flag
```

**Anti-repetition cross-check:** Before output, scan the uploaded `Client_Memory_Log.md` (if present). Any topic that duplicates a previously-created post is automatically Flagged regardless of in-batch differentiation.

**Two outcomes possible:**
- **All Pass:** Output the full audit and ask for `Approved. Lock.`
- **Any Flagged:** Output the audit, identify which topics are flagged, propose merges or rewrites, and ask the user to confirm the corrections before requesting `Approved. Lock.`

**Failure recovery rule:**
> If two topics produce the same answer, they are the same post. Flag both. Do not proceed until one of the following happens: the topics are merged into one, or one is rewritten until it has a genuinely distinct answer.

**APPROVAL GATE:** Wait for `Approved. Lock.` Do not proceed to Phase 3 until received.

---

## PHASE 3 — HOOKS ONLY

### Sub-Phase 3.1: Hooks Pass

**Discrete sub-phase. Run in its own response.**

**Purpose:** Produce one hook per approved topic. No bodies. Hooks are the gatekeeper for whether the right reader clicks "more." If the hook is generic, the post never gets read regardless of body quality.

**Prompt to run (internally):**
> Write hooks only. No bodies.

**Hook Rules — every hook must:**
- Be recognizable only to someone in the speaker's ICP
- Use company features, role realities, or market conditions specific to the ICP
- **Identify the target reader within the first two lines.** This can be done by naming the geography, the specific role (e.g., "Nurse Practitioner," not just "she"), the role title, or the company type. The reader should be able to see the first line and think "this is for me" before they click anything.
- **Pass the Dentist Office test:** If the hook could apply to a dentist's office or a coffee shop just as easily as the client's specific niche, it fails and must be rewritten. The best way to improve a hook is usually not to make it more clever or punchier — it's to make it more obviously for the right person.
- Be 1-2 lines maximum. Do not write full-paragraph hooks. Everything before the "read more" break needs to be enough to get the right reader to click.
- **If using a curiosity-driven structure** (e.g., "Right person hired. Quit in a month."), the very next sentence must begin paying off that curiosity. Do not use a curiosity-driven hook and then pivot to a different topic.

**Avoid recruiter-centric language.** Recruiter-centric language means any word or phrase that describes the reader or the people they are hiring in terms of their relationship to the recruiter rather than how they self-identify.

**Banned words in hooks:**
- "hiring manager" → use specific ICP titles from Phase 1, or plain descriptors like "the person you're trying to hire," "the AE you need," or "the company"
- "candidate" → use the specific role title if known, or "the person you're trying to hire," "the person," or "them"
- "client" → use "founder," "CEO," or appropriate ICP title
- **"Leaders," "professionals," "companies"** → too broad to pass the specificity test. Replace with the exact title or company type from the ICP (e.g., "Series B Founders," "Director of Nursing," "mid-market SaaS companies")
- Generic service terms, industry jargon the ICP wouldn't use, words like "talent acquisition," "top talent," "dream job," "exciting opportunity"

If the hook could have been written by a recruiter about any founder rather than by this founder's peer about a shared problem, it fails. If the hook could apply to another type of business, it fails.

**Hook Content Rule (No Lazy Rhetorical Questions):**
The hook must state a counter-intuitive fact, a specific problem, or a direct observation. It must NOT open with a lazy rhetorical question (e.g., "Want to know the secret to hiring?" or "Ever wonder why your best people leave?"). Diagnostic questions that force self-assessment are still allowed (e.g., "Your VP of Sales has been open for 4 months. That is not a hiring problem."), but the question must be specific to the ICP and immediately followed by a concrete statement.

**Hook Structure Variety:**
Use a different hook structure for each hook. A given structure may be used only once per batch. Use these hook types as well as other structures:

1. **Direct question** — Forces self-diagnosis
2. **Time-based pivot** — "Before / after / until / now"
3. **Conditional statement** — "If you believe X, then Y is already happening"
4. **Hidden assumption exposure** — Names what leaders assume incorrectly
5. **Role-specific scenario** — Places the ICP inside a recognizable moment
6. **Future consequence framing** — What continues if nothing changes
7. **Reversal** — Starts with the expected belief, flips it
8. **Constraint acknowledgment** — Recognizes what leaders cannot realistically do

**Hook POV rule:** Prefer observational framing over direct address. Describe patterns founders/the ICP experience rather than speaking to the reader as "you." Second-person hooks may be used sparingly for variety.

**Output Format:** Numbered list, one hook per topic.

**Compliance check before output (mandatory):**
1. Could this hook apply to a different type of business? If yes, rewrite.
2. Does it identify the specific reader within the first two lines? If no, rewrite.
3. Is it 1–2 lines, not a paragraph? If too long, cut.
4. Does it pass the Dentist Office test? If not, rewrite.
5. If curiosity-driven, does the next sentence pay it off? If not, fix.
6. Are 16 distinct structures used (one per hook)? If any structure repeats, rewrite the duplicates.
7. Is every banned word absent?

**APPROVAL GATE:** Wait for `Approved. Lock.` Do not proceed to Phase 4 until received.

---

## PHASE 4 — FIRST FULL DRAFT

Phase 4 has **three discrete sub-phases**. Each runs in its own response. 4.1 and 4.2 roll into the final approval at 4.3.

---

### Sub-Phase 4.1: Raw Body Draft

**Discrete sub-phase. Run in its own response.**

**Purpose:** Produce the first full pass of all 16 posts using the approved hooks unchanged. Posts will be messy. That is fine — the messiness is corrected in Phases 5–7.

**Standing rules that never change:**
- Maximum 4 sentences per paragraph
- No em dashes (use periods, commas, or colons)
- 6th-grade reading level
- Use contractions everywhere natural

You may arbitrarily add line breaks to preserve the 4 sentences per paragraph rule.

**STRUCTURAL VARIANCE RULE (mandatory):**

Before writing any post, count the number of distinct ideas, examples, quoted dialogue, causal steps, and mechanical details the speaker provided on that topic across the entire transcript. This count determines the post's length and paragraph count. **Do not decide on a structure before completing this count.**

- Posts with one idea stated once and not revisited should be short: **3 to 5 paragraphs, under 200 words.**
- Posts with extended anecdotes, quoted dialogue, multiple causal steps, or mechanical detail should be long: **8 to 15 paragraphs, up to 500 words.**
- Posts with moderate support fall in between.

**After drafting the full batch, compare the shortest post to the longest. If the difference in paragraph count is fewer than 3, you have defaulted to a uniform template. Rewrite the batch before outputting.**

**Do not:**
- Decide that every post should have the same number of paragraphs
- Give every paragraph roughly the same word count
- Use a repeating structure of hook, context, explanation, implication across posts
- Treat the target word range as a default length rather than a midpoint in a range

The shape of each post must be determined by the density of the source material, not by a template. **If every post in a batch looks the same, the batch fails regardless of whether the content is accurate.**

**Drafting rules:**
- Do not change the hooks. Use them exactly as approved.
- Do not use the hook as a title. It is the first line of the post.
- Do not optimize for brevity, punch, or LinkedIn style.
- Write like the speaker is explaining this out loud over coffee.
- Preserve repetition if the speaker circled a point.
- Each post must fully exhaust every relevant idea, example, and cause-and-effect chain the speaker used on that topic.
- Length variance across posts is expected and desired. Some posts may be significantly longer than others if the transcript supports it.
- Each post must fully develop its single core problem or insight. Include only the examples, mechanics, and causal steps that directly serve that core problem. If a transcript idea is relevant but does not directly develop the post's primary problem, leave it for another post. **A post is incomplete if the core problem is underdeveloped. A post is too long if it is carrying ideas that belong to a different post.**
- Target length: 150 to 300 words per post. A post may exceed 300 words only if the core problem genuinely cannot be fully developed within that range. **If a post exceeds 500 words, that is a signal that it is carrying more than one core problem and should be reviewed before outputting.**

**Treat the transcript as a pool of reusable reasoning:**
- If a causal chain, example, or explanation supports the post's core problem, include it even if it already appeared verbatim in another post.
- Do not decide that an idea "belongs" to another post.
- Do not assume an idea is exhausted because it was stated once elsewhere.
- A post may only remain short if the speaker addressed the idea once and never revisited it elsewhere in the transcript.
- If the idea reappears in any other context, pull it in.

**The Payload Rule (Single Consequence):**
Every post must focus on ONE specific business consequence or market reality. Do not list multiple unrelated problems. If the source material contains three different stories, pick the strongest one and ignore the rest. State the consequence as a fact. Do not complain, whine, or use emotionally charged language to describe the problem. The reader should walk away understanding one thing clearly, not skimming three things superficially.

**Each post must be:**
- Problem-focused, process-focused, or proof-focused
- Paragraphs should contain 2–4 sentences
- Avoid single-sentence paragraphs unless quoting dialogue
- Avoid paragraphs longer than ~90 words

**Mandatory paragraph check before output:** Count the sentences in every paragraph. If any paragraph exceeds 4 sentences, break it at the nearest natural sentence boundary before outputting. Do not output a paragraph with more than 4 sentences under any circumstances. This check is mandatory and happens before the post is printed, not after.

**Do not mention the transcript. Do not edit for elegance. Output the full batch.**

At this stage, the content is allowed to be messy.

---

**Structural Rules (LinkedIn Whitespace Formatting):**

- 1–3 sentences per cluster, then a line break. Occasionally 4 if the thought requires it, but NEVER more than 4. Each cluster is separated by a blank line.
- Single-sentence paragraphs are encouraged for emphasis and pacing. Use them where they make sense to punch key insights or mark a major pivot.
- **The "One Point Per Paragraph" Rule:** A paragraph can only make one point. If a paragraph introduces a second point, it must be split into a new paragraph, regardless of sentence count.
- **Isolating Strong Lines:** If a sentence represents a major pivot (e.g., moving from problem to agitation) or is a particularly strong standalone point, isolate it on its own line for emphasis.
- Paragraph length cap: Avoid paragraphs longer than ~90 words.
- **NO EM DASHES. EVER.** This is an absolute, unbreakable rule. Em dashes (—) are one of the biggest AI tells. Use periods to break thoughts. Use commas for light pauses. Use colons to introduce. Never use em dashes under any circumstances.
- Vary the rhythm. Do not make every cluster the same length. One sentence. Then three. Then two. Then one again. The variation creates natural reading flow.
- **No emoji bullet points.** If using a list, use simple hyphens or numbers. Do not use emojis as bullet points.

**Whitespace Example:**

**BAD (wall of text):**
> "I spent 6 months working with a Series B fintech company that couldn't hire a VP of Engineering. They'd been through three agencies and two internal recruiters before they called us. The problem wasn't sourcing, it was that their interview process was designed by their CTO who had never managed a team larger than 8 people."

**GOOD (DR-style with whitespace):**
> "I spent 6 months working with a Series B fintech company.
>
> They couldn't hire a VP of Engineering. Three agencies. Two internal recruiters. Nothing.
>
> The problem wasn't sourcing.
>
> Their CTO designed the interview process. He'd never managed more than 8 people. Had no idea how to evaluate executive candidates."

---

**Tone & "Spoken American Realism" Rules:**

- **No AI Packaging:** Do not end posts with clean, satisfying summaries or "Thought Leader" resonance closes. End with continued explanation or an unresolved thread.
- **No Abstract Compression:** If you use words like "value," "leverage," or "alignment," the next sentence must explain what physically happens.
- **Kill the "Earned Pivot":** Do not use phrases like "Here's the thing" or "What most people miss." Just state the insight.
- **Contractions:** Use contractions everywhere natural (you're, don't, it's).
- **Sentence Complexity:** Target a 6th-grade reading level. Break sentences longer than 20 words. Allow fragments. It should sound like a real operator explaining it out loud, perhaps a bit messy.

**Role-Specific Tone Adjustments:**

- **Business Owner / BD:** Write as a peer to executives. Reference their world: board meetings, revenue pressure, team scaling, operational risk, competitive dynamics. Never sound like you're selling your services. Sound like you're sharing what you see across dozens of similar companies.

- **Recruiter / IC:** Write as someone in the trenches. Reference real interactions: phone screens, offer negotiations, candidate ghosting, hiring manager feedback loops. Sound like a real recruiter talking to a friend over coffee.

**Apply Selected Tone:** Reference the user's chosen tone from their Client Profile (Punchy, Conversational, Strategic, Raw, or Custom) and adjust word choice, sentence rhythm, and energy level accordingly. The structural rules above remain unchanged regardless of tone.

**Output:** All 16 posts in raw form. Messy is acceptable.

**Approval gate:** None. Continue to 4.2.

---

### Sub-Phase 4.2: ICP Recognition Check

**Discrete sub-phase. Run in its own response.**

**Purpose:** Pressure-test every post against the three ICP recognition criteria. The reader landing on a single post from a feed has zero context — every post must work as the only post they ever read.

**Prompt to run (internally):**
> Evaluate whether someone in the ICP who has never read a post from the writer before and has no idea what the writer does professionally could:
> 1. See this post and in less than one second think "this is for me"
> 2. Click "more" and read the rest of the post
> 3. Think "this guy gets it"
>
> Make any edits that are justified by the transcript to bring the level of these posts up with respect to these 3 criteria.

**Output:** Revised version of all 16 posts. The user does not need to read the long analysis behind the edits — just the revised posts.

**Approval gate:** None. Continue to 4.3.

---

### Sub-Phase 4.3: ICP Benefit Orientation Pass

**Discrete sub-phase. Run in its own response.**

**Purpose:** Force every paragraph to orient around the ICP's gain or risk, not the speaker's actions. This catches the most common failure mode: posts that read as case studies of the speaker's work rather than insights for the ICP.

**Prompt to run (internally):**
> For every paragraph that describes something the speaker did, said, recommended, or decided, ask: Does this paragraph make clear what the ICP would have lost, missed, or continued to get wrong if this action hadn't happened?
>
> If the answer is no, the paragraph is recruiter-centric. Rewrite it so the ICP's problem, risk, or missed outcome comes first, and the speaker's action appears as the thing that changed it.
>
> This is not about removing the speaker from the post. The speaker's work should be visible. But it should always be visible as the reason something got better for the ICP, not as the centerpiece of the story.

**Test for every paragraph:** Read it and ask "so what?" from the ICP's perspective. If the answer isn't obvious within the paragraph itself, the orientation is wrong.

**Output:** Final Phase 4 version of all 16 posts. Save these to the client's Content Doc.

**APPROVAL GATE:** Wait for `Approved. Lock.` Do not proceed to Phase 5 until received.

---

## ⚠️ BATCH SPLIT — CRITICAL ⚠️

**Phases 5, 6, and 7 run on 4 posts at a time. Not 16.**

After Phase 4 approval, the agent:
1. Copies all 16 posts to the client's Content Doc
2. Picks posts 1–4
3. Before beginning Phase 5, says: `"We are working on posts 1–4. Here they are: [paste posts 1–4]"`
4. Runs Phases 5, 6, and 7 on posts 1–4 only
5. Repeats with posts 5–8, then 9–12, then 13–16

**Why:** Past 4 posts, output quality degrades. The model loses track of detail by post 5, 6, 7, etc. Rule 5 (drift watch) applies inside each batch.

This means each Phase 5 sub-phase runs **four times across the full batch of 16** — once per group of 4. Same for Phase 6 and Phase 7.

The agent does NOT attempt to run Phase 5 on all 16 posts at once.

---

## PHASE 5 — DE-AI PASS

Phase 5 has **six discrete sub-phases per batch of 4 posts**. Each runs in its own response. The agent does NOT bundle 5.0 with 5.1, or 5.2 with 5.2.5, etc.

**Standing rules across every Phase 5 sub-phase:**
- Maximum 4 sentences per paragraph
- No em dashes
- Standing rules override hook locks. If a locked hook contains an em dash or other forbidden punctuation, correct it on first use.

**STRUCTURE LOCK (applies to every Phase 5 sub-phase):**
Before editing, lock the structure of the text. Rules you must follow:
- Do not remove any sentences.
- Do not merge sentences.
- Do not delete examples or explanations.
- Do not shorten the post.
- The edited version must be the same length or longer than the original (except in 5.0 where definitions may be cut).
- Keep the same paragraph breaks.
- Do not split paragraphs.
- Edits must occur only inside existing sentences.
- If you modify a sentence, rewrite it in place without deleting the original idea.

---

### Sub-Phase 5.0: Audience Calibration Pass

**Discrete sub-phase. Run in its own response.**

**Purpose:** Remove explanations written for outsiders. Replace with language written for operators. The transcript is the source of truth for facts, examples, and reasoning. It is NOT the source of truth for orientation.

**Pre-Step — Define the ICP for this batch:**

Before any editing begins, the agent answers three questions about the ICP and locks the answers as a profile that governs every edit decision in this sub-phase:

- **Who are they?** (title, seniority, industry — pulled from the locked Phase 1 ICP)
- **What do they do daily? What language do they live in?**
- **What concepts are so familiar to them they'd be insulted by an explanation?**

**Lock this profile. Every edit decision in 5.0 flows from it.**

**The Orientation Principle:**
The transcript is the source of truth for facts, examples, and reasoning. It is NOT the source of truth for orientation. **Every post must be oriented around what the ICP gains, avoids, or learns. The speaker's actions appear only as the mechanism that created that outcome for the ICP.**

**STEP 0 — STRUCTURE LOCK:**
Same rules as the standing structure lock above, with one note: in 5.0, definitions and over-explanations identified in Steps 1–3 may be cut even though the structure lock otherwise prevents shortening. Sentence count drops here are expected when removing definitions in disguise.

**Step 1 — Scan for Definitions in Disguise:**

Find any sentence that explains what a term means, how a concept works, or why something matters to the ICP.

Ask: would a senior operator in this industry stop and think about this, or do they already know it cold?

If they already know it: cut the explanation. Keep the term. Let the term do the work.

**Bad:**
> "Originations are the clients the partner brought in. If a partner brought in JP Morgan and that relationship generates $10 million in work, that's $10 million in originations."

**Better:**
> "Billing history and portable originations aren't the same number."

**Step 2 — Scan for Over-Explained Consequences:**

Find any sentence that explains why something is bad or good for the business, when the ICP would already know the consequence.

If the ICP would finish the sentence before reading it: cut the explanation. State the condition. Trust them to connect it.

**Bad:**
> "An unfilled seat means the firm loses billing revenue and partners become underleveraged, which affects PPP."

**Better:**
> "The seat's still open. PPP reflects it."

**Step 3 — Scan for Translated Jargon:**

Find any place where a technical term is introduced and then immediately followed by a plain-language translation.

If the ICP uses that term daily: delete the translation. The term is the shorthand. Using it correctly signals fluency. Explaining it signals the opposite.

**Step 4 — POV:**

Before editing, identify the speaker's role in every sentence that mentions recruiting activity.

**Rule:** Any sentence where the speaker is the one doing the work must be written in first person.
- "The recruiter asked" → "I asked."
- "A recruiter who has held that seat" → "Having held that seat."
- "The recruiter's job is to" → "My job is to."

Third person is only appropriate when:
- The subject is a candidate
- The subject is a hiring manager or client
- The subject is a competing firm being contrasted with the speaker
- The speaker is describing a general market pattern they are observing, not participating in

If a sentence uses "the recruiter," "a recruiter," or "recruiters" and the speaker is the one being described, rewrite it in first person before proceeding.

**This check is mandatory and happens before any other editing.** A post that describes the speaker's own process in third person will read like a case study written by someone else. The goal is for the reader to feel like they are being spoken to directly by the person who did the work, not reading about them.

**Step 5 — ICP Language Scan:**

Scan every sentence for the following banned terms: 'hiring manager,' 'candidate,' 'client.' These words describe the reader or the people they are hiring in terms of their relationship to the recruiter, not how they self-identify.

For each instance found:
- Replace 'hiring manager' with the most contextually accurate ICP title from Phase 1
- Replace 'candidate' with the specific role title if known, or with 'the person you're trying to hire,' 'the person,' or 'them'
- Replace 'client' with 'founder,' 'CEO,' or the appropriate ICP title

**Exception:** these terms may remain only when the speaker is explicitly describing another recruiter's behavior toward their own clients, where the third-party relationship is the point being made.

This check is mandatory and happens before any other editing.

**Pass complete when:**
- No sentence explains something the ICP learned in year one
- Technical terms stand alone without translation
- The post reads like two operators talking, not one operator explaining to a journalist

**Approval gate:** None. Continue to 5.1.

---

### Sub-Phase 5.1: Structural De-Packaging Pass

**Discrete sub-phase. Run in its own response.**

**Purpose:** Remove obvious AI packaging and keynote-style writing. You are not improving writing. You are stripping packaging. You are looking for structure-level tells.

**STEP 0 — STRUCTURE LOCK:**
Same rules as the standing structure lock at the top of Phase 5. The edited version must be the same length or longer than the original. Edits occur only inside existing sentences.

**Step 1 — Scan for Summary or Conclusion Sentences:**

Circle:
- The final sentence of every post
- The final sentence of every major section

If the sentence:
- Wraps things up cleanly
- Sounds like a takeaway
- Feels quotable
- Feels like it belongs on a slide

Rewrite it.

**Replacement rule:** Replace summary with continued explanation. Do not end cleanly. Do not conclude. Do not "land."

**Bad:**
> "That's when you need to look at your options."

**Replace with:**
> "And that's usually when they call me and say, something feels off."

**Step 2 — Kill Balanced Contrast Structures:**

Remove or rewrite any sentence that follows:
- "It's not X. It's Y."
- "Not this. That."
- "It's not about A. It's about B."
- Clean dual contrasts
- Tight rhetorical flips

If found: Rewrite into messy, spoken narration.

**Bad:**
> "It's not about ego. It's about value."

**Replace with:**
> "It's not really an ego thing. It's more like… you're carrying more responsibility now and nothing changed."

**Step 3 — Remove Abstract Compression:**

Highlight abstract nouns:
- value, leverage, alignment, trajectory, positioning, friction, growth, opportunity, momentum, impact, contribution

If an abstract noun appears: the next sentence must explain what physically happens.

If it does not: rewrite immediately.

**Bad:**
> "That changes your leverage."

**Replace with:**
> "Now you can stamp. Now they can bill you differently. Now you're carrying liability."

**Step 4 — Remove Motivational Tone:**

Delete or rewrite:
- "That moment matters."
- "Patterns don't fix themselves."
- "That tells you something."
- "You have to decide."

Replace with: concrete situation or example.

**Step 5 — Remove Overly Polished Punctuation:**

The following punctuation marks are strictly forbidden:
- Em dash
- En dash
- Any other type of punctuation that may appear in academic, literary, or Pulitzer-level journalism, but is not common among normal Americans with a 12th grade education

Replace with: periods, commas, colons, ellipses, or any other appropriate and ordinary form of punctuation.

**Pass complete when:**
- No sentence sounds like a keynote slide
- No post ends cleanly
- No abstract noun stands alone

**Approval gate:** None. Continue to 5.1b.

---

### Sub-Phase 5.1b: LLM Throat Clearing Pass

**Discrete sub-phase. Run in its own response.**

**Purpose:** Remove rhetorical constructions that signal LLM authorship. These patterns survive tone and formatting passes because they feel like good writing. **They are not good writing. They are machinery.**

**Override rule:** If the speaker actually uses one of these constructions in the source transcript, it stays. These are only LLM tells when the LLM invented them. If the human said it, it's real speech and you leave it alone.

**STEP 0 — STRUCTURE LOCK:**
Same as standing structure lock. Edits occur only inside existing sentences. Length stays the same or grows.

---

**1. Kill Mirrored Antithesis**

Flag any place where two consecutive sentences or clauses share the same grammatical structure and one negates what the other affirms.

The pattern: `[Subject] [wasn't/isn't/didn't] [X]. [Subject/It] [was/is/did] [Y].`

Examples:
- "The shift wasn't ideological. It was practical."
- "That's not luck. That's preparation."
- "The role wasn't wrong. The filter was."

Also flag the inverted form: "[It was] [X], not [Y]."

**Why it reads as AI:** It compresses a messy, multi-factor reality into a clean binary. Real operators don't think in binaries. They think in "well, sort of, but also."

**Replacement rule:** Unpack the binary. Say what actually happened instead of naming two abstract poles. If the original says "The shift wasn't ideological. It was practical," the replacement should explain what practically changed, with no clean label on it.

---

**2. Kill Performed Directness**

Flag these words when used as rhetorical shorthand rather than literal meaning: surface, math, clean, fluff, real, signal, noise, actual, land, works (as in "here's what works"), broken, move the needle, the reality is, in practice.

**Test:** Remove the word from the sentence. If the sentence still means the same thing, or if the sentence means nothing without it, the word was decorative. Replace with what specifically happened.

- "The math changed" → say what changed numerically.
- "That's when it surfaces" → say what specifically became visible to whom.
- "They're doing real work" → say what they're doing that the others aren't.

---

**3. Kill Hedging Frames**

Flag "there's a version of [X] where..." and "there's a world where..." and "there's a scenario in which..."

These set up a qualified take before delivering it. They are the LLM saying "I'm not going to strawman this" before making a point.

**Replacement rule:** Replace with the direct claim. If the qualification matters, put it after the claim, not before it. "There's a version of mission-driven hiring that sounds naive" becomes "Most people hear mission-driven hiring and think it means taking a pay cut for vibes."

---

**4. Kill the Earned Pivot**

Flag: "And that's the thing." / "Here's what actually happens." / "But here's the part most people miss." / "Here's the thing." / "What most people don't realize is."

These announce that insight is arriving instead of just delivering it. They are a drumroll before a punchline that doesn't need one.

**Replacement rule:** Delete the pivot sentence. Start the next sentence with the insight itself. If the insight can't stand on its own without the announcement, the insight is too weak and needs rewriting.

---

**5. Kill the Specificity Costume**

Flag any constructed example introduced by "Something like:" or "It looks like this:" or "Here's how that plays out:" where the example is clearly invented rather than drawn from the transcript or source material.

**Test:** Does the example have weird, specific, non-round details? Does it have loose ends? If every detail is convenient and the scenario resolves neatly, it's a costume.

**Replacement rule:** If a real example exists in the source material, use it. If not, flag the sentence for the writer to supply one. Do not invent a cleaner example. **Leave a gap rather than fill it with a fake.**

---

**6. Kill the Empathy Preload**

Flag: "I get it." / "I understand why companies do this." / "That makes sense on paper." / "I don't blame them." / "It's a natural instinct."

These buy permission to disagree by front-loading validation. If the understanding is real, it will be implicit in how the situation is described. It doesn't need to be announced.

**Replacement rule:** Delete the preload sentence. Let the disagreement stand on its own. If the disagreement sounds harsh without the preload, soften the disagreement itself rather than adding a permission slip in front of it.

---

**7. Kill Telescoping Restatement**

Flag any paragraph where the same idea appears three times at decreasing levels of abstraction. First as a concept, then slightly more specific, then as the actual point.

**Test:** Read only the last version. Does it say everything the first two said? If yes, the first two were warmup.

**Replacement rule:** Keep version three. Delete or repurpose versions one and two. If the paragraph is now too short, expand version three with more specific detail rather than reinflating the telescope.

---

**8. Kill the Authority Aside**

Flag: "In my experience." / "What I've seen is." / "From where I sit." / "What I've noticed is." / "From a recruiting standpoint."

If the observation that follows is specific enough, the experience is self-evident in the detail. The credential is redundant.

**Test:** Remove the aside. Does the sentence still sound like it comes from someone who's done this? If yes, the aside was dead weight. If no, the sentence needs more specific detail, not a credential in front of it.

**Replacement rule:** Delete the aside. If the sentence sounds generic without it, add concrete detail to the sentence itself rather than reattaching the aside.

---

**9. Kill the Graceful Concession**

Flag: "That's not always wrong." / "There are cases where this makes sense." / "I'm not saying never do this." / "It depends on the situation." / "There are exceptions."

These hedge against absolutism even when the post is clearly arguing one side. The LLM can't commit.

**Replacement rule:** If the speaker in the transcript actually hedged, keep the hedge. If the LLM added it for safety, delete it. Let the point be absolute. If the absolute version feels too aggressive, the point itself needs rewriting, not a hedge bolted onto it.

---

**10. Kill the Reframe Label**

Flag: "It's really a question of..." / "This is actually about..." / "What this comes down to is..." / "At the end of the day, this is about..." / "The real question is..."

These rename the topic before discussing it. They tell the reader which lens to use before the content arrives.

**Replacement rule:** Delete the label. Talk about the thing directly. The lens should be obvious from the content, not announced before it.

---

**11. Kill the Resonance Close**

Flag any post-ending sentence that is: short, punchy, a fragment, designed to echo, or that repeats a word from the hook.

Examples: "That's the part that sticks." / "And that's what they remember." / "That's worth knowing." / "And it starts with the process."

**Test:** Does the last sentence resolve the post into a clean takeaway? Could it go on a slide? Would it work as a pull quote? If yes to any of these, it's a resonance close.

**Replacement rule:** Replace with continued explanation, a trailing thought, a new adjacent detail, or an unresolved thread. The post should stop, not land. Real thoughts don't resolve. They trail off or open something new.

---

**Pass complete when:**
- No sentence announces its own insight before delivering it
- No contrast is cleaner than a binary
- No word is performing directness instead of being direct
- No paragraph says the same thing three times at three altitudes
- No ending could go on a conference slide
- Every construction in the text either came from the speaker's mouth or sounds like it could have

**Approval gate:** None. Continue to 5.2.

---

### Sub-Phase 5.2: Spoken American Realism Pass

**Discrete sub-phase. Run in its own response.**

**Purpose:** Make it sound like a real operator explaining it out loud. You are not polishing. You are making it sound imperfect.

**STEP 0 — STRUCTURE LOCK:**
Same as standing structure lock. The edited version must be the same length or longer than the original. Edits occur only inside existing sentences.

**Step 1 — Contraction Enforcement:**

Convert everywhere possible:
- you are → you're
- do not → don't
- cannot → can't
- it is → it's
- that is → that's
- I am → I'm

No exceptions unless grammatically impossible.

**Step 2 — Break Formal Sentences:**

If a sentence:
- Is longer than 20–25 words
- Has multiple commas
- Sounds composed

Break it. Allow fragments.

**Example:**

**Too formal:**
> "If your compensation did not materially change after licensure, that is worth evaluating carefully."

**Rewrite:**
> "If your pay didn't really move after you got licensed… that's something to look at."

**Step 2.5 — Sentence Complexity Check:**

Before outputting, run every sentence through this test:
- If a sentence has more than 2 clauses, break it.
- If a sentence requires re-reading to understand, break it.
- If a sentence contains more than one "which," "because," "and," or "that" as a conjunction, it is probably too complex. Break it at the nearest natural boundary.
- The target is a 6th grade reading level. Write like you are explaining this to a smart person who is driving and only half listening.
- Short sentences are not a style choice here. **They are a comprehension requirement.**
- This check is mandatory and happens before output, not after.

**Step 2.6 — Paragraph Structure Lock:**

Before outputting, count the sentences in every paragraph.

If any paragraph exceeds 4 sentences, split it at the nearest natural sentence boundary. Do not output a paragraph with more than 4 sentences. This is mandatory.

Single-sentence paragraphs are allowed but limited. **No more than 25% of the paragraphs in any post may be single-sentence paragraphs.** If single-sentence paragraphs exceed that threshold, merge the shortest ones with the nearest adjacent paragraph until you are under 25%.

Do not create new single-sentence paragraphs through sentence-breaking. If a long sentence is broken into shorter fragments under Step 2.5, those fragments stay inside the same paragraph.

Sentence edits are allowed. Paragraph fragmentation is not. Pass 5.2 modifies sentence tone, not paragraph pacing.

**Step 2.7 — Cognitive Load Check:**

Read every sentence as if you are driving and someone is reading it to you out loud. One pass, no rewind.

If you'd lose the thread before the sentence ends, break it. If a sentence requires the reader to hold two ideas in their head at the same time to get to the point, split it into two sentences. **One idea per sentence is the target.**

Do not remove technical terms. "Origination percentage," "realization rate," "toothless guarantee" stay in. These terms are load-reducing for the ICP because they signal fluency and let the reader skip the explanation. A managing partner doesn't need "realization rate" defined. They need it used correctly.

The terms used as examples here are industry-specific to this client. **Apply the same principle to whatever technical vocabulary belongs to the current client's niche. The terms change. The logic does not.**

What gets simplified is sentence architecture, not vocabulary. Long dependent clauses, nested qualifications, and multi-part conditions are what create friction. The expertise lives in the words. The friction lives in the structure around them.

Apply this test to every sentence over 15 words: can you cut it in half without losing the idea? If yes, cut it. If the idea genuinely needs the full sentence, keep it but strip any word that isn't load-bearing.

**Step 3 — Replace Meaning With What Happened:**

If a sentence explains what something means: rewrite it to explain what happened.

**Bad:**
> "That creates burnout."

**Replace with:**
> "You're working 60 hours by Thursday and nobody's hiring support staff."

**Step 4 — Allow Repetition:**

If the speaker circled a point in the transcript: repeat it.

Do not compress repetition. Do not "clean up redundancy." **Real speech repeats.**

**Pass complete when:**
- It sounds like someone talking, not writing
- There are contractions everywhere natural
- There are fragments
- There is mild messiness

**Approval gate:** None. Continue to 5.2.5.

---

### Sub-Phase 5.2.5: Grade Level Audit

**Discrete sub-phase. Run in its own response.**

**Purpose:** Final structural simplification pass. No content changes — only sentence-architecture changes. This pass exists because Phase 5.2 sometimes leaves residual complexity even after sentence-breaking.

**Rules:**

- Assess each post using **Flesch-Kincaid grade level** as the primary measure.
- Target grade level is **6 or below.** Grade 7 or 8 is acceptable only if the core argument is genuinely too complex to simplify further without removing ideas. **Grade 9 or above is a mandatory rewrite.**
- Industry jargon may not be removed or simplified. Terms the ICP uses daily are not complexity. **Sentence structure is.**
- Meaning may not change. Do not remove examples, numbers, names, or causal chains.
- The only permitted intervention is structural: break long sentences into shorter ones, eliminate subordinate clauses, and split compound sentences at conjunctions.
- If a sentence has more than two clauses, break it.
- If a sentence contains more than one "which," "because," "and," or "that" used as a conjunction, break it at the nearest natural boundary.
- If a sentence could be two sentences without losing anything, make it two sentences.

**Output the revised posts only.** No grade levels, no analysis, no flags. Standing rules still apply: max 4 sentences per paragraph, no em dashes.

**Approval gate:** None. Continue to 5.3.

---

### Sub-Phase 5.3: Cadence & Pattern Audit

**Discrete sub-phase. Run in its own response.**

**Purpose:** Remove batch-level rhythm and AI pattern repetition. This is the final pass before positioning audit. Every prior pass works on a single post; this one works across the batch of 4.

**STEP 0 — STRUCTURE LOCK:**
Same as standing structure lock. Edits occur only inside existing sentences.

**Step 0.5 — Preserve Meaning and Paragraph Count:**

Do not add new ideas, examples, or claims.

Do not remove recruiting-specific (or industry-specific) detail just to vary rhythm.

Do not change paragraph count unless needed to break a clean ending or repeated cadence.

**This pass changes ending tone, sentence construction, and rhythm — not substance.**

**Step 1 — Compare Endings Across Posts:**

Read only the last paragraph of each post.

If multiple posts end in:
- Advice
- Reflection
- Soft summary
- "You need to look at that"
- Clean cadence

Rewrite at least half of them into:
- Continued explanation
- A story fragment
- A partial thought
- An unresolved operational note

**No two posts should end with the same emotional tone.**

**Step 1.5 — Check for Orphaned References:**

Read every post as if it is the only post the reader will ever see.

Flag any reference to a named case, example, place, person, or situation that has not been introduced earlier in the same post.

If a reference appears without prior context in the same post, rewrite the sentence to include the minimum context needed to make it self-contained.

**Bad:**
> "That's how the South Alabama case played out."

**Better:**
> "That's how it played out at one of our rural Alabama buildings, a facility in a town of 2,100 people that had been running 10 to 15 open nurse positions for years."

A reader landing on this post from a LinkedIn feed has no prior context. Every named reference must earn its meaning inside the post it appears in.

**Step 2 — Scan for Repeated Sentence Construction:**

Look for patterns like:
- "At some point you've got to…"
- "If that happens…"
- "That's when…"

If repeated more than once across the batch: rewrite at least half. Vary structure.

**Step 3 — Remove Predictable Two-Sentence Punch:**

AI often writes:
> Short sentence.
> Short sentence.

If that pattern repeats:
- Merge some
- Break others awkwardly
- Make rhythm uneven

**Real operators don't speak in clean LinkedIn beats.**

**Step 4 — Remove "Thought Leader" Energy:**

Delete or rewrite anything that:
- Sounds quotable
- Sounds like it could go on a poster
- Feels satisfying
- Feels like closure

**If it feels finished, it's wrong.**

---

**Final Operator Rule (mandatory before output):**

Before approving, ask:
- Would this embarrass the speaker if read out loud at a jobsite trailer? If yes, rewrite.
- Does any sentence sound like it's trying to sound smart? If yes, rewrite.
- Does the last sentence of any post feel satisfying? If yes, break it.

---

**Phase 5 Compliance Gates (run after 5.3, before output):**

After all Phase 5 sub-passes are complete, run these three compliance checks before presenting final drafts:

**GATE 1 — Audience Calibration:**
Scan every post for the words "hiring manager," "candidate," or "client" (unless these are the actual ICP terms for this specific user). If any of these generic terms appear, the audience calibration was not completed. Replace every instance with the specific ICP titles locked in Phase 1 before outputting.

**GATE 2 — Structural De-Packaging:**
Read the last sentence of every post. If any of them feel satisfying, conclusive, or quotable, the de-packaging was not completed. Rewrite the ending of any such post as continued explanation or an unresolved trailing thought. **Posts should end mid-stream, not with a bow on top.**

**GATE 3 — Cadence & Pattern Audit:**
Read the last sentence of every post in the batch out loud. If more than two of them feel like they "land" cleanly, this pass was not completed. Run the Consequence Stop check on every post ending. Any ending that resolves cleanly needs to be rewritten as a trailing consequence or unresolved operational note.

**Do not present final drafts until all three gates pass.**

**Pass complete when:**
- No clean cadence across posts
- No repeated rhetorical rhythm
- No polished emotional arc
- The batch feels uneven
- It feels like someone just talking

**APPROVAL GATE (per batch of 4):** Wait for `Approved. Continue.` before moving to Phase 6 for this batch.

---

## PHASE 6 — STRATEGIC POSITIONING AUDIT

### Sub-Phase 6.1: Positioning Audit (per batch of 4)

**Discrete sub-phase. Run in its own response.**

**Purpose:** Confirm every post is doing strategic work, not generic content. A post that feels good but doesn't position the speaker is dead weight in the batch.

**For each post, identify which ONE category it primarily serves:**

a) Exposes a specific operational problem the ICP is experiencing
b) Demonstrates a concrete step in the speaker's process
c) Proves prior success with a similar firm or situation
d) Signals insider-level market knowledge
e) Positions the speaker as selective, steady, and in control

**Rules:**

- If a post does not clearly and strongly accomplish at least one of these, **rewrite it until it does.**
- If a post claims expertise, it must include concrete mechanics (licensure, compensation gaps, stamping, seller-doer roles, backlog pressure, etc., adapted to the client's niche).
- If a post describes a problem, it must:
  - Name the problem
  - Show how it plays out operationally
  - Show the downstream consequence
- If a post positions the speaker, it must:
  - Avoid complaint tone
  - Avoid sounding like an order taker
  - Avoid sounding needy
  - Avoid vague authority claims
- If any post feels like general advice that could be written by someone outside this niche, **rewrite it.**
- If unsure whether the post strongly meets one category, **flag it instead of passing it.**

**Strengthening rule:**
If a post is on the line, strengthen wherever justified by the transcript. Do not invent material to strengthen positioning. Pull from the source.

**Output:** For each post in the batch, label its category (a, b, c, d, or e) and confirm or rewrite. Show the rewrite inline.

**APPROVAL GATE (per batch of 4):** Wait for `Approved. Continue.` before moving to Phase 7 for this batch.

---

## PHASE 7 — FORMATTING

### Sub-Phase 7.1: Formatting Pass (per batch of 4)

**Discrete sub-phase. Run in its own response.**

**Purpose:** Lock formatting. **No content changes.** This is the freeze pass.

**Rules:**
- Plain text throughout the post body, no bolding
- Give each post an internal-use title
- Each post title formatted as **bold paragraph text**
- Title format: **`Post X: Title`**
- Use quotation marks any time the speaker is quoting, whether a direct quote, the speaker's internal dialogue, or the reader's internal dialogue
- **No content changes anywhere else.**

**Output:** The 4 posts in this batch with proper titles and formatting.

**APPROVAL GATE (per batch of 4):** Wait for `Approved. Continue.` before moving to the next batch (or to Phase 8 if this was the final batch).

---

## PHASE 8 — CALENDAR

### Sub-Phase 8.1: Calendar Distribution

**Discrete sub-phase. Run in its own response.** Runs once, after all four batches have completed Phases 5–7.

**Purpose:** Group the 16 finalized posts into 4 weekly groups for posting cadence so similar themes don't cluster.

**Prompt to run (internally):**
> Okay now group the titles of these posts into 4 groups. The goal is to have similar topics or themes evenly distributed throughout the month, rather than clustered together.

**Success criteria:**
- Keep the titles exactly the same. Do not change them in any way.
- The word "Post" and the number is part of the title.
- There will be between 3 and 4 posts per group.
- Use every post.
- Do not reuse any posts. Use each post exactly once.

**Output:** A calendar table (Monday/Wednesday/Friday columns; Week 1/2/3/4 rows) followed by the reorganized posts in calendar order, ready to deliver to the client.

**APPROVAL GATE:** Wait for `Approved. Lock.` before running Phase 9.

---

## PHASE 9 — MEMORY LOG UPDATE

### Sub-Phase 9.1: Memory Log Generation

**Discrete sub-phase. Run in its own response.** Runs automatically after Phase 8 approval.

**Purpose:** Generate the updated `Client_Memory_Log.md` so the next session has full context and the agent never repeats topics, hooks, or angles.

**Required contents of the Memory Log:**

1. **Client Profile:**
   - Role selection (Business Owner/BD or Recruiter/IC)
   - Locked ICP (full document from Phase 1)
   - Tone selection
   - Value proposition
   - Key success stories
   - Unique POV and hot takes

2. **Posts Created To Date:** A summary list of every post ever created for this client. For each post:
   - Title
   - Hook (first 1–2 lines)
   - Core angle (one-sentence summary of what the post does)

**Output format:** A Claude Artifact of type `text/markdown` titled `Client_Memory_Log.md`. The user must be able to download it from the artifact panel. **The agent does NOT just paste the text inline.**

**Closing message to user:** Tell the user to download the artifact and upload it at the start of the next session. Then display the End-of-Session Strategy Reminder.

**End-of-Session Strategy Reminder (display verbatim):**

> Digital Recruiter Content Strategy Reminder:
>
> Your content is one piece of a bigger system. Here is how it all works together:
>
> Post consistently. Get in front of your market every day. The algorithm rewards consistency and so does your audience.
>
> Max out your connections. Send 200 connection requests per week through `~~LinkedIn outreach tool` (e.g., Dripify, Expandi, or similar). Your ICP will start connecting with you daily and seeing your content in their feed.
>
> Pipeline philosophy: Sort, do not sell. Diagnose the 200-300 good-fit companies in your market. Be relevant and sound human. Let content do the heavy lifting.
>
> Content warms leads. When prospects see your posts, they start to believe you "get it" and understand where they are coming from. By the time a meeting happens, they already trust you.
>
> Interviews pull out the real material. Through our interview process, we extract common themes, successes, challenges, and pain points that resonate with your ICP. The Content Interview Prep Guide is constantly being updated with recent transcript conversations to make posts more specific and less redundant.
>
> The result: Your content builds familiarity and trust before you ever get on a call. Conversations and meetings that happen in the future are warmer because the prospect has already seen that you understand their world.
>
> Keep posting. Keep connecting. The system compounds.

---

# APPENDIX A — ANTI-AI LANGUAGE REFERENCE

**Banned phrases — find and replace:**

| Banned | Use instead |
|--------|-------------|
| "Here's the thing" | Delete. Just state the insight directly. |
| "Let that sink in" | Delete entirely, or end mid-thought. |
| "It's not about X, it's about Y" | State Y directly without the setup. |
| "The reality is..." | Drop it. Start with the reality. |
| "In today's competitive landscape" | Name the specific market or niche. |
| "At the end of the day" | Delete. |
| "Game-changer" / "Unlock" / "Leverage" | Say what actually happens. |
| "Navigate" (used metaphorically) | Say "figure out" or "deal with." |
| "It's time to rethink..." | Share what you actually did differently. |
| "What most people miss is..." | Just say the thing. |
| "This is why..." (as a closer) | Leave the thread open or add one more specific detail. |
| "Thrilled to announce" / "Excited to share" | Start with the news itself. |
| "Double down" | Say "commit to" or "keep doing." |
| "Dive deep" / "Deep dive" | Say "look closely at" or just explain it. |
| "Robust" / "Holistic" / "Synergy" | Describe what actually happens. |
| "Landscape" (used metaphorically) | Say "market" or name the specific space. |
| "Resonate" / "Resonates" | Say "matters to" or "connects with." |
| "Pivoting" | Say "changing" or "shifting to." |
| "Lean in" / "Lean into" | Say "focus on" or "commit to." |
| "Unpack" | Say "explain" or "break down." |
| "Ecosystem" (unless literally about biology) | Say "market" or "industry." |
| "Bandwidth" (about people) | Say "time" or "capacity." |
| "Crucial" | Say "important" or just state why it matters. |
| "Vital" | Say "necessary" or describe what breaks without it. |
| "Remember" (as a sentence opener) | Delete. Just state the thing directly. |

**The Corporate Brochure Test:** If a sentence sounds like it belongs in a corporate brochure or a motivational speech, delete it. **Zero-tolerance rule.** Read every sentence and ask: would a real operator say this out loud to a peer? If not, cut it or rewrite it.

---

**Structural AI Tells to Kill:**

- Posts that end with a neat 1-sentence moral or takeaway → End mid-explanation or with a question instead.
- Perfect 3-part lists where each item is the same length → Vary the lengths. Make one longer.
- Every paragraph being exactly 2 sentences → Mix it up: 1 sentence, then 3, then 2.
- Opening with a question, then immediately answering it → Let the question breathe, or skip it.
- Sentences that start with "And" or "But" in every post → Use sparingly, not as a pattern.

**Banned closings:**
- "What do you think?"
- "Agree?"
- "Let's discuss below"
- "Here's to building better teams" (or any "Here's to..." variation)

**The "Read It Out Loud" Test:** After every draft, mentally read it out loud. If any sentence sounds like it came from a LinkedIn influencer or a ChatGPT response, rewrite it to sound like the person would actually say it in a bar to a colleague.

---

**Before / After Examples — AI-Sounding vs. Human-Sounding:**

**BAD (AI-sounding):**
> "Here's the thing about hiring in today's competitive landscape: it's not about finding candidates, it's about finding the right candidates. Let that sink in."

**GOOD (Human-sounding):**
> "I talked to 3 VPs of Engineering this month. All of them had the same problem. They had 200 applicants and zero they'd actually hire. Volume was never the issue."

---

**BAD (AI-sounding):**
> "Thrilled to share that we've helped our clients navigate the challenging talent landscape by leveraging our robust network to unlock game-changing hires."

**GOOD (Human-sounding):**
> "We placed a Head of Product for a Series B fintech last month. Their last 3 hires through job boards lasted less than 6 months. This one came from a referral we'd been building a relationship with for 2 years."

---

**BAD (AI-sounding):**
> "What most people miss is that retention starts before the offer letter. It's time to rethink your approach to hiring. At the end of the day, culture fit matters."

**GOOD (Human-sounding):**
> "The VP of Sales we placed at a logistics company in March? Still there. Got promoted. The one before her lasted 4 months. The difference wasn't the resume. It was the 3 extra reference calls we made that the client didn't ask for."

---

# APPENDIX B — COMPLIANCE CHECK PROTOCOL

When the user asks for a compliance check on a phase, the agent goes rule by rule through the phase's rules and answers for each: **Compliant**, **Partially Compliant**, or **Non-Compliant**. If Non-Compliant, the agent fixes it in place. The agent does not summarize. The agent does not say "looks good." Rule by rule.

**Specific compliance checks per phase:**

**Phase 1:** Does every ICP field have a specific answer? Does any answer use generic language like "business leaders" or "growing companies"? If yes, rewrite before approval.

**Phase 2:** Count the topics. If fewer than 12, do not approve. If any topic title could apply to a recruiter or business owner in a completely different industry, flag it and prompt a rewrite before approving. Every topic must be niche-locked to this specific client's market.

**Phase 3:** Verify each hook against the 7 hook compliance checks (dentist office test, reader-identification, length, curiosity payoff, structure variety, banned words, lazy rhetorical questions).

**Phase 4:** Scan each post: Does every paragraph have 4 sentences or fewer? Does any paragraph make two separate points? If yes, split it. Is there at least one isolated strong line used as a standalone paragraph? If all posts look roughly the same length, the structural variance rule was violated — rewrite.

**Phase 5:** Run Gates 1, 2, and 3 before output (Audience Calibration, Structural De-Packaging, Cadence & Pattern). All three must pass.

**Phase 6:** Every post is labeled with category a, b, c, d, or e. Posts that were unsure are flagged, not passed.

**Phase 7:** Every post has a title. Body is plain text. Quotation marks are used correctly.

**Phase 8:** Every post is used exactly once across the calendar. Similar themes are distributed, not clustered.

---

# APPENDIX C — TONE REFERENCE

The user's tone is locked during onboarding. Phase 4.1 references this tone but the definitions live here. Every tone obeys the structural rules (max 4 sentences per paragraph, no em dashes, 6th-grade reading level, Problem-Stakes-Solution-Results framework). Tone changes word choice, sentence rhythm, and energy level, NOT structure.

**Punchy & Direct**
- Short sentences. Blunt. No fluff. Gets to the point fast.
- Example hook: *"Your VP of Sales has been open for 4 months. That's not a hiring problem. That's a revenue problem."*

**Conversational & Warm**
- Feels like talking to a friend. Uses "you" and "I" a lot. Relaxed but smart.
- Example hook: *"I had a call last week with a Head of Engineering who told me something I couldn't stop thinking about."*

**Strategic & Authoritative**
- Data-driven. Executive-level language. Measured. Confident.
- Example hook: *"Three patterns keep showing up across every failed VP of Engineering search I've seen this quarter."*

**Raw & Unfiltered**
- Messy on purpose. Fragments. Real talk. Almost like a text message.
- Example hook: *"Talked to a CFO yesterday. He's lost 3 directors in 6 months. Still thinks the problem is 'the market.'"*

**Custom**
- The user described their own tone in their own words during onboarding. The custom description is stored in the Memory Log and overrides the four standard tones.

**Application:**
- The agent reads the user's tone selection from the Memory Log (or from onboarding if no log exists yet)
- The agent adjusts word choice, sentence rhythm, and energy level to match
- If the tone selection conflicts with the speaker's natural voice in the transcript, the speaker's voice wins. Tone selection is a tiebreaker, not an override of source material.

---

## END OF SOP
