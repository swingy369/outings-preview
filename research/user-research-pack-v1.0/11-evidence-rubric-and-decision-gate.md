# Evidence Rubric and Decision Gate

**Use with:** `01-assumption-evidence-map.md`, `10-synthesis-framework.md`, `evidence-matrix.csv`, and the final evidence-backed problem statement.
**Purpose:** Rate each assumption transparently and record one final decision: proceed, narrow, reframe, or stop. This is qualitative, purposive research; counts support transparency but do not make this small purposive sample statistically representative.

## Before rating a claim

For every assumption, list supporting, contradictory, and ambiguous `evidence ID` values; unique `WA-###` research IDs; any `DY-###` context; segment tags; evidence categories; recency; parent-owned status; alternatives; and outstanding alternative explanations. Keep adult-child third-party inference separate from older-adult evidence. Do not rate a claim from a quote count, demographic context, founder belief, or a hypothetical reaction.

Use this worksheet once per assumption (`P1`, `P2`, `P3`, `U1`, `B1`, `R1`, `R2`, `T1`, `C1`, `C2`, `W1`):

| Assumption ID | Proposed claim and segment | Direct older-adult evidence IDs | Other evidence IDs / type | Contradictory evidence IDs | Alternatives considered | Parent-owned status | Rating | Reviewer/date |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  | `unsupported / weak / moderate / strong` |  |

### Unsupported

There is no direct evidence for the claim. The apparent support is only founder belief, demographic context, a hypothetical reaction, third-party inference, or a researcher interpretation. A claim also remains unsupported where required behavioural, ownership, or alternative evidence is absent.

### Weak

Evidence is isolated or vague, has low recurrence, lacks a recent behavioural example, or has substantial alternative explanations. It may be a useful lead, but it does not establish a problem, segment, cause, family mechanism, or unmet need.

### Moderate

There is repeated recent evidence across multiple independent participants, including older-adult ownership, and some contradictory cases are understood. The evidence is specific enough to describe a segment, trigger or job, current behaviour, and relevant alternatives without erasing remaining uncertainty.

### Strong

There is consistent recent behavioural and diary evidence in a specific segment, with clear importance and recurrence, meaningful inadequacy of alternatives, and disconfirming cases that sharpen rather than overturn the claim. Parent-owned older-adult evidence is explicit, and any relationship or privacy implications are compatible with the proposed scope.

## Rating safeguards

- More rows, sessions, or dyad members do not automatically improve a rating. Count unique independent participants and distinguish corroboration from repeated material about the same event.
- `observed_behaviour` and recent `reported_behaviour`, especially diary evidence, can strengthen a claim when specific and relevant. `attitude` can contextualise it. `third_party_inference` and `researcher_interpretation` cannot establish older-adult ownership by themselves.
- A paired session is not a tie-breaker. It adds voluntarily shared evidence and may reveal mismatch; it never overrides private individual evidence.
- A satisfied routine, viable alternative, no desired change, rejected family help, infrequent event, unresolved alternative explanation, or non-clinical scope boundary may lower or prevent a rating.
- Record all exceptions and strongest contradictory evidence IDs. A favourable claim without its contradicting evidence is incomplete.

## Decision rules

The final decision is based on the final evidence-backed problem statement and completed ratings worksheet. It does not establish product-market fit, clinical suitability, or permission to monitor anyone.

### Proceed

Select **proceed** only when all of the following are true:

- `P1`, `P2`, `P3`, `U1`, and `B1` are each rated at least **moderate**.
- A specific segment, recurring trigger, parent-owned job or desired outcome, current behaviour and alternatives, and unmet need are explicit and traceable to evidence IDs.
- The claim includes behavioural evidence, recurrence across multiple independent participants, older-adult ownership, alternative analysis, and explicit contradictory cases.
- No privacy or relationship evidence makes a shared concierge test unacceptable. The proposed test preserves older-adult control and does not require surveillance, continuous monitoring, compelled sharing, or clinical assessment.

Only **proceed** authorises an MVP PRD, and only for the segment, trigger, parent-owned job, current behaviour/alternatives, unmet need, and privacy boundary documented in the final decision record.

### Narrow

Select **narrow** when a meaningful problem is moderate or strong only in a smaller, evidence-defined segment, trigger, or job. Record what is supported, adjacent segments/triggers/jobs that are not, and additional evidence needed before any broader claim. A **Narrow** decision always blocks the MVP PRD. If the narrowed scope later independently satisfies every Proceed condition, formally reassess the decision record and change the final decision to **Proceed** before authorising a PRD.

