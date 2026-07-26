# Assumption and Evidence Map

**Status:** Field-ready; every assumption below is initially `unsupported`.

Use this map with the canonical sequence, `WA-###` research IDs, consent-state labels, sample targets, and hard MVP PRD gate in `README.md`. This map defines what the research needs to learn; it does not establish a finding or authorise a PRD.

## How to record atomic evidence

Add one row per discrete observation, quotation, or reported behaviour to `evidence-matrix.csv`. Use the participant's analytical `WA-###` research ID; where relevant, use a separately assigned dyad ID. Do not include names, contact information, precise addresses, diagnoses, detailed health histories, or other direct identifiers. Keep verbatim evidence or observations separate from the researcher's interpretation, and record contradictory evidence rather than silently reconciling it.

Use only these values in the matrix:

| Field | Allowed values | Recording rule |
| --- | --- | --- |
| `session_type` | `older_adult_individual`, `adult_child_individual`, `paired`, `diary` | Record the session that generated the row. A paired session follows both individual sessions; do not use it to override private accounts. |
| `evidence_type` | `observed_behaviour`, `reported_behaviour`, `attitude`, `third_party_inference`, `researcher_interpretation` | Prefer observed or recent reported behaviour. Adult-child accounts about the older adult are `third_party_inference`, unless they describe the adult child’s own behaviour. |
| `source_strength` | `low`, `medium`, `high` | Assess directness, specificity, recency, and corroboration; do not use strength to erase contradictory cases. |
| `parent_owned` | `yes`, `no`, `unclear` | Mark `yes` only when the older adult expresses or demonstrates the relevant outcome as their own; adult-child concern alone is not parent-owned evidence. |
| `confidence` | `low`, `medium`, `high` | Record confidence in the row's interpretation, not confidence that the hypothesis is true. |

For `recency`, use a concrete time reference from the participant where possible (for example, `yesterday`, `past 7 days`, or `about 3 months ago`), and otherwise record `not stated`. In `alternative_explanation`, capture a plausible non-hypothesis explanation. In `contradictory_evidence`, link or describe directly conflicting evidence; use `none identified in this item` only when none is present in that specific item. The `EV-0000` row is an example format only and must not be treated as collected evidence.

## PRD prerequisites

`P1`, `P2`, `P3`, `U1`, and `B1` are **hard prerequisites** for a meals-first concierge MVP PRD. They operationalise the README's required evidence for a parent-owned desired outcome, recurrence, an addressable problem, a specific initial segment, and an unmet need beyond current alternatives. All five must be supported under the final decision rubric; no other assumption in this document can substitute for a missing prerequisite.

### P1 — Desired meal-related outcome

- **Current handbook belief:** The older adult experiences a meal-related outcome they want to change.
- **Risk if false:** A meals-first offer would be responding to family anxiety or a generic content preference rather than a parent-owned problem.
- **Direct evidence required:** Recent first-person accounts from older adults of a meal-related outcome they want changed, plus examples of how it affects meal decisions or routines.
- **Evidence that would weaken or disprove it:** Older adults consistently report satisfaction with their meal routines, do not want a change, or say the concern belongs to someone else.
- **Participant source:** Independently living older adults, including satisfied non-cooks and participants recruited without a participating adult child.
- **Research method:** Older-adult individual interviews and seven-day behaviour diaries.
- **Current status:** `unsupported`.

### P2 — Recurring, action-worthy problem

- **Current handbook belief:** The problem is recurring and important enough to prompt action.
- **Risk if false:** The team may design for isolated inconvenience that will not sustain engagement or justify a concierge service.
- **Direct evidence required:** Recent, concrete examples showing frequency, triggers, consequences, and prior or current attempts to change the situation.
- **Evidence that would weaken or disprove it:** Accounts show the issue is rare, low consequence, already resolved, or not worth changing despite acknowledgement.
- **Participant source:** Older adults first; adult children may provide corroborating context about their own actions.
- **Research method:** Older-adult individual interviews, diaries, and selected paired interviews after both individual interviews.
- **Current status:** `unsupported`.

### P3 — Non-clinically addressable causes

- **Current handbook belief:** The main causes are addressable without clinical care or surveillance.
- **Risk if false:** A meals-first concierge MVP could create inappropriate clinical, safety, or monitoring expectations outside the research and product scope.
- **Direct evidence required:** Behavioural accounts linking the difficulty mainly to non-clinical routine, planning, shopping, cooking-for-one, access, information, motivation, or coordination barriers that participants can describe without requiring diagnosis, treatment, or surveillance.
- **Evidence that would weaken or disprove it:** The problem is predominantly caused by clinical needs, medication, acute safety concerns, or conditions requiring professional care or monitoring.
- **Participant source:** Older adults, with adult children used only to surface contextual contrast; exclude clinical assessment.
- **Research method:** Individual interviews and diaries; log scope-boundary cases without collecting unnecessary health details.
- **Current status:** `unsupported`.

### U1 — Distinct Toronto/GTA initial segment

- **Current handbook belief:** A specific Toronto/GTA segment experiences the problem more strongly than adjacent groups.
- **Risk if false:** The initial segment would be arbitrary, recruitment would overfit anecdotes, and the MVP could be too broad to test.
- **Direct evidence required:** Repeated contrasts across purposeful segments showing a defined group has stronger recurrence, consequence, parent ownership, or unmet need than adjacent groups.
- **Evidence that would weaken or disprove it:** Similar experiences occur evenly across contrasts, the proposed segment has no meaningful difference, or adjacent groups have stronger evidence.
- **Participant source:** Older adults across the README contrast dimensions, including independently recruited participants; adult children provide secondary comparison context.
- **Research method:** Recruitment segmentation, individual interviews, diaries, and interim/final synthesis.
- **Current status:** `unsupported`.

