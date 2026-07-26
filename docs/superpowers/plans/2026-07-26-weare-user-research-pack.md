# Weare User Research Pack v1.0 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build an English-only, founder-operated, field-ready Toronto/GTA research pack that can test the meals-first problem thesis and block an unsupported MVP PRD.

**Architecture:** Create a modular Markdown pack in `research/user-research-pack-v1.0/`, with one operational responsibility per file and two CSV templates for participant and evidence tracking. The README defines the study sequence; all modules share the same research IDs, evidence categories, four-level evidence rubric, and proceed/narrow/reframe/stop decision model.

**Tech Stack:** Markdown, CSV, POSIX shell validation commands, Git

## Global Constraints

- Treat the Weare Founder’s Handbook v1.0 as the strategic source of truth while keeping its unvalidated product claims labelled as hypotheses.
- Limit the research market to Toronto and the Greater Toronto Area.
- Write all materials in plain English for founder-led research.
- Use Markdown for narrative and facilitator materials and CSV only for operational tracking.
- Target 15 older-adult interviews, 15 adult-child interviews, five paired follow-up interviews, and at least five seven-day diaries.
- Interview both members of a dyad separately before conducting their paired session.
- Recruit at least half of older-adult participants independently of a participating adult child.
- Do not describe Weare features during core problem discovery.
- Do not imply that cooking more is inherently healthier, safer, or evidence of longer independence.
- Keep participation, recording, diary, quotation, and future-contact choices granular.
- Do not collect diagnoses, detailed health histories, precise location, continuous monitoring data, or photographic proof.
- Do not add product features, production architecture, or clickable-prototype flows.
- Require a supported segment, trigger, parent-owned job, current behaviour, and unmet need before an MVP PRD can proceed.
- Mark research consent language as requiring appropriate legal review before operational use.

---

### Task 1: Pack Foundation and Operating Guide

**Files:**
- Create: `research/user-research-pack-v1.0/README.md`
- Create: `research/user-research-pack-v1.0/participant-tracker.csv`

**Interfaces:**
- Consumes: `docs/superpowers/specs/2026-07-26-weare-user-research-pack-design.md`
- Produces: The canonical study sequence, research-ID convention, consent-state labels, sample targets, file map, and PRD gate used by every later task.

- [ ] **Step 1: Create the pack directory and README**

Write `README.md` with these sections:

1. title, version, date, status, operator, market, and language;
2. purpose and the five required research outputs;
3. scope and explicit exclusions;
4. sample and session targets;
5. research principles;
6. fieldwork sequence from recruitment through decision;
7. session-order rule for dyads;
8. research-ID convention `WA-###`;
9. consent-state labels `yes`, `no`, `withdrawn`, and `not_asked`;
10. file-by-file operating map;
11. daily founder checklist;
12. privacy and incident-handling boundaries;
13. the hard MVP PRD gate.

State that a research ID is analytical, not anonymous, while a separately held contact list may still identify a participant.

- [ ] **Step 2: Create the participant tracker**

Create `participant-tracker.csv` with exactly this header:

```csv
research_id,participant_type,dyad_id,recruitment_source,recruited_independently,age_band,living_arrangement,cooking_frequency_band,wants_to_cook_more,smartphone_confidence,family_distance_band,family_contact_frequency,help_history,current_food_alternatives,individual_interview_status,diary_status,paired_interview_status,participation_consent,recording_consent,diary_consent,quotation_preference,future_contact_consent,scheduled_date,completed_date,contact_record_location,withdrawal_status
```

Add one non-person example row using research ID `WA-000`, mark it clearly as `EXAMPLE_DELETE_BEFORE_USE`, and avoid names, emails, phone numbers, diagnoses, or addresses.

- [ ] **Step 3: Validate the foundation**

Run:

```bash
test -f research/user-research-pack-v1.0/README.md
test -f research/user-research-pack-v1.0/participant-tracker.csv
head -n 1 research/user-research-pack-v1.0/participant-tracker.csv
rg -n '15 older-adult|15 adult-child|five paired|five seven-day|MVP PRD|WA-###' research/user-research-pack-v1.0/README.md
```