### Reframe

Select **reframe** when a meaningful problem exists, but meals, the assumed cause, or the shared-family mechanism is not supported. State the evidence IDs that establish the problem and those that disconfirm the meals-first framing, cause, or mechanism. Reframe does not authorise a meals-first shared-concierge PRD; it authorises only further problem discovery within the documented boundaries.

### Stop

Select **stop** when the problem is not recurring, not important, not parent-owned, adequately solved, structurally outside Weare’s non-clinical scope, or dependent on surveillance. Stop also applies when a shared concierge test would require unacceptable pressure, relationship intrusion, monitoring, clinical judgement, or access the older adult does not control. Preserve the evidence and negative cases; do not reinterpret them as a feature opportunity. **Stop explicitly blocks the PRD.**

## PRD authorisation gate

Complete every field below before commissioning, drafting, or authorising a PRD.

| Required output | Explicit evidence required | Gate result |
| --- | --- | --- |
| Specific segment | Evidence-defined segment and adjacent contrast; evidence IDs | `present / not established` |
| Recurring trigger | Recent repeated triggering situation; evidence IDs | `present / not established` |
| Parent-owned job | Older adult’s own desired outcome; evidence IDs; not adult-child inference alone | `present / not established` |
| Current behaviour and alternatives | What happens now, alternatives used/considered, and their trade-offs; evidence IDs | `present / not established` |
| Unmet need | Important remaining parent-owned gap after alternatives; evidence IDs | `present / not established` |
| Prerequisite ratings | `P1`, `P2`, `P3`, `U1`, and `B1` at least moderate | `met / not met` |
| Privacy and relationship boundary | Shared test acceptable without surveillance or unwanted sharing; evidence IDs | `acceptable / unacceptable / not established` |
| Final decision | `proceed / narrow / reframe / stop` |  |

**Block rule:** The PRD is blocked unless each of the first five required outputs is `present`, the prerequisite ratings are `met`, the privacy and relationship boundary is `acceptable`, and the final decision is **proceed**. If the segment, trigger, parent-owned job, current behaviour, or unmet need is missing or `not established`, record **“PRD authorisation: BLOCKED”** even if other evidence is promising.

## Final decision record

Complete and retain this record with final synthesis. Use de-identified research IDs and evidence IDs only.

| Field | Final record |
| --- | --- |
| Decision and date | `proceed / narrow / reframe / stop — YYYY-MM-DD` |
| Evidence summary | Claim, ratings, unique participant/dyad context, and supporting evidence IDs |
| Strongest contradictory evidence | Direct contradictory/negative-case evidence IDs and what they change |
| Segment and trigger | Evidence-defined segment tags and recurring trigger; evidence IDs |
| Parent-owned job | Older-adult desired outcome; evidence IDs |
| Current behaviour and alternatives | Behaviour, alternatives used/considered, what works, trade-offs; evidence IDs |
| Unmet need | Remaining important parent-owned gap, or `not established`; evidence IDs |
| Privacy and relationship finding | Chosen boundaries, alignment/mismatch, and shared-test acceptability; evidence IDs |
| Unresolved risks | Evidence gaps, alternative explanations, scope boundary, or relationship risk |
| What the next deliverable is authorised to assume | Only the exact rated, evidence-defined scope; or `no product assumption authorised` |
| PRD authorisation or block | `PRD authorisation: APPROVED` only for Proceed with every gate field met; otherwise `PRD authorisation: BLOCKED` and reason |

### Decision-record sign-off questions

Before marking the record final, answer each question with evidence IDs or “not established”:

1. Is the problem directly parent-owned, recurring, and important—not simply a family concern or hypothetical preference?
2. Are the segment, trigger, parent-owned job, current behaviour, alternatives, and unmet need explicit?
3. Are `P1`, `P2`, `P3`, `U1`, and `B1` at least moderate?
4. What is the strongest contradictory evidence, and does it narrow, reframe, or stop the claim?
5. Does the proposed shared concierge test avoid surveillance, monitoring, clinical judgement, and unwanted information sharing?
6. Does the final decision explicitly state whether the PRD is authorised or blocked?

If any answer is “not established,” a Proceed decision is unavailable and the PRD remains blocked.