### B1 — Meaningful alternative gap

- **Current handbook belief:** Current alternatives leave a meaningful gap.
- **Risk if false:** A concierge MVP would duplicate satisfactory existing food, cooking, family, or community alternatives without a compelling reason to switch.
- **Direct evidence required:** Recent behavioural evidence of alternatives tried or considered, their costs and trade-offs, and a specific unresolved parent-owned need.
- **Evidence that would weaken or disprove it:** Participants report that current alternatives work well enough, have no important trade-offs, or resolve the desired outcome without further help.
- **Participant source:** Older adults as primary source; adult children may describe their own alternatives and support actions.
- **Research method:** Individual interviews, diaries, and synthesis comparison of alternatives and exceptions.
- **Current status:** `unsupported`.

### R1 — Helpful family involvement without pressure

- **Current handbook belief:** Family involvement can help without creating pressure or control.
- **Risk if false:** The service could damage autonomy, create family conflict, or make older adults avoid participation.
- **Direct evidence required:** Examples in which family support was invited or welcomed, retained older-adult choice, and produced a helpful meal-related outcome without coercion.
- **Evidence that would weaken or disprove it:** Older adults describe help as pressure, control, guilt, conflict, or unwanted oversight; family involvement suppresses honest choice.
- **Participant source:** Older adults and adult children interviewed separately, followed by selected consenting dyads.
- **Research method:** Individual interviews, paired interviews, and contradiction coding across accounts.
- **Current status:** `unsupported`.

### R2 — Sufficient cross-dyad alignment

- **Current handbook belief:** Parent and adult-child accounts of the problem are sufficiently aligned for a shared intervention.
- **Risk if false:** A shared intervention may address different problems for each person or intensify disagreement.
- **Direct evidence required:** Within selected dyads, separately collected accounts identify compatible triggers, desired outcomes, boundaries, and helpful roles.
- **Evidence that would weaken or disprove it:** Separate accounts materially conflict on whether a problem exists, who owns it, what help is wanted, or what information may be shared.
- **Participant source:** Selected older-adult/adult-child dyads after each person completes an individual interview.
- **Research method:** Separate individual interviews first, then paired interviews only where both consent; synthesis must preserve disagreement.
- **Current status:** `unsupported`.

### T1 — Understandable, controllable information sharing

- **Current handbook belief:** Older adults can understand and control proposed information-sharing boundaries.
- **Risk if false:** Any family-connected service could undermine informed choice, autonomy, or privacy.
- **Direct evidence required:** Older adults can explain in their own words what they would and would not share, with whom, and can distinguish optional sharing from monitoring.
- **Evidence that would weaken or disprove it:** Participants cannot explain boundaries, feel they cannot refuse family access, or expect continuous monitoring despite clear prompts.
- **Participant source:** Older adults, including varied smartphone-confidence and family-contact contrasts.
- **Research method:** Individual interviews using neutral boundary scenarios; paired interviews only to compare, never pressure, preferences.
- **Current status:** `unsupported`.

### C1 — Adult-child value without monitoring access

- **Current handbook belief:** Adult children derive potential value without requiring monitoring access.
- **Risk if false:** Adult-child value could depend on surveillance, contradicting the non-monitoring and older-adult-control principles.
- **Direct evidence required:** Adult children describe useful support, reassurance, coordination, or communication outcomes that do not require ongoing access to the older adult's activity or data.
- **Evidence that would weaken or disprove it:** Adult children say value requires tracking, proof, alerts, continuous updates, or access the older adult would not control.
- **Participant source:** Adult children, contrasted with older-adult privacy and boundary accounts.
- **Research method:** Adult-child individual interviews and selected paired interviews.
- **Current status:** `unsupported`.

### C2 — Credible payment signal

- **Current handbook belief:** There is credible prior spending, sacrifice, or continuation intent that warrants later payment testing.
- **Risk if false:** The team may mistake hypothetical enthusiasm for willingness to pay or sustained use.
- **Direct evidence required:** Concrete, recent examples of money, time, effort, or trade-offs already made for the outcome, or a specific continuation condition that can later be payment-tested.
- **Evidence that would weaken or disprove it:** Participants express only abstract interest, reject any meaningful sacrifice, or describe no past effort despite claiming the problem matters.
- **Participant source:** Older adults and adult children, with ownership and payer role recorded separately.
- **Research method:** Individual interviews and diaries focused on past behaviour; do not run payment testing in this discovery phase.
- **Current status:** `unsupported`.

### W1 — Meals as a repeated-routine wedge

- **Current handbook belief:** Meals are a credible first wedge into a repeated routine rather than merely a recipe-content need.
- **Risk if false:** The product may become undifferentiated recipe content or choose a narrow problem without a repeatable routine.
- **Direct evidence required:** Accounts show meal decisions recur in identifiable situations and involve actions, coordination, or workarounds beyond seeking recipes alone.
- **Evidence that would weaken or disprove it:** Participants primarily want occasional recipes or inspiration, do not have a repeated meal routine problem, or prefer content that solves the need fully.
- **Participant source:** Older adults first; adult children may add context about support routines.
- **Research method:** Individual interviews, seven-day diaries, and alternatives analysis.
- **Current status:** `unsupported`.

## Review rule

At interim and final synthesis, assess each assumption against direct and contradictory atomic evidence, not counts of favourable quotes. Retain `unsupported` until the decision rubric supports the claim. A hard prerequisite remains unmet when the evidence is chiefly third-party inference, lacks recurrence or parent ownership, excludes viable alternatives, or omits contradictory cases.