Expected: both files exist; the CSV header matches Step 2; all required study targets and the gate appear in the README.

- [ ] **Step 4: Commit the foundation**

```bash
git add research/user-research-pack-v1.0/README.md research/user-research-pack-v1.0/participant-tracker.csv
git commit -m "docs: add research pack operating foundation"
```

---

### Task 2: Assumption and Evidence System

**Files:**
- Create: `research/user-research-pack-v1.0/01-assumption-evidence-map.md`
- Create: `research/user-research-pack-v1.0/evidence-matrix.csv`

**Interfaces:**
- Consumes: Research sequence and IDs from `README.md`.
- Produces: The critical assumption IDs and atomic evidence format used by interview debriefs, synthesis, and the final decision gate.

- [ ] **Step 1: Write the assumption map**

Define and prioritise at least these assumption IDs:

- `P1`: The older adult experiences a meal-related outcome they want to change.
- `P2`: The problem is recurring and important enough to prompt action.
- `P3`: The main causes are addressable without clinical care or surveillance.
- `U1`: A specific Toronto/GTA segment experiences the problem more strongly than adjacent groups.
- `B1`: Current alternatives leave a meaningful gap.
- `R1`: Family involvement can help without creating pressure or control.
- `R2`: Parent and adult-child accounts of the problem are sufficiently aligned for a shared intervention.
- `T1`: Older adults can understand and control proposed information-sharing boundaries.
- `C1`: Adult children derive potential value without requiring monitoring access.
- `C2`: There is credible prior spending, sacrifice, or continuation intent that warrants later payment testing.
- `W1`: Meals are a credible first wedge into a repeated routine rather than merely a recipe-content need.

For every assumption include:

- current handbook belief;
- risk if false;
- direct evidence required;
- evidence that would weaken or disprove it;
- participant source;
- research method;
- current status set initially to `unsupported`.

Identify `P1`, `P2`, `P3`, `U1`, and `B1` as hard prerequisites for a meals-first concierge MVP PRD.

- [ ] **Step 2: Create the atomic evidence matrix**

Create `evidence-matrix.csv` with exactly this header:

```csv
evidence_id,research_id,dyad_id,session_type,session_date,assumption_id,evidence_type,recency,verbatim_or_observation,researcher_interpretation,alternative_explanation,contradictory_evidence,source_strength,parent_owned,segment_tags,confidence,source_note_location
```

Define allowed values in the assumption-map instructions:

- `session_type`: `older_adult_individual`, `adult_child_individual`, `paired`, `diary`;
- `evidence_type`: `observed_behaviour`, `reported_behaviour`, `attitude`, `third_party_inference`, `researcher_interpretation`;
- `source_strength`: `low`, `medium`, `high`;
- `parent_owned`: `yes`, `no`, `unclear`;
- `confidence`: `low`, `medium`, `high`.

Add one clearly marked example row using `EV-0000` and `WA-000`.

- [ ] **Step 3: Validate the evidence system**

Run:

```bash
rg -n '^### (P1|P2|P3|U1|B1|R1|R2|T1|C1|C2|W1)' research/user-research-pack-v1.0/01-assumption-evidence-map.md
head -n 1 research/user-research-pack-v1.0/evidence-matrix.csv
rg -n 'unsupported|weaken|disprove|hard prerequisite' research/user-research-pack-v1.0/01-assumption-evidence-map.md
```

Expected: all eleven assumption IDs exist, the CSV header matches Step 2, and each assumption can be disproved.

- [ ] **Step 4: Commit the evidence system**

```bash
git add research/user-research-pack-v1.0/01-assumption-evidence-map.md research/user-research-pack-v1.0/evidence-matrix.csv
git commit -m "docs: define research assumptions and evidence model"
```

---

### Task 3: Recruitment, Segmentation, Screening, and Outreach

