DIGITAL RECRUITER — COWORK MODE SOP

Version: 2.1
Purpose: This SOP defines how the agent operates when the operator invokes it in Claude Cowork. Cowork is an autonomous execution environment, which means the agent runs without operator-in-the-loop approval gates between most phases. This SOP defines exactly which gates remain, what triggers them, and how the agent reports back.

Cowork Mode is OPTIONAL. It exists for operators who don't want to sit at the screen typing approvals for an hour straight. They want to launch a batch, walk away, get pinged at a checkpoint, approve from their phone or laptop whenever they get to it, then walk away again. Same single operator, same single persona, just async.

The default in claude.ai is Standard Mode (full gates) or Express Mode (bundled gates) per the Content Creation SOP. Cowork Mode is a third tier built specifically for async use in the Cowork environment.

VERSION 2.1 NOTE: This SOP supersedes v1.0 and v2.0. v1.0 placed both checkpoints upstream of Phase 5, leaving the highest-failure zone running with no operator visibility. v2.0 added a third checkpoint and over-corrected. v2.1 settles on two checkpoints, both positioned where Phase 5 actually fails, with the option to add a final review for high-stakes runs.

═══════════════════════════════════════════════════════════════
WHEN TO USE COWORK MODE
═══════════════════════════════════════════════════════════════

Cowork Mode is appropriate when:
- The operator has shipped at least 3 prior batches in Standard or Express Mode
- The Memory Log is rich (locked ICP, voice notes captured, prior themes tagged)
- The source transcript is clean and substantial (15+ minutes of dense material, or a thorough intake form)
- The operator wants to run the batch without sitting at the screen continuously

Cowork Mode is NOT appropriate when:
- The operator is brand new with no Memory Log yet
- The source material is thin, vague, or the agent has flagged source-quality concerns
- The batch is high-stakes (launch content, sensitive topic) — though the operator can opt into a final review checkpoint to make Cowork acceptable for those runs
- The operator has not validated the engine on at least one Standard Mode batch first

If an operator asks for Cowork Mode but the criteria aren't met, the agent should respond:
"Cowork Mode is built for operators with rich Memory Logs and substantial source material. Right now I'd recommend Standard or Express Mode in claude.ai because [specific reason]. Want to proceed with that instead, or do you want me to run Cowork Mode anyway?"

The operator can override the recommendation. The agent cannot self-override.

═══════════════════════════════════════════════════════════════
THE COWORK MODE PHASE MAP (v2.1)
═══════════════════════════════════════════════════════════════

| Phase | Sub-Phase | Standard | Express | Cowork v2.1 |
|-------|-----------|----------|---------|-------------|
| 0 | 0.1 Source Lock-In | No (ack only) | No (ack only) | AUTO |
| 1 | 1.1 ICP Confirmation | HARD GATE | HARD GATE | AUTO-PASS (Memory Log) |
| 2 | 2.0 Topic Qualification | rolls to 2.3 | bundled | AUTO |
| 2 | 2.1 Atomic vs. System Split | rolls to 2.3 | bundled | AUTO |
| 2 | 2.2 Concrete Subject Check | rolls to 2.3 | bundled | AUTO |
| 2 | 2.3 Differentiation Audit | HARD GATE | HARD GATE | AUTO |
| 3 | 3.1 Hooks Pass | HARD GATE | HARD GATE | AUTO |
| 4 | 4.1 Raw Body Draft | rolls to 4.3 | bundled | AUTO |
| 4 | 4.2 ICP Recognition Check | rolls to 4.3 | bundled | AUTO |
| 4 | 4.3 ICP Benefit Orientation | HARD GATE | HARD GATE | **CHECKPOINT 1** |
| — | — | BATCH SPLIT — Phases 5-7 run on 4 posts at a time | — | — |
| 5 | 5.0 Audience Calibration | No | bundled | AUTO |
| 5 | 5.1 Structural De-Packaging | No | bundled | AUTO |
| 5 | 5.1b LLM Throat Clearing | No | bundled | AUTO |
| 5 | 5.2 Spoken American Realism | No | bundled | AUTO |
| 5 | 5.2.5 Grade Level Audit | No | bundled | AUTO |
| 5 | 5.3 Cadence & Pattern Audit | YES per batch | bundled | AUTO |
| 6 | 6.1 Strategic Positioning | YES per batch | bundled | AUTO |
| 7 | 7.1 Formatting Pass | YES per batch | HARD GATE per batch | **CHECKPOINT 2** (posts 1-4 only) |
| — | — | Posts 5-8, 9-12, 13-16 + Phase 8 run autonomously after Checkpoint 2 | — | — |
| 8 | 8.1 Calendar Distribution | HARD GATE | HARD GATE | AUTO (or OPTIONAL CHECKPOINT 3 if requested) |
| 9 | 9.1 Memory Log Update | Auto | Auto | AUTO |

