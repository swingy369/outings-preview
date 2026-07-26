# Screeners and Outreach

**Status:** Field-ready neutral scripts. Use with `02-recruitment-and-segmentation.md`, the canonical sample and dyad rules in `README.md`, and the existing fields in `participant-tracker.csv`.

## Researcher instructions: minimum necessary data

Use these questions only to decide eligibility, fill purposeful sampling gaps, and schedule a session. Record only the corresponding eligibility and segmentation values in the participant tracker; place names, email addresses, telephone numbers, and scheduling details in the separate contact record. Do not ask for medical labels, medication, detailed health history, income, immigration status, or a reason someone does not cook.

Read the study description before screening: “We are doing research about everyday meal decisions and family support. We are interested in a range of experiences, including people who are satisfied with their routines and people who would like something to be different. This is a research conversation, not a service.” A person may skip any screening question or stop at any time.

Use neutral response options. Do not treat interest in a future offering, technology confidence, a family member's concern, or agreement with the researcher as eligibility.

## Older-adult screener

Use for a direct older-adult invite or a person referred to the study. If the person does not want to continue, thank them and do not retain a profile.

1. **Age and location.** “Are you 65 or older, and do you live in Toronto or the Greater Toronto Area?”
   - Record eligibility only; record `age_band` as 65–74, 75–84, or 85+ and confirm GTA eligibility. Do not record a precise address.
2. **Living arrangement.** “Which best describes who you live with: by yourself; with a spouse or partner; with family; with a roommate; or another arrangement you would like to name?”
   - Record `living_arrangement`.
3. **Independence and consent.** “Are you able to choose for yourself whether to take part in a research conversation?”
   - If no or unclear, do not enrol. Do not ask for an explanation.
4. **First-study scope.** “For this first study, we can only include people who can join an English conversation without continuous supervision and whose everyday meal choices can be discussed without a clinical nutrition plan or an urgent situation. Does that describe your situation?”
   - If no or unclear, do not enrol. Do not seek medical details. Use the exclusion guidance in `02-recruitment-and-segmentation.md` if a person mentions an urgent concern.
5. **Cooking frequency.** “In a typical week, how often do you prepare or cook a meal yourself: rarely or never; once or twice; several times; most days; or another description?”
   - Record `cooking_frequency_band`.
6. **Preference for change.** “Which is closest to you right now: I would like to cook more; I would like to cook less; I would like something else about my meals to be different; I am satisfied with how I eat now; or I am not sure?”
   - Record `wants_to_cook_more`, including neutral and satisfied responses exactly as offered; do not reinterpret satisfaction as a problem.
7. **Everyday meal options.** “What do you usually do for meals? For example, you might cook, use ready-made or delivered food, eat out, get help from someone, use a community option, or mix these.”
   - Record broad categories in `current_food_alternatives`, including whether an alternative is working well if volunteered.
8. **Technology comfort.** “How comfortable are you using a smartphone for ordinary tasks: not at all comfortable; a little; somewhat; very; or I do not use one?”
   - Record `smartphone_confidence`.
9. **Family connection.** “Is there an adult child or other family supporter you are in touch with about everyday life? You do not need to name anyone.” If yes: “Are they in your household, nearby, farther away, or would you rather not say?” and “How often are you usually in contact?”
   - Record `family_distance_band` and `family_contact_frequency`; a “no family involvement” response is valid.
10. **History of help.** “Has anyone offered or provided help related to meals or food choices? If so, did that feel welcome, not taken up, unwanted, mixed, or is there no relevant experience?”
    - Record `help_history`. Do not ask who offered it unless the participant independently offers only the broad relationship needed for a dyad check.
11. **Interview availability.** “Would you be open to a 45–60 minute research conversation at a time and format we agree on?”
    - Record individual-interview eligibility and availability in the separate contact record. Explain that participation, recording, diary, quotations, and future contact are separate choices later.

## Adult-child screener

Use for adult children and other adult family supporters. Their account does not establish an older adult's needs; it supplies a separate perspective and may be a useful contrast even when they report little involvement.

1. **Age and connection.** “Are you 18 or older, and are you an adult child or other family supporter of an older adult who lives independently in Toronto or the Greater Toronto Area?”
   - Include people who live outside GTA if the older adult meets the GTA location criterion. Do not record the older adult's name or address.
2. **Independent-living and first-study scope.** “To your knowledge, does the older adult make their own choice about taking part and live without continuous supervision?”
   - If no or unclear, do not recruit them as a dyad through this study. The adult child may still be eligible for an individual interview if their own experience fits the study; do not request medical detail.