**Files:**
- Create: `research/user-research-pack-v1.0/02-recruitment-and-segmentation.md`
- Create: `research/user-research-pack-v1.0/03-screeners-and-outreach.md`

**Interfaces:**
- Consumes: Sample targets, assumption IDs, and participant fields from Tasks 1–2.
- Produces: A purposeful contrast sample and scripts that can recruit without pitching Weare or presupposing a meal problem.

- [ ] **Step 1: Write recruitment and segmentation guidance**

Include:

- older-adult and adult-child inclusion criteria;
- first-study exclusions tied to continuous supervision, advanced cognitive impairment, medically prescribed nutrition, emergency response, inability to consent, and inability to participate in English;
- soft quotas for living arrangement, cooking frequency, desire to cook more, age band, smartphone confidence, family distance, involvement intensity, cultural meal context, current alternatives, and previous acceptance or rejection of help;
- a minimum of eight independently recruited older adults;
- five dyads eligible for separate individual sessions followed by a paired session;
- deliberate inclusion of satisfied non-cooks, people using successful alternatives, and people who reject family assistance;
- recruitment channels in Toronto/GTA;
- a live sampling-gap review after approximately ten and twenty individual interviews;
- anti-bias instructions prohibiting recruitment only through founder networks or enthusiastic adult children.

Do not claim demographic representativeness at this sample size.

- [ ] **Step 2: Write separate screeners**

Create:

- older-adult screener;
- adult-child screener;
- dyad follow-up eligibility check;
- diary suitability check.

Each screener must record only eligibility and segmentation information necessary for this study. Questions about cooking frequency and desire to change must permit neutral responses such as “I am satisfied with how I eat now.”

Include a researcher-only selection rubric that prioritises contrast coverage rather than high expressed interest.

- [ ] **Step 3: Write outreach and scheduling copy**

Include:

- general community outreach;
- direct older-adult invitation;
- adult-child invitation;
- community-organisation referral request;
- invitation to a separate paired follow-up;
- diary invitation;
- confirmation and reminder messages;
- respectful decline and wait-list messages.

Describe the study as research about everyday meal decisions and family support. Do not advertise an app, AI, health improvement, monitoring, or a promise to help someone remain independent longer.

- [ ] **Step 4: Validate recruitment neutrality**

Run:

```bash
rg -n 'eight|independently|satisfied|successful alternatives|reject|five dyads' research/user-research-pack-v1.0/02-recruitment-and-segmentation.md
rg -n 'Older-adult screener|Adult-child screener|Diary suitability|Selection rubric' research/user-research-pack-v1.0/03-screeners-and-outreach.md
rg -ni 'monitoring|diagnos|health improvement|remain independent longer|AI-powered' research/user-research-pack-v1.0/03-screeners-and-outreach.md
```

Expected: purposeful disconfirming cases and independent recruitment are explicit; all four screening components exist; any matches to prohibited positioning appear only in facilitator warnings, not participant-facing recruitment copy.

- [ ] **Step 5: Commit recruitment materials**

```bash
git add research/user-research-pack-v1.0/02-recruitment-and-segmentation.md research/user-research-pack-v1.0/03-screeners-and-outreach.md
git commit -m "docs: add neutral research recruitment materials"
```

---

### Task 4: Consent and Privacy Materials

**Files:**
- Create: `research/user-research-pack-v1.0/04-consent-and-privacy.md`

**Interfaces:**
- Consumes: Consent-state labels and data-separation rules from `README.md`.
- Produces: Plain-language participant information, consent scripts, withdrawal handling, and field safeguards referenced by every study method.

- [ ] **Step 1: Write the participant information sheet**

Explain:

- who is conducting the research;
- the purpose of studying meal decisions and family support;
- what participation involves;
- voluntary participation and the right to skip questions;
- foreseeable discomfort, especially during family discussions;
- absence of clinical, emergency, or monitoring services;
- what information is collected;
- how research IDs and separately stored contact records are used;
- retention and deletion handling;
- who may access the research;
- withdrawal limitations after de-identification or aggregate reporting;
- how questions or withdrawal requests can be raised.