Total checkpoints in Cowork Mode v2.1: **2 default**. **3 if the operator opts into a final review at run start.**

WHY THIS PLACEMENT: The de-AI passes (5.0–5.3) plus positioning (6.1) and formatting (7.1) are where the engine ships AI-sounding posts. Failures cluster around three modes:
1. Voice mismatch — the polished post drifts from the operator's actual phrases captured in the Memory Log
2. AI-tells residue — em dashes, "Here's the thing," and clean satisfying endings survive sub-pass 5.1b
3. Specificity loss — concrete numbers, names, and situations from the source soften into generic claims during the cadence audit (5.3)

Earlier versions of this SOP put the checkpoints upstream of Phase 5 and caught none of these. v2.1 puts a calibration checkpoint after the first batch of 4 finished posts (Checkpoint 2) so the operator can confirm the de-AI passes are tuned correctly before the agent runs them on the remaining 12.

═══════════════════════════════════════════════════════════════
CHECKPOINT 1 — AFTER PHASE 4 (Combined Upstream Review)
═══════════════════════════════════════════════════════════════

The agent runs Phases 0, 1, 2, 3, and 4 autonomously, including all sub-phases. At Phase 4.3 completion, the agent STOPS and outputs:

DELIVERABLE AT CHECKPOINT 1:
1. The locked ICP being used (one paragraph confirming what the agent loaded from the Memory Log)
2. The 12-16 approved topics with theme tags AND brief angle notes (so the operator can spot duplicates against their gut sense of past batches)
3. The 12-16 hooks (one per topic), formatted clearly
4. The 12-16 raw drafts (post-Phase 4.3), in the same numbered order as the topics and hooks
5. A FLAGS section listing any decisions the agent made conservatively:
   - Topics where the theme tag was carried over from the previous batch (max 1 allowed)
   - Topics where the angle was unusual or borderline duplicated against past Memory Log entries
   - Hooks that the agent had to rewrite multiple times to pass the Dentist Office test
   - Phase 4.2 recognition checks where the agent edited the draft substantially to land the ICP
   - Phase 4.3 benefit orientation rewrites that materially changed the post's argument
   - Posts exceeding 500 words (signal that more than one core problem may be embedded)
   - Posts where the source supported less than 200 words and the agent had to keep them short
   - Any source material gaps the agent worked around

The agent then waits for one of three operator responses:
- "Continue" or "Approved. Continue." — proceed to Phase 5 on posts 1-4 autonomously
- "Stop and revise [specific items]" — agent rewrites only the flagged items at the appropriate phase and re-presents Checkpoint 1
- "Cancel" — agent stops the run, generates a partial Memory Log, and exits

If the operator does not respond, the agent does NOT proceed. Silence is a hard stop.

DESIGN NOTE: Showing topics, hooks, and drafts together at one gate is intentional. It's the cheapest layer where voice, ICP, and topic drift are all visible. Hooks alone hide voice problems; topics alone hide angle problems; drafts surface both. One review covers Phases 2, 3, and 4.

═══════════════════════════════════════════════════════════════
CHECKPOINT 2 — AFTER FIRST BATCH OF 4 (De-AI Calibration Review)
═══════════════════════════════════════════════════════════════

After "Continue" at Checkpoint 1, the agent runs the full Phase 5 + 6.1 + 7.1 chain on posts 1-4 only. At completion of post 4's formatting pass, the agent STOPS and outputs:

