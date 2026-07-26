# Synthesis Framework

**Use with:** `01-assumption-evidence-map.md`, `02-recruitment-and-segmentation.md`, `07-paired-family-interview-guide.md`, `08-seven-day-behaviour-diary.md`, `09-session-notes-and-debrief.md`, and `evidence-matrix.csv`
**Purpose:** Turn de-identified atomic evidence into a transparent, revisable account of patterns, exceptions, and evidence gaps. This framework does not itself validate an assumption or authorise a PRD.

## Non-negotiable traceability rules

- Every synthesis claim, comparison, rating input, and problem-statement phrase must cite the relevant `evidence ID` values (for example, `EV-0142; EV-0171`). A claim without an evidence ID is a question or interpretation, not a finding.
- Preserve the original `research_id`, `dyad_id`, `assumption_id`, `evidence_type`, `parent_owned`, and post-consent re-confirmed `segment_tags` when working from `evidence-matrix.csv`. Do not replace the matrix with an aggregated note.
- Keep the direct material in `verbatim_or_observation` separate from `researcher_interpretation`. Do not upgrade an `attitude`, `third_party_inference`, or `researcher_interpretation` into reported or observed behaviour.
- Use the allowed evidence categories exactly: `observed_behaviour`, `reported_behaviour`, `attitude`, `third_party_inference`, and `researcher_interpretation`. Recent first-person older-adult behaviour carries particular weight for parent-owned problem claims.
- A paired account supplements, but never overwrites, either private individual account. Adult-child evidence about an older adult remains third-party inference unless the adult child describes their own action.
- Never infer a problem from low cooking, a missed diary entry, silence, age, living arrangement, or an adult child's concern. Keep satisfactory routines and viable alternatives in the synthesis.

## 1. Prepare and clean the evidence

1. Work only from de-identified records. Exclude withdrawn material and do not add names, contact details, precise addresses, diagnoses, or detailed health history to working files.
2. Check each atomic row has a unique `evidence ID`, valid `WA-###` research ID, applicable `DY-###` or `not applicable`, valid assumption ID, allowed evidence type, parent-owned status, recency, post-consent re-confirmed segment tags, and source-note reference. Flag missing or ambiguous fields; do not silently complete them from memory or screening records.
3. Check atomicity. Split a row only when source notes support distinct observations/actions; retain the original source location and link resulting rows. Do not merge different participants, events, assumptions, or contradictory accounts.
4. De-duplicate only exact accidental imports. Retain repeated accounts as separate evidence and record their independent `research_id` values. Do not count multiple rows from one event as independent recurrence.
5. Re-read `alternative_explanation` and `contradictory_evidence` for every row used in a claim. Create a follow-up question or an explicit limitation when they leave material ambiguity.
6. Mark each row's analytical role: direct older-adult evidence, adult-child own behaviour, third-party inference, paired shared account, diary account, or researcher interpretation. This is a sorting aid, not a new evidence type.
7. Maintain a cleaning log: date, evidence ID, change, reason, and whether it affects a previous synthesis claim. Never edit away an inconvenient quotation, alternative, or contradiction.

## 2. Initial codebook

Apply one or more descriptive codes to each relevant atomic row. Codes organise evidence; they are not proof. Record the exact `evidence ID` beside every coded entry.

| Code family | Initial codes | Apply when the row shows | Important distinction or counter-code |
| --- | --- | --- | --- |
| Meals and routines | `meal_routine`, `meal_decision`, `cooking_for_one`, `food_acquisition`, `leftovers`, `prepared_food` | How a meal is made, bought, received, planned, or not made | `routine_satisfactory` when no change is wanted |
| Effort and trade-offs | `effort`, `time_cost`, `money_cost`, `coordination_cost`, `worth_it`, `abandoned_intention` | Effort, sacrifice, or why an option was/was not worthwhile | Do not equate effort with a problem if accepted or valued |
| Current alternatives | `alternative_used`, `alternative_considered`, `alternative_works`, `alternative_tradeoff`, `alternative_rejected` | Delivery, groceries, restaurants, family help, community meals, batch cooking, or another response | Name the alternative; do not write only “no alternative” |
| Triggers and sequences | `trigger`, `behaviour`, `consequence`, `workaround`, `remaining_gap` | A before-to-after event sequence or repeatable situation | `no_trigger_or_one_off` for isolated or unclear events |
| Desired outcomes and ownership | `desired_outcome`, `parent_owned_job`, `no_change_wanted`, `adult_child_goal` | What the older adult wants changed, or what only the adult child wants | `parent_owned_job` requires older-adult expression or demonstration |
| Family support and relationship | `support_offered`, `support_requested`, `support_accepted`, `support_declined`, `support_unneeded`, `role_boundary`, `tension`, `alignment`, `mismatch` | Help, expectations, conflict, or alignment | Preserve each person's account; do not use a dyad to settle disagreement |
| Privacy and autonomy | `privacy_boundary`, `choice_control`, `shared_information`, `monitoring_concern`, `surveillance_required` | Information/involvement chosen, refused, or required | `surveillance_required` is a potential scope/stop signal |
| Current spending and commitment | `current_spending`, `time_investment`, `prior_attempt`, `sacrifice`, `continuation_condition` | Recent money, time, effort, prior attempt, or trade-off | Hypothetical willingness alone is not spending evidence |
| Non-problems and scope | `satisfied`, `problem_rare`, `problem_unimportant`, `adequately_solved`, `clinical_or_structural_boundary` | Evidence against recurrence, importance, ownership, unmet need, or non-clinical scope | Keep these rows in all claim reviews |
| Evidence quality | `recent_behaviour`, `diary_corroboration`, `third_party_only`, `alternative_explanation`, `contradiction`, `uncertain` | Directness, recency, corroboration, or limits of an account | Qualifies a claim; does not replace the evidence category |