Use editable operational fields only for organisation-controlled contact details and retention periods, and label those fields `OPERATIONAL FIELD — COMPLETE BEFORE RECRUITMENT`, not with generic drafting markers.

- [ ] **Step 2: Write granular consent scripts**

Provide separate yes/no choices for:

- study participation;
- audio recording;
- video recording if ever proposed;
- diary participation;
- use of anonymised quotations;
- future research contact.

State that declining recording or future contact does not prevent core interview participation.

- [ ] **Step 3: Add dyad, withdrawal, and incident safeguards**

Include:

- a paired-session reminder that private individual-interview content will not be disclosed;
- permission for either participant to pause or end the paired discussion;
- a withdrawal and deletion workflow keyed by research ID;
- handling for accidental sensitive disclosures;
- a boundary stating that urgent safety concerns require pausing research and using a separately approved escalation policy;
- a legal-review notice before field use.

Do not invent hotline, clinical, legal, or emergency instructions.

- [ ] **Step 4: Validate consent granularity and scope**

Run:

```bash
rg -n 'Study participation|Audio recording|Video recording|Diary participation|Anonymised quotations|Future research contact' research/user-research-pack-v1.0/04-consent-and-privacy.md
rg -n 'legal review|skip|withdraw|research ID|separately|not.*clinical|not.*emergency|not.*monitoring' research/user-research-pack-v1.0/04-consent-and-privacy.md
rg -n '\b(T[B]D|T[O]DO|F[I]XME)\b' research/user-research-pack-v1.0/04-consent-and-privacy.md && exit 1 || true
```

Expected: all consent choices are independent, participant rights and service boundaries are explicit, and no unresolved drafting marker exists.

- [ ] **Step 5: Commit consent materials**

```bash
git add research/user-research-pack-v1.0/04-consent-and-privacy.md
git commit -m "docs: add research consent and privacy safeguards"
```

---

### Task 5: Individual and Paired Interview Guides

**Files:**
- Create: `research/user-research-pack-v1.0/05-older-adult-interview-guide.md`
- Create: `research/user-research-pack-v1.0/06-adult-child-interview-guide.md`
- Create: `research/user-research-pack-v1.0/07-paired-family-interview-guide.md`

**Interfaces:**
- Consumes: Assumption IDs, consent boundaries, and evidence-type definitions.
- Produces: Three facilitator-ready session protocols that generate comparable behavioural, relational, and disconfirming evidence.

- [ ] **Step 1: Write the older-adult interview guide**

Create a 45–60 minute guide with:

- pre-session consent and recording check;
- opening rapport questions unrelated to age or decline;
- a chronological reconstruction of meals from the last seven days;
- deep dives into two recent meal decisions, including one that went as intended and one that did not;
- cooking-for-one context, effort, portioning, repetition, grocery acquisition, and current alternatives;
- prior attempts to change the routine and resulting outcomes;
- family help that felt useful, neutral, annoying, or controlling;
- privacy and sharing boundaries discussed without proposing a specific product;
- explicit questions that test satisfaction with cooking less and absence of a problem;
- a closing importance and change-readiness check;
- facilitator probes and “do not lead” warnings;
- post-session evidence capture by assumption ID.

Do not ask participants to diagnose themselves or justify cooking more.

- [ ] **Step 2: Write the adult-child interview guide**

Create a 45–60 minute guide with:

- pre-session consent and recording check;
- reconstruction of the last specific event that caused concern;
- separation of directly observed facts from assumptions about the parent;
- current calls, visits, food support, coordination, and workarounds;
- previous attempts and what happened;
- existing spending, services, or sacrifices;
- moments when support caused tension or was rejected;
- acceptable and unacceptable information visibility;
- evidence that concern is not recurring or not important;
- what would make no product necessary;
- a closing value and continuation check without quoting a subscription price;
- facilitator warnings against treating worry as proof of the parent’s problem;
- post-session evidence capture by assumption ID.