DELIVERABLE AT CHECKPOINT 2:
1. Posts 1-4 in their fully finalized form (post-de-AI, post-positioning, post-formatting)
2. For each of the four posts, a CALIBRATION CARD with three explicit reads:

   a. VOICE MATCH:
      - List the specific phrases pulled from the Memory Log voice notes that landed in this post
      - List any sentences where the agent chose phrasing that wasn't in the voice notes (and why)
      - Verdict: matches operator voice / needs voice rework

   b. AI-TELLS RESIDUE:
      - Confirm zero em dashes
      - List any phrasings 5.1b flagged but kept (e.g., a borderline "Here's the thing" the agent decided was load-bearing)
      - Confirm the ending was rewritten away from clean-satisfying-summary patterns
      - Verdict: clean / borderline / contains residue

   c. SPECIFICITY PRESERVATION:
      - List concrete details from the source that survived into the final post (numbers, names, situations)
      - List concrete details that were softened or dropped during 5.0-5.3 (and why)
      - Verdict: concrete / partially generalized / drifted to generic

3. A BATCH FLAGS section listing any sub-pass that did substantial rewriting (e.g., "5.1b killed mirrored antithesis in para 3 of post 2; 5.3 rewrote the ending of post 4")

4. The agent's own assessment: "These four are calibrated. Run the same passes on posts 5-16 with confidence." OR "Posts [X] and [Y] needed concessions in [voice / AI-tells / specificity]. Recommend revising before I run the same passes on the remaining 12."

The operator then chooses:
- "Continue" — agent runs Phase 5 + 6.1 + 7.1 on posts 5-8, 9-12, 13-16 autonomously, then Phase 8 (Calendar), then Phase 9 (Memory Log), and delivers final output. (If the operator opted into Checkpoint 3 at run start, the agent stops at Checkpoint 3 instead.)
- "Stop and revise [specific items]" — agent rewrites flagged items at the appropriate sub-phase and re-presents Checkpoint 2
- "Recalibrate and retry posts 1-4" — agent rolls back to the Phase 4 drafts and re-runs Phase 5 with operator-supplied guidance (e.g., "preserve the construction-business specifics more aggressively" / "kill more of the polished endings")
- "Cancel" — agent stops, generates a partial Memory Log, exits

WHY THIS GATE EXISTS: Phase 5 is calibration-sensitive. If the de-AI sub-passes are tuned right for posts 1-4, they're tuned right for the rest of the batch. If they overshot on voice or undershot on AI-tell removal in posts 1-4, they will do the same on posts 5-16. Catching this after 4 posts and not after 16 saves the operator a full re-run.

═══════════════════════════════════════════════════════════════
OPTIONAL CHECKPOINT 3 — FINAL REVIEW (only if requested at run start)
═══════════════════════════════════════════════════════════════

By default, after "Continue" at Checkpoint 2, the agent finishes everything and delivers final output without stopping again. That is the right default for routine batches.

For high-stakes batches (launch content, sensitive topic, first batch in a new theme area), the operator may request a third checkpoint by adding "Add a final review" to the run start message. With this option enabled:

After "Continue" at Checkpoint 2, the agent runs Phase 5+6+7 on posts 5-16 and Phase 8 autonomously. At Phase 8 completion, the agent STOPS and outputs:

DELIVERABLE AT OPTIONAL CHECKPOINT 3:
1. All 16 finalized posts in calendar order
2. The posting calendar table
3. A consolidated FLAGS section covering anything flagged on posts 5-16 that the operator hasn't seen yet
4. The agent's final assessment

The operator chooses:
- "Continue" or "Approved. Lock." — agent runs Phase 9 (Memory Log) and delivers final output
- "Stop and revise [specific posts]" — agent rewrites flagged posts at the appropriate sub-phase and re-presents
- "Cancel" — agent stops without updating the Memory Log

This checkpoint is opt-in, not default. The default Cowork Mode run is two checkpoints. The third is for runs the operator explicitly wants to eyeball end-to-end before the Memory Log records the batch.

═══════════════════════════════════════════════════════════════
WHAT THE AGENT DOES BETWEEN CHECKPOINTS
═══════════════════════════════════════════════════════════════