### Emergent-code rule

Add an emergent code when a recurring idea, mechanism, alternative, boundary, or negative case is not captured well by the initial codebook. Define it in a code log with: code name, plain-language definition, inclusion rule, exclusion rule, first `evidence ID`, date added, and analyst. Apply it prospectively and recode earlier relevant rows. Never delete, rename away, or fold contradictory evidence into a favourable code; retain both initial and emergent codes where both apply. If a code proves unhelpful, mark it retired in the log and preserve its historical use.

## 3. Build the comparison records

### Within-participant summary

Create one record per `WA-###` before comparing participants. This protects chronology and prevents a memorable quote from standing in for a person's full account.

| Field | Record with evidence IDs |
| --- | --- |
| Participant and context | `WA-###`; role; relevant post-consent re-confirmed segment tags from the matrix; session/diary sources; limitations |
| Recent meal events | Event, recency, trigger, behaviour, consequence, and `evidence ID` |
| Parent-owned desired outcome or no-change account | Older-adult wording/behaviour; ownership status; `evidence ID` |
| Current behaviour and alternatives | What happens now; alternatives used/considered; trade-offs; `evidence ID` |
| Workarounds and remaining gap | What was attempted, what it solved, what remained; `evidence ID` |
| Family support and privacy | Invited/declined help, boundaries, tension or alignment; `evidence ID` |
| Contradictions and alternative explanations | Direct conflict, uncertainty, satisfactory routine, or plausible other explanation; `evidence ID` |
| Assumption contribution | `P1` through `W1`: supports, weakens, or cannot assess, with `evidence ID` |

Keep older-adult and adult-child summaries separate. An adult-child summary may establish the adult child's current actions, effort, spending, or concern; it cannot establish the older adult's job, recurrence, or unmet need without direct older-adult evidence.

### Dyad comparison

For each `DY-###`, compare the two individual summaries first, then add only publicly shared paired evidence. Keep all three sources visibly separate.

| Topic | Older-adult individual evidence IDs | Adult-child individual evidence IDs | Paired evidence IDs | Alignment, mismatch, or unresolved difference |
| --- | --- | --- | --- | --- |
| Trigger and current routine |  |  |  |  |
| Parent-owned job / desired outcome |  |  |  |  |
| Current behaviour and alternatives |  |  |  |  |
| Helpful versus unwanted support |  |  |  |  |
| Privacy and information boundary |  |  |  |  |
| Consequence and remaining gap |  |  |  |  |

Do not infer agreement from silence or make private evidence visible in the paired record. A material mismatch on ownership, help, privacy, or whether a problem exists is a finding that can weaken `R1`, `R2`, `T1`, or `C1` and may block a shared concierge test.

### Segment comparison

Use only post-consent re-confirmed segment tags recorded in the debrief and `evidence-matrix.csv` (for example, living arrangement, cooking frequency, desired cooking change, smartphone confidence, family distance/contact, help history, cultural meal context, and current alternatives). Screening, tracker, and sampling-gap worksheet values remain operational and are not analytical evidence; never copy or complete matrix tags from those records. Define a segment only if observable in the matrix and distinguishable from an adjacent contrast; do not create an identity-based segment from assumptions.

| Segment tag / contrast | Participants and evidence IDs | Recurring trigger and consequence | Parent-owned job | Current alternatives and gap | Important exceptions / negative cases | Evidence gap |
| --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  |

Compare independent older-adult evidence first. Counts can show how many independent participants or dyads contributed, but do not turn this purposeful sample into a prevalence estimate.

### Current-alternative analysis

For every proposed problem, list the current alternative before naming a gap. Compare the same alternative across people rather than treating all delivery, family help, or cooking as equivalent.