- [ ] **Step 3: Write the paired-family interview guide**

Create a 60-minute follow-up guide with:

- confirmation that both individual interviews occurred;
- renewed consent and ground rules;
- neutral comparison of one recent meal or support event;
- turn-taking that lets each person describe the same event;
- identification of agreement, mismatch, and unspoken assumptions;
- negotiation of useful help and unacceptable pressure;
- information-sharing scenarios expressed as relationship situations rather than product screens;
- a closing summary that each participant can correct;
- a private facilitator debrief after both participants leave.

Prohibit disclosure of one person’s private interview answers and prohibit the facilitator from mediating family conflict.

- [ ] **Step 4: Validate guide structure and solution neutrality**

Run:

```bash
for f in research/user-research-pack-v1.0/0{5,6,7}-*.md; do rg -n 'Consent|Recent|Current|Previous|Disconfirm|Close|Debrief' "$f"; done
rg -ni 'Would you use|Would you pay for|our app|Weare would|feature|prototype' research/user-research-pack-v1.0/0{5,6,7}-*.md
```

Expected: every guide contains consent, recent-behaviour, current-alternative, disconfirmation, closing, and debrief coverage; any solution-language matches appear only in facilitator prohibitions.

- [ ] **Step 5: Commit the interview guides**

```bash
git add research/user-research-pack-v1.0/05-older-adult-interview-guide.md research/user-research-pack-v1.0/06-adult-child-interview-guide.md research/user-research-pack-v1.0/07-paired-family-interview-guide.md
git commit -m "docs: add problem-led interview guides"
```

---

### Task 6: Seven-Day Diary and Session Debrief

**Files:**
- Create: `research/user-research-pack-v1.0/08-seven-day-behaviour-diary.md`
- Create: `research/user-research-pack-v1.0/09-session-notes-and-debrief.md`

**Interfaces:**
- Consumes: Research IDs, consent rules, assumption IDs, and evidence types.
- Produces: Contemporaneous behavioural evidence and a consistent same-day conversion from sessions to atomic evidence.

- [ ] **Step 1: Write the diary setup and daily template**

Include:

- researcher setup instructions and diary consent check;
- participant-facing purpose and privacy reminder;
- low-burden completion options for paper, print, or simple digital use;
- one setup page;
- one reusable daily page;
- end-of-week reflection;
- missed-day guidance stating that gaps are acceptable and not evidence of risk.

The daily page must capture:

- meals and how each was obtained;
- the decision that led to the meal;
- intended meals that did not happen;
- grocery or other food-acquisition actions;
- effort and “worth it” moments in the participant’s own words;
- help offered, requested, accepted, ignored, or refused;
- relevant calls, visits, or messages;
- optional context chosen by the participant.

Do not require calories, “healthy” ratings, location history, or photographs.

- [ ] **Step 2: Write the session notes and debrief template**

Include:

- session metadata and consent confirmation;
- concise participant context;
- chronological event notes;
- exact quotations;
- observed behaviour;
- third-party inference;
- researcher interpretation;
- alternative explanations;
- contradictions and disconfirming evidence;
- assumption-by-assumption evidence;
- segment tags;
- questions for later sessions;
- researcher-bias reflection;
- atomic evidence rows ready to transfer into `evidence-matrix.csv`.

- [ ] **Step 3: Validate diary burden and evidence separation**

Run:

```bash
rg -n 'Day [1-7]|reusable daily|missed|acceptable|not.*risk|End-of-week' research/user-research-pack-v1.0/08-seven-day-behaviour-diary.md
rg -n 'Exact quotation|Observed behaviour|Third-party inference|Researcher interpretation|Alternative explanation|Disconfirming evidence|Atomic evidence' research/user-research-pack-v1.0/09-session-notes-and-debrief.md
rg -ni 'calorie|healthy rating|location history|photograph.*required' research/user-research-pack-v1.0/08-seven-day-behaviour-diary.md
```