3. **Contact and distance.** “How often are you generally in contact, if at all?” and “Are you in the same household, nearby, farther away, or would you rather not say?”
   - Record `family_contact_frequency` and `family_distance_band` for the adult-child participant's relationship context.
4. **Involvement intensity.** “How involved are you in everyday meal decisions: not involved; occasionally talk about them; sometimes help practically; often help practically; or another description?”
   - Record this within `help_history` using the participant's words where possible.
5. **Current alternatives.** “As far as you know, what options are currently used for meals: cooking, ready-made or delivered meals, eating out, family help, community options, or something else? It is also fine to say you do not know.”
   - Record broad `current_food_alternatives` categories and “do not know” when applicable.
6. **History of help.** “Have you offered or provided meal-related help? If yes, was it welcomed, not taken up, unwanted, mixed, or are you not sure?”
   - Record `help_history`; do not ask the person to evaluate the older adult's health or capability.
7. **Preference and availability.** “Would you be open to a 45–60 minute research conversation about your own experiences of everyday meal decisions and family support?”
   - Record individual-interview eligibility and scheduling availability separately. Do not ask whether they want an offering or assume there is a problem.

## Dyad follow-up eligibility check

Run this check separately with each person after both `older_adult_individual` and `adult_child_individual` interviews are complete. Use a dyad ID only after both people independently agree to consider the paired follow-up.

1. Confirm the research IDs and that each person's individual interview is complete. Do not repeat or share what either person said.
2. Ask each person privately: “We may invite some family pairs to a separate 60-minute conversation about everyday meal decisions and family support. Would you be open to considering that conversation with [relationship only]?”
3. Ask each person privately: “Do you understand that you may decline, skip questions, or stop the paired conversation, and that we will not use it to make either person share private interview content?”
4. Confirm each person can participate in English and can provide their own consent for this separate session.
5. Confirm scheduling feasibility only after both say yes. Record `paired_interview_status` in the tracker; keep scheduling details separately.

Do not require agreement about meal choices, family help, or a shared problem. Include some dyads with uncertainty or disagreement when both people freely consent. Do not invite a paired session if either person declines, appears pressured, or asks that the relationship not be contacted.

## Diary suitability check

Use this after an individual interview. The diary is a seven-day record of ordinary meal decisions; it is not a test of good behaviour. It should include days when a participant is satisfied with their routine or does not make a meal decision.

1. “Would you be willing to make a short seven-day record of everyday meal decisions in a format that suits you?”
2. “Would paper, a simple digital form, or a short phone check-in be easiest? It is also fine to say none of these are suitable.”
3. “Can you complete a brief entry without someone continuously assisting or supervising you?”
4. “Do you understand that you can skip any day or question, that no photos or proof are needed, and that choosing not to do the diary will not affect your interview?”
5. “Would recording a day when you are satisfied with your meals, use an alternative that works well, or do not change anything feel okay?”

Record only `diary_status`, preferred mode in the separate contact record, and later `diary_consent` using the exact tracker consent labels. A lack of smartphone use is never a reason to decline a diary; offer paper or another low-burden format.

## Researcher-only Selection rubric

Select from eligible people to fill the most important contrast gap, not from those who express the most interest. Review the tracker before scheduling and assign a short rationale in the fieldwork log, not the analytical tracker.

| Priority | Selection rule | Assumptions informed |
| --- | --- | --- |
| 1 | Protect the target: recruit independently living older adults directly and keep at least eight independently recruited older adults in the 15-person older-adult sample. | `P1`, `P2`, `U1` |
| 2 | Fill the least-covered tracker contrast: living arrangement, cooking frequency, desire to cook more (including satisfied), age band, smartphone confidence, family distance/contact, help history, or current alternatives. | `U1`, `W1`, `T1` |
| 3 | Prioritise a disconfirming case: satisfied non-cook, successful alternative, no family involvement, ignored or rejected help, or adult child who reports no concern or no involvement. | `P1`, `P2`, `B1`, `R1`, `R2` |
| 4 | Build five voluntary dyads only after each person independently qualifies and completes an individual interview; preserve individual privacy and disagreement. | `R1`, `R2`, `C1` |
| 5 | Invite diary participants across contrasting routines, including people for whom nothing needs to change and people using alternatives that work. | `P1`, `P2`, `B1`, `W1` |

