# Weare User Research Pack v1.0 — Design Specification

**Status:** Approved design  
**Date:** 26 July 2026  
**Source of truth:** Weare Founder’s Handbook v1.0  
**Deliverable type:** Modular, field-ready research pack  
**Primary operator:** Weare founder  
**Research market:** Toronto and the Greater Toronto Area  
**Language:** English  

## 1. Purpose

The pack will enable Weare’s founder to run disciplined, problem-led research before commissioning an MVP PRD or production application.

The research must determine whether a specific group of independently living older adults experiences a meaningful, recurring meal-related problem that they want to change, whether family involvement helps or harms, and whether the problem is suitable for a non-clinical, privacy-preserving product.

The pack will not validate the full Weare product concept. It will create the evidence needed to decide whether the meals-first thesis should proceed, narrow, reframe, or stop.

## 2. Required Research Output

Research synthesis must identify, with supporting evidence:

1. a specific initial user segment;
2. a recurring triggering situation;
3. a parent-owned job or desired outcome;
4. the user’s current behaviour and alternatives;
5. an important unmet need that existing approaches do not adequately resolve.

The MVP PRD remains blocked until all five outputs are supported by evidence that meets the decision rubric.

## 3. Research Boundaries

### In scope

- Independently living older adults in Toronto/GTA.
- Adult children or family supporters of independently living older adults.
- Meal decisions, cooking-for-one behaviour, grocery routines, family involvement, current alternatives, and previous attempts to improve the situation.
- Separate older-adult and adult-child interviews.
- Paired family interviews after individual interviews.
- Seven-day behaviour diaries.
- Qualitative synthesis, evidence grading, and a decision gate.

### Out of scope

- Product feature prioritisation.
- Production-app requirements.
- Clinical nutrition, diagnosis, treatment, medication, emergency response, or health-risk scoring.
- Prototype usability testing.
- Hong Kong discovery.
- Cantonese or Mandarin research materials.
- Validation of outings, social connection, or broader independent-living modules except where participants raise them naturally as context.
- Claims that meal behaviour extends independence or improves health.

## 4. Research Principles

1. **Problem before solution.** Do not describe proposed Weare features during the problem-discovery portion of a session.
2. **Parent evidence is indispensable.** Adult-child concern cannot establish that an older adult has an unmet problem.
3. **Behaviour over opinion.** Ask about recent events, actions, workarounds, spending, and trade-offs before asking about preferences.
4. **Disconfirmation is intentional.** Recruit sceptics, satisfied non-cooks, people who rejected family help, and people using viable alternatives.
5. **Separate perspectives first.** Interview members of a participating family separately before a paired conversation.
6. **Consent is granular.** Participation, recording, diary completion, quotations, and future contact must not be bundled unnecessarily.
7. **Minimum necessary data.** Avoid collecting diagnoses, detailed health histories, precise location, or unrelated family information.
8. **No surveillance framing.** Missing diary entries, unshared activity, or participant silence must not be interpreted as danger.
9. **Evidence and interpretation remain distinct.** Notes must distinguish what was observed or said from the researcher’s inference.
10. **No premature PMF claim.** This research can justify a concierge experiment; it cannot establish product-market fit.

## 5. Participant and Session Model

The initial study will target:

- 15 individual older-adult interviews;
- 15 individual adult-child interviews;
- five paired family interviews;
- at least five seven-day behaviour diaries.

The five paired sessions will use dyads whose members have first completed individual interviews. This yields 30 individual interviews and five follow-up paired sessions rather than substituting a paired session for either person’s private interview.

At least half of the older-adult participants should be recruited through channels other than a participating adult child. This reduces the risk that the research sample inherits the buyer’s definition of the problem.

Recruitment will use purposeful contrasts rather than attempting demographic representativeness. The matrix will track:

- living alone versus living with a spouse or other adult;
- age band;
- current cooking frequency;
- whether the older adult wants to cook more;
- smartphone confidence;
- family distance and contact frequency;
- intensity of family involvement;
- cultural meal context;
- use of meal delivery, prepared food, restaurants, batch cooking, or family-provided meals;
- whether help has previously been welcomed, ignored, or rejected.