Pre-Checkpoint 1 (Phases 0-4):
- 0.1 Source Lock-In (acknowledge silently)
- 1.1 ICP Confirmation (auto-pass from Memory Log; HARD ERROR if Memory Log missing or ICP unlocked)
- 2.0, 2.1, 2.2, 2.3 Topics
- 3.1 Hooks
- 4.1, 4.2, 4.3 Drafts
- Output Checkpoint 1

Between Checkpoint 1 and Checkpoint 2 (Phase 5+6+7 on posts 1-4 only):
- 5.0, 5.1, 5.1b, 5.2, 5.2.5, 5.3 (run on posts 1-4)
- 6.1 Strategic Positioning Audit (run on posts 1-4)
- 7.1 Formatting Pass (run on posts 1-4)
- Build Calibration Cards
- Output Checkpoint 2

After Checkpoint 2 (default — no opt-in for Checkpoint 3):
- Run Phase 5+6+7 chain on posts 5-8, 9-12, 13-16
- 8.1 Calendar Distribution
- 9.1 Memory Log Update
- Final delivery

After Checkpoint 2 (operator opted into Checkpoint 3):
- Run Phase 5+6+7 chain on posts 5-8, 9-12, 13-16
- 8.1 Calendar Distribution
- Output Checkpoint 3
- After approval, run 9.1 Memory Log Update and final delivery

The agent does NOT output between sub-phases during autonomous runs. The operator only sees the agent's output at the checkpoints and at final delivery.

═══════════════════════════════════════════════════════════════
THE FLAGS DISCIPLINE
═══════════════════════════════════════════════════════════════

This is the most important rule for Cowork Mode. Without it, autonomous runs become invisible failure modes.

When the agent encounters a decision point that would have triggered an operator check in Standard Mode, the agent in Cowork Mode does the following:

1. Apply the most conservative interpretation of the SOP rule
2. Make the decision and continue
3. Log the decision in the next checkpoint's FLAGS section (or, at Checkpoint 2, in the Calibration Card for the affected post)

Examples of decisions that get FLAGGED but don't stop the run:

- A topic could be tagged either "tuition" or "career-development" — agent picks one, flags it
- A hook borderline-passes the Dentist Office test — agent keeps it, flags it
- A post in Phase 4 reaches 480 words because the source supported it — agent keeps it long, flags the length
- During Phase 5.1b, the agent had to delete an Earned Pivot that was load-bearing for the post structure — agent rewrites the surrounding sentences, flags the rewrite
- Phase 5.3 cadence audit softened a specific number to a range — agent flags the specificity drift on the Calibration Card
- The Memory Log shows "tuition" theme appeared in the previous batch but the source has 4 strong tuition angles — agent picks the strongest 1 and flags the 3 candidates for next batch

The operator reviews FLAGS at each checkpoint and at final delivery. Most flags are non-issues. Some flags reveal real problems the operator wants to fix. The flagging discipline is what makes autonomous runs trustworthy.

If the agent finds itself flagging more than 5 items per checkpoint (or more than 2 calibration concerns per post at Checkpoint 2), that is a signal that Cowork Mode is not the right tool for this batch. The agent should output: "I'm flagging more decisions than usual on this batch. Recommend dropping back to Standard or Express Mode in claude.ai for the rest of this run." Then wait for operator direction.

═══════════════════════════════════════════════════════════════
HOW THE OPERATOR LAUNCHES COWORK MODE
═══════════════════════════════════════════════════════════════

The operator creates a Cowork agent (in the Cowork interface) and configures it with:
- The same system_prompt.txt that powers the claude.ai Project
- The same SOP files in the agent's knowledge base, including this Cowork_Mode_SOP.md
- The operator's Client_Memory_Log.md file uploaded to the agent

To run a batch in Cowork, the operator invokes the agent with a message like:

"Run in Cowork Mode. Source material is the transcript below. Use my locked ICP from the Memory Log. Theme guidance: [optional]."

[Pasted source transcript follows]

To enable the optional final review:

"Run in Cowork Mode. Add a final review. Source material is the transcript below..."