Expected: the diary explicitly tolerates missed entries, the debrief separates evidence types, and prohibited collection appears only in “do not collect” instructions.

- [ ] **Step 4: Commit diary and debrief materials**

```bash
git add research/user-research-pack-v1.0/08-seven-day-behaviour-diary.md research/user-research-pack-v1.0/09-session-notes-and-debrief.md
git commit -m "docs: add behaviour diary and debrief templates"
```

---

### Task 7: Synthesis Framework and Decision Gate

**Files:**
- Create: `research/user-research-pack-v1.0/10-synthesis-framework.md`
- Create: `research/user-research-pack-v1.0/11-evidence-rubric-and-decision-gate.md`

**Interfaces:**
- Consumes: Atomic evidence rows, assumption IDs, segment tags, dyad IDs, and evidence categories from all earlier tasks.
- Produces: A reproducible method for turning field evidence into a proceed, narrow, reframe, or stop decision.

- [ ] **Step 1: Write the synthesis framework**

Include:

- evidence-cleaning instructions;
- an initial codebook aligned to meals, effort, alternatives, triggers, desired outcomes, family support, tension, privacy, current spending, and non-problems;
- rules for adding emergent codes without deleting contradictory evidence;
- within-participant summary;
- parent versus adult-child evidence separation;
- dyad comparison;
- segment comparison;
- current-alternative analysis;
- trigger → behaviour → consequence → workaround → remaining gap mapping;
- pattern, exception, and negative-case tracking;
- interim synthesis after approximately one-third and two-thirds of individual sessions;
- researcher-bias review;
- a final evidence-backed problem statement template.

Require every synthesis claim to link back to evidence IDs.

- [ ] **Step 2: Define the four evidence ratings**

In `11-evidence-rubric-and-decision-gate.md`, define:

- **Unsupported:** no direct evidence, only founder belief, demographic context, hypothetical reaction, or third-party inference.
- **Weak:** isolated or vague evidence, low recurrence, no recent behavioural example, or substantial alternative explanations.
- **Moderate:** repeated recent evidence across multiple independent participants, including older-adult ownership, with some contradictory cases understood.
- **Strong:** consistent recent behavioural and diary evidence in a specific segment, clear importance and recurrence, meaningful inadequacy of alternatives, and disconfirming cases that sharpen rather than overturn the claim.

State that counts support transparency but do not make this small purposive sample statistically representative.

- [ ] **Step 3: Define the decision rules**

Require these outcomes:

- **Proceed:** `P1`, `P2`, `P3`, `U1`, and `B1` are at least moderate; the segment, trigger, parent-owned job, current behaviour, and unmet need are explicit; no privacy or relationship evidence makes a shared concierge test unacceptable.
- **Narrow:** a meaningful problem is moderate or strong only in a smaller segment, trigger, or job.
- **Reframe:** a meaningful problem exists, but meals, the assumed cause, or shared-family mechanism is not supported.
- **Stop:** the problem is not recurring, not important, not parent-owned, adequately solved, structurally outside Weare’s non-clinical scope, or dependent on surveillance.

Include a final decision record with:

- decision and date;
- evidence summary;
- strongest contradictory evidence;
- segment and trigger;
- parent-owned job;
- current behaviour and alternatives;
- unmet need;
- privacy and relationship finding;
- unresolved risks;
- what the next deliverable is authorised to assume;
- explicit PRD authorisation or block.

- [ ] **Step 4: Validate evidence traceability and the stop route**

Run:

```bash
rg -n 'evidence ID|Within-participant|Dyad|Segment|Alternative|Negative case|one-third|two-thirds|problem statement' research/user-research-pack-v1.0/10-synthesis-framework.md
rg -n '^### (Unsupported|Weak|Moderate|Strong|Proceed|Narrow|Reframe|Stop)' research/user-research-pack-v1.0/11-evidence-rubric-and-decision-gate.md
rg -n 'P1|P2|P3|U1|B1|parent-owned job|current behaviour|unmet need|PRD' research/user-research-pack-v1.0/11-evidence-rubric-and-decision-gate.md
```