| Alternative | Who uses or considers it (evidence IDs) | Trigger / job it addresses | What works well | Costs or trade-offs | Why rejected or insufficient, if at all | Parent-owned remaining gap |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  |

An alternative that works well enough is disconfirming evidence for `B1`. Do not claim an unmet need merely because an alternative has any inconvenience.

## 4. Map behaviours, patterns, and exceptions

### Trigger → behaviour → consequence → workaround → remaining gap

Map each sufficiently described recent event before generalising. Use one row per event or repeatable event type and attach all source `evidence ID` values.

| Segment / participant | Trigger | Current behaviour | Consequence | Workaround or alternative | Remaining gap or satisfactory resolution | Parent-owned? | Evidence IDs |
| --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  |  |

Only a repeated pattern across independent participants can support recurrence. If the chain is incomplete, label the missing link rather than inventing a cause or consequence.

### Pattern, exception, and Negative case tracker

Maintain this tracker alongside every candidate claim. A pattern is not complete until its exceptions have been actively examined.

| Candidate claim / assumption ID | Pattern evidence IDs and independent participants | Exception or Negative case evidence IDs | Alternative explanation | What the negative case changes | Current status / next evidence needed |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |

Examples of a Negative case include a satisfied non-cook, a person whose delivery or family arrangement resolves the job, a parent who does not want help, a dyad with incompatible boundaries, an infrequent event, or a case primarily requiring clinical or structural support. Retain these cases in the final synthesis even when uncommon.

## 5. Interim and final synthesis cadence

Run interim reviews after approximately **one-third** and **two-thirds** of the 30 individual sessions (about 10 and 20 completed individual interviews). Add completed diaries and paired sessions as supplementary evidence, without allowing them to substitute for the individual-session denominator.

At each interim review:

1. Clean and code new rows; update Within-participant summaries, Dyad comparisons, Segment comparison, and alternative analysis.
2. Review each assumption (`P1`, `P2`, `P3`, `U1`, `B1`, `R1`, `R2`, `T1`, `C1`, `C2`, `W1`) against direct, contradictory, and missing evidence IDs.
3. Identify the largest evidence gap, especially missing independent older-adult accounts, untested adjacent segments, no-problem cases, current alternatives, and privacy or relationship boundaries.
4. Adjust recruitment toward purposeful contrasts or add neutral follow-up prompts. Do not change questions, selection, or coding merely to pursue a preferred conclusion.
5. Record an interim memo: date; sessions/diaries reviewed; claims considered; relevant evidence IDs; Negative cases; potential researcher bias; changed recruitment priority; and what remains unknown. Do not issue a proceed decision at an interim review.

At final synthesis, repeat the full review, complete the evidence-rubric worksheet, and create the decision record in `11-evidence-rubric-and-decision-gate.md`.

## 6. Researcher-bias review

Before any rating or decision, have the primary researcher and, where practical, a second reviewer complete this check using evidence IDs:

- Did we treat adult-child concern, demographic context, a hypothesis, or a hypothetical reaction as evidence of a parent-owned need?
- Did we privilege articulate, high-contact, digitally confident, or family-recruited participants over independent older-adult evidence?
- Did we equate cooking more, accepting help, diary completion, or information sharing with success?
- Did we ignore viable alternatives, satisfied routines, rejected help, rare events, structural constraints, or clinical/surveillance boundaries?
- Did a prominent quote, early session, or founder belief anchor the codes or segment definition?
- Did we convert correlation into an assumed cause, or interpretation into direct behaviour?
- Did the paired session create pressure, obscure a private mismatch, or make agreement appear stronger than it is?
- Have we stated the strongest contradictory evidence IDs beside each positive claim?

Record the answer, correction made, unresolved limitation, reviewer, date, and affected evidence IDs. If a bias cannot be corrected, lower confidence or leave the claim unsupported rather than explaining it away.

## 7. Final evidence-backed problem statement

Complete this only after final comparison and rating. Use exact evidence IDs in every bracket; replace unsupported fields with “not established.”

> For **[specific initial segment, with evidence IDs]**, when **[recurring trigger, with evidence IDs]** happens, independently living older adults currently **[parent-owned current behaviour and alternatives, with evidence IDs]** because **[non-clinical context/cause only where supported, with evidence IDs]**. They are trying to achieve **[parent-owned job or desired outcome, with evidence IDs]**. Existing alternatives **[work / do not work]** because **[trade-offs and remaining unmet need, with evidence IDs]**. The strongest exception or Negative case is **[exception, with evidence IDs]**. Family involvement is **[invited/helpful/limited/unacceptable]** under **[privacy and relationship boundary, with evidence IDs]**. Therefore the evidence currently supports **[claim and rating]**, subject to **[unresolved risk or evidence gap]**.

Do not write a solution, feature requirement, market-size claim, or PRD requirement in this statement. The decision gate—not this template—determines whether a PRD may be authorised.