The agent then:
1. Acknowledges receipt and confirms the locked ICP it will use
2. Runs Phases 0-4 autonomously
3. Outputs Checkpoint 1
4. Waits for operator response
5. Runs Phase 5+6+7 on posts 1-4 autonomously
6. Outputs Checkpoint 2
7. Waits for operator response
8. Runs Phase 5+6+7 on posts 5-16, Phase 8, and (if no Checkpoint 3) Phase 9 autonomously
9. Delivers final output (or stops at Checkpoint 3 first if requested)

═══════════════════════════════════════════════════════════════
WHAT IF THE OPERATOR DOES NOT RESPOND TO A CHECKPOINT
═══════════════════════════════════════════════════════════════

Cowork agents have a timeout window. If the operator does not respond within that window:

- The agent does NOT proceed past the checkpoint without explicit approval
- The agent's last output remains the latest state
- When the operator returns, they read the checkpoint output and respond normally
- The agent resumes from where it stopped

The agent must NEVER assume "Continue" if the operator is silent. Silence is a hard stop in Cowork Mode. This is the entire point of the mode — the operator can step away and come back.

═══════════════════════════════════════════════════════════════
ERROR RECOVERY IN COWORK MODE
═══════════════════════════════════════════════════════════════

If the agent encounters a real error during an autonomous run (not a flag — a hard problem):

Examples of hard errors:
- The Memory Log is missing or the ICP is not locked
- The source transcript is too short to support 12 topics
- The locked ICP is incompatible with the source material
- The agent's own self-verification (per Rule 2) catches a violation it cannot fix
- A sub-pass produces output that fails its own internal validation

When this happens, the agent stops the autonomous run, outputs an ERROR section explaining what went wrong and at which sub-phase, and asks the operator how to proceed. The agent does NOT attempt to silently work around hard errors.

The operator's options when an error is reported:
- Provide additional information (e.g., upload a missing Memory Log)
- Direct the agent to proceed with reduced scope (e.g., "make 8 topics instead of 16")
- Cancel the run and switch to Standard Mode in claude.ai

═══════════════════════════════════════════════════════════════
DELIVERABLE FORMAT AT FINAL OUTPUT
═══════════════════════════════════════════════════════════════

Final delivery contains, in this order:

1. SUMMARY: One paragraph confirming what was delivered (16 posts, calendar, Memory Log update)
2. THE 16 POSTS: Numbered, with titles, in calendar order
3. THE CALENDAR: Table format showing the posting cadence across the relevant week range
4. CONSOLIDATED FLAGS: Anything flagged during autonomous runs that the operator hasn't seen yet
5. MEMORY LOG ARTIFACT: Generated as a downloadable Claude artifact

The operator downloads the Memory Log artifact and replaces the old one in their Cowork agent's knowledge base.

═══════════════════════════════════════════════════════════════
COWORK MODE VS EXPRESS MODE — WHEN TO USE WHICH
═══════════════════════════════════════════════════════════════

| Scenario | Recommendation |
|----------|----------------|
| First time using the engine | Standard Mode (claude.ai) |
| Done 1-2 batches, want to move faster | Express Mode (claude.ai) |
| Done 3+ batches, can sit at the screen for an hour | Express Mode |
| Done 3+ batches, want to step away during the run | Cowork Mode |
| High-stakes launch content, async | Cowork Mode + "Add a final review" |
| Brand new persona, no Memory Log | Standard Mode (claude.ai) |
| First batch in a new theme area | Standard or Express; not Cowork |

The operator only needs to be present at two checkpoints per batch (three with the optional final review), all of which can be answered asynchronously from a phone.

═══════════════════════════════════════════════════════════════
WHAT COWORK MODE DOES NOT DO
═══════════════════════════════════════════════════════════════

- Cowork Mode does not skip any sub-phases. Every sub-phase still runs.
- Cowork Mode does not lower output quality. The same anti-AI rules, structural rules, and content rules apply.
- Cowork Mode does not replace the operator's judgment. The two (or three) checkpoints are real decision points where the operator catches problems.
- Cowork Mode does not work with thin source material. The agent will report an ERROR if the transcript can't support 12 topics.
- Cowork Mode does not auto-update the Memory Log on the operator's machine. The operator must download the artifact and re-upload it for the next batch.

END OF COWORK MODE SOP