The pack will include inclusion criteria, exclusion criteria, soft quotas, screeners, outreach text, and a participant tracker.

## 6. Modular Deliverable Structure

The implemented pack will be stored at:

`research/user-research-pack-v1.0/`

It will contain:

### `README.md`

Study objective, research sequence, founder instructions, session order, ethical safeguards, document map, and the PRD gate.

### `01-assumption-evidence-map.md`

A prioritised map of problem, user, behaviour, relationship, trust, and commercial assumptions. Each assumption will include:

- current belief;
- why it matters;
- evidence needed;
- disconfirming evidence;
- research method;
- current evidence status.

### `02-recruitment-and-segmentation.md`

Target population, inclusion and exclusion criteria, purposeful contrasts, soft quotas, independent recruitment requirement, sample composition, and anti-bias guidance.

### `03-screeners-and-outreach.md`

Separate older-adult and adult-child screeners, paired-session eligibility, channel-specific outreach copy, invitation language, follow-up language, and a non-coercive participation description.

### `04-consent-and-privacy.md`

Plain-language information sheet, verbal or written consent script, separate optional recording consent, diary consent, quotation preferences, withdrawal process, data-handling rules, retention expectations, and researcher safety notes.

The language will clearly state that this is non-clinical product research, not a safety or health assessment. It will also state that the materials require appropriate legal review before operational use.

### `05-older-adult-interview-guide.md`

A 45–60 minute guide covering recent meals, cooking decisions, grocery behaviour, current alternatives, previous attempts, family support, autonomy, privacy, and explicit disconfirmation.

The guide will begin with lived behaviour and will not introduce the Weare concept during core problem discovery.

### `06-adult-child-interview-guide.md`

A 45–60 minute guide covering observed events, sources of concern, current support behaviour, unsuccessful attempts, family tension, alternatives, spending, privacy expectations, and credible indicators of value.

The guide will repeatedly distinguish what the adult child knows from what they infer.

### `07-paired-family-interview-guide.md`

A 60-minute guide used only after separate interviews. It will explore differences in how both people describe the same routines, negotiate support, interpret concern, and define acceptable information sharing.

The facilitator will not attempt to resolve family disagreements or pressure either participant to disclose information shared privately in an individual interview.

### `08-seven-day-behaviour-diary.md`

A low-burden daily diary covering:

- meals and how they were obtained;
- meal decisions and abandoned intentions;
- grocery or food-acquisition activity;
- help offered, requested, accepted, ignored, or refused;
- relevant calls, visits, or messages;
- moments when cooking felt worthwhile or not worthwhile;
- participant-selected context.

The diary will support paper, printable, or simple digital completion. It will not ask for calorie counts, health scoring, continuous location, or photographic proof.

### `09-session-notes-and-debrief.md`

A consistent note structure with separate fields for verbatim evidence, observed behaviour, researcher interpretation, contradictions, disconfirming evidence, follow-up questions, and immediate confidence assessment.

### `10-synthesis-framework.md`

Instructions for coding and comparing evidence across participants, within dyads, and across segments. It will include:

- a codebook;
- evidence atomicity rules;
- within-participant summaries;
- dyad comparison;
- pattern and exception tracking;
- current-alternative analysis;
- causal-chain mapping;
- researcher-bias checks;
- a synthesis summary template.

### `11-evidence-rubric-and-decision-gate.md`

A transparent rubric for rating claims as unsupported, weak, moderate, or strong. It will require behavioural evidence, recurrence, multiple independent participants, parent ownership, consideration of alternatives, and explicit contradictory cases.

The final decision will be one of:

- **Proceed:** a specific meal-related problem and segment are sufficiently supported for a concierge MVP PRD.
- **Narrow:** evidence supports a smaller segment, trigger, or job than the handbook proposes.
- **Reframe:** a meaningful problem exists, but the meals-first formulation or assumed mechanism is wrong.
- **Stop:** no sufficiently important, recurring, parent-owned problem is supported.

### Tabular templates

- `participant-tracker.csv`
- `evidence-matrix.csv`