High expressed interest, a founder referral, an enthusiastic adult child, willingness to use technology, or a compelling story are never positive selection criteria by themselves. When two eligible people fill the same gap, choose the person recruited independently or the one who broadens contrast coverage.

## Participant-facing outreach and scheduling copy

Use the copy below verbatim or with only local contact, availability, accessibility, and approved compensation details added. Do not add a product description or language that suggests a participant needs help.

### General community outreach

> **Invitation: everyday meal decisions and family support research**
> We are inviting adults in Toronto and the GTA to take part in a research conversation about everyday meal decisions—such as what people prepare, buy, choose not to prepare, or do instead—and the role family support may or may not play. We would like to hear from people who are satisfied with their current routines as well as people who would like something to be different.
>
> The conversation lasts about 45–60 minutes. Taking part is voluntary, and you may skip any question. This is research, not a service. To ask about eligibility or availability, contact [research contact].

### Direct older-adult invitation

> Hello [first name],
> We are inviting Toronto/GTA adults age 65+ to a research conversation about everyday meal decisions. We are interested in many experiences: cooking often, cooking rarely, using ready-made or delivered meals, eating out, receiving family help, choosing not to receive help, and being satisfied with how things are now.
>
> The conversation takes about 45–60 minutes and is entirely voluntary. It is not necessary to have a meal concern or to use a smartphone. Would you be open to a short eligibility check? You can say no or stop at any time.
>
> [Researcher name and contact]

### Adult-child or family-supporter invitation

> Hello [first name],
> We are inviting adult children and other family supporters to a research conversation about everyday meal decisions and family support. We want to hear from people who are very involved, occasionally involved, not involved, comfortable with current routines, or unsure what role is useful.
>
> The conversation is about your own experience and takes about 45–60 minutes. It is voluntary, and it does not require your family member to take part. Would you be open to a brief eligibility check?
>
> [Researcher name and contact]

### Community-organisation referral request

> Hello [organisation contact],
> We are conducting Toronto/GTA research about everyday meal decisions and family support. We are seeking a broad range of older adults and adult children/family supporters, including people who are satisfied with their routines, use alternatives that work well, or prefer little family involvement.
>
> Would you be willing to share the attached invitation through your usual public channel? Please do not nominate people based on a perceived need or provide us with anyone's contact details. Interested people can contact us directly and decide for themselves whether to complete a brief eligibility check.
>
> Thank you,
> [Researcher name and contact]

### Invitation to a separate paired follow-up

> Thank you for your individual research conversation. We are inviting a small number of family pairs to a separate 60-minute conversation about everyday meal decisions and family support. This follow-up would happen only if both of you separately choose to take part after completing your individual conversations.
>
> We will not ask either person to repeat or reveal private interview content, and the paired conversation is not for settling disagreements. It is fine to decline; your decision will not affect anything else. Would you like us to ask the other person privately whether they are also open to considering it?

### Diary invitation

> Thank you for your conversation. We are inviting some participants to keep a short seven-day record of everyday meal decisions. You can use paper, a simple digital form, or another agreed format. We are interested in ordinary days, including days when you are satisfied with your meals, use an option that works well, or make no change.
>
> The diary is optional. You may skip any entry, and no photos or proof are needed. Would you like to hear whether it could suit you?

### Confirmation message

> Thank you for agreeing to a research conversation about everyday meal decisions and family support. Your session is [date, time, format/location]. It will take about [length]. Taking part is voluntary: you may skip questions or stop at any time. If you need to reschedule, have an accessibility request, or no longer wish to take part, contact [research contact].

### Reminder message

> A reminder that your voluntary research conversation is [tomorrow/on date] at [time] by [format/location]. We will talk about everyday meal decisions and family support. If you would like to reschedule or no longer take part, please contact [research contact].

### Respectful decline message

> Thank you for letting us know. We will not contact you again about this study unless you ask us to. We appreciate your time and wish you well.

### Wait-list message

> Thank you for your interest. We are currently filling a limited set of research conversations to include a range of everyday experiences. We are not scheduling another conversation right now. With your permission, we can keep a separate contact record in case a suitable opening becomes available; saying no will not affect anything. If you prefer, we can remove your contact details now.

## Researcher-only wording safeguard

Do not add prohibited positioning to participant-facing copy. In particular, do not describe this study as **monitoring**, **diagnosis**, **health improvement**, a way to **remain independent longer**, or **AI-powered**. Those concepts are outside this research scope and can make participants feel assessed, observed, or promised a benefit.
