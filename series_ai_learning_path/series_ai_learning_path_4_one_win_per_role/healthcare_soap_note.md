# Healthcare Professional — SOAP Note from Voice Dictation

The highest-impact Basics Phase move for a healthcare professional: a structured clinical note from a voice dictation — before the next patient.

**What changes:** Notes drafted between patients instead of batched at the end of a 10-hour shift.

**Note:** All AI-generated clinical documentation requires clinician review before use in any medical record. The professional's judgment is the final authority.

## The prompt

```
I'm going to describe a patient encounter. Create a structured SOAP note from what I say.

Patient encounter:
[Dictate or type: chief complaint, history, examination findings, assessment, plan]

Format it as:
- S (Subjective): what the patient reported
- O (Objective): examination findings and observations
- A (Assessment): your diagnosis / differential
- P (Plan): treatment, referrals, follow-up

Flag anything that's ambiguous or that you'd want me to clarify before signing.
Keep clinical language accurate — don't simplify to lay terms in the note itself.
```

## How to use

Dictate or type the patient encounter as you naturally describe it after the visit — chief complaint, relevant history, what you observed and examined, your assessment, your plan. Don't restructure it first; let the model do the formatting work.

The instruction to flag ambiguous or incomplete sections is critical: it surfaces what needs your review before signing. Don't skip this step — it's what makes the prompt safe to use in a clinical workflow.

The "keep clinical language accurate" instruction prevents the model from paraphrasing medical terminology into lay terms. Verify this in the output — it can occasionally simplify language that needs to remain precise.