The CSV files will use research IDs rather than participant names in analytical fields. Contact details, if operationally required, must be stored separately from research notes.

## 7. Research Flow

1. Recruit against the segmentation matrix.
2. Assign a research ID and record consent choices.
3. Conduct individual interviews.
4. Complete the same-day debrief before the next session.
5. Invite a selected contrast sample into the seven-day diary.
6. Conduct paired interviews only after both people have been interviewed separately.
7. Add atomic evidence to the evidence matrix.
8. Run interim synthesis after approximately one-third and two-thirds of individual interviews.
9. Adjust recruitment to fill evidence gaps without changing questions merely to pursue a preferred conclusion.
10. Complete final synthesis and apply the evidence rubric.
11. Record a proceed, narrow, reframe, or stop decision.
12. Authorise an MVP PRD only after the required research output is present.

## 8. Evidence Rules

The pack will distinguish:

- **Reported behaviour:** a specific action the participant says occurred.
- **Observed behaviour:** something directly seen by the researcher or captured contemporaneously in a diary.
- **Attitude:** a stated preference, belief, or reaction.
- **Interpretation:** the researcher’s explanation.
- **Inference by another participant:** for example, an adult child’s belief about a parent’s meals.

Repeated stories, hypothetical enthusiasm, and demographic statistics will not be treated as behavioural validation by themselves.

Positive evidence must be considered alongside:

- people who do not experience the problem;
- people content with cooking less;
- people whose current alternative works well;
- people who reject family involvement;
- cases where the parent and adult child disagree;
- structural causes a consumer product cannot reasonably address.

## 9. Privacy and Safety Handling

- Use participant IDs in notes, diary analysis, and synthesis.
- Store contact information separately from research content.
- Obtain explicit consent before audio or video recording.
- Make recording optional without affecting participation.
- Permit participants to skip any question or withdraw.
- Do not ask one member of a dyad to reveal another person’s private interview content.
- Do not present research participation as monitoring, care, or emergency support.
- If a participant raises an immediate safety concern, the researcher must pause the research role and follow a separately approved escalation policy; the pack will not invent clinical or emergency guidance.
- Do not reuse research material for model training, marketing, or a materially different purpose without separate consent and review.

## 10. Quality Assurance

Before field use, the implemented pack must pass:

1. **Completeness check:** every required module and template exists.
2. **Solution-bias check:** core discovery questions can be asked without describing proposed features.
3. **Leading-question check:** questions do not imply that cooking more is inherently better.
4. **Perspective check:** adult-child inference is not recorded as fact about the older adult.
5. **Disconfirmation check:** each critical assumption has questions and recruitment cases capable of disproving it.
6. **Privacy check:** participation and recording consent are separate, and unnecessary sensitive data is excluded.
7. **Operational check:** the founder can recruit, schedule, conduct, debrief, diary, synthesise, and decide using only the pack.
8. **Gate check:** no route to the MVP PRD bypasses the required segment, trigger, parent-owned job, current behaviour, and unmet-need evidence.
9. **Consistency check:** terminology, research IDs, rating levels, and decision outcomes match across all files.
10. **Placeholder check:** no unresolved drafting markers remain.

## 11. Success Criteria for the Pack

The pack is complete when:

- all listed files are usable without additional research-design work;
- the founder can run the first recruitment and interview cycle immediately;
- materials consistently reflect the handbook’s privacy and dignity boundaries;
- the research can produce credible negative as well as positive findings;
- evidence from older adults and adult children can be separated and compared;
- the decision rubric can block unsupported progression to the MVP PRD;
- no section silently turns the proposed product into an established user need.

## 12. Implementation Constraints

- Use Markdown for all narrative and facilitator materials.
- Use CSV only for operational tracking and evidence matrices.
- Keep files printable and compatible with copying into Google Docs or Sheets.
- Use plain English and avoid clinical, patronising, or surveillance-oriented language.
- Do not add product features, production architecture, or prototype flows.
- Preserve the handbook as the strategic source of truth while marking its product claims as hypotheses where research evidence does not yet exist.