Expected: synthesis claims are traceable, all ratings and outcomes are defined, and the gate can explicitly block the PRD.

- [ ] **Step 5: Commit synthesis and decision materials**

```bash
git add research/user-research-pack-v1.0/10-synthesis-framework.md research/user-research-pack-v1.0/11-evidence-rubric-and-decision-gate.md
git commit -m "docs: add research synthesis and decision gate"
```

---

### Task 8: Cross-Pack Quality Assurance and Founder Handoff

**Files:**
- Modify: `research/user-research-pack-v1.0/README.md`
- Modify if needed: every file in `research/user-research-pack-v1.0/`

**Interfaces:**
- Consumes: The complete modular pack from Tasks 1–7.
- Produces: A consistent, field-ready pack with a documented validation result and no unresolved drafting markers.

- [ ] **Step 1: Verify the complete file inventory**

Run:

```bash
find research/user-research-pack-v1.0 -maxdepth 1 -type f -print | sort
```

Expected: one README, eleven numbered Markdown modules, `participant-tracker.csv`, and `evidence-matrix.csv`.

- [ ] **Step 2: Run drafting and formatting checks**

Run:

```bash
rg -n '\b(T[B]D|T[O]DO|F[I]XME)\b|impl[e]ment later|fill[ ]in' research/user-research-pack-v1.0 && exit 1 || true
git diff --check
```

Expected: no unresolved drafting markers and no whitespace errors. The phrase `OPERATIONAL FIELD — COMPLETE BEFORE RECRUITMENT` is allowed because it identifies organisation-controlled information that cannot be invented.

- [ ] **Step 3: Run cross-file consistency checks**

Run:

```bash
rg -l 'WA-###|research ID' research/user-research-pack-v1.0/*.md
rg -l 'unsupported|weak|moderate|strong' research/user-research-pack-v1.0/*.md
rg -l 'proceed|narrow|reframe|stop' research/user-research-pack-v1.0/*.md
rg -n 'MVP PRD' research/user-research-pack-v1.0/*.md
```

Expected: the README and all analytical modules use the same research-ID convention, evidence ratings, decision outcomes, and PRD gate.

- [ ] **Step 4: Run scope and language checks**

Search for risky terms:

```bash
rg -ni 'patient|elderly|compliance|decline score|monitoring alert|malnourished|diagnose|treat|guarantee safety|extends independence|improves health' research/user-research-pack-v1.0
```

Review every match. Retain a match only when it is an explicit prohibition, a participant’s possible language, or a necessary non-clinical boundary. Rewrite any researcher-authored claim that medicalises participants, promises health or independence outcomes, or normalises surveillance.

- [ ] **Step 5: Simulate the founder workflow**

Using only the pack, walk through this dry run:

1. select a hypothetical participant against the recruitment matrix;
2. assign `WA-901`;
3. record consent choices;
4. choose the correct interview guide;
5. complete one mock debrief;
6. convert one mock observation into an evidence-matrix row;
7. trace it to one assumption;
8. apply an evidence rating;
9. record a hypothetical `stop` decision.

Do not add the mock participant or mock evidence to production CSV templates. Record dry-run issues in the working notes, correct the pack, and rerun the affected checks.

- [ ] **Step 6: Add validation status to the README**

Add a “Validation status” section stating:

- file inventory complete;
- placeholder scan passed;
- terminology consistency checked;
- scope and language review passed;
- founder workflow dry run passed;
- consent language still requires appropriate legal review before operational use.

- [ ] **Step 7: Verify the final worktree**

Run:

```bash
git diff --check
git status --short
```

Expected: only intended research-pack changes are present and no formatting error is reported.

- [ ] **Step 8: Commit the verified pack**

```bash
git add research/user-research-pack-v1.0
git commit -m "docs: complete Weare user research pack v1.0"
```
