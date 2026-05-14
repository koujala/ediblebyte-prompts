# Healthcare Professional — Structured Clinical Note from Voice Dictation

From Post 2 of the Your AI Path series: the example prompt showing what Phase 1 looks like for a healthcare professional.

The problem this solves: physicians and nurses spend an estimated 34–55% of their time on documentation. Every hour of documentation is an hour not with a patient. This prompt structures patient notes from a voice dictation in real time — patient notes drafted before the next encounter, not batched at the end of a 10-hour shift.

**Note:** All AI-generated clinical documentation requires clinician review before use in any medical record. The professional's judgment is the final authority.

## The prompt

```
Based on this voice note from a patient encounter, create a structured clinical note in SOAP format:

[paste or transcribe voice note]

Flag anything that needs clarification.
```

## How to use

Dictate or type the patient encounter as you naturally describe it — chief complaint, history, what you observed, your assessment, your plan. Don't restructure it first; let the model do the formatting work. Ask it to flag ambiguous or incomplete sections so you know exactly what to review before signing.

Keep clinical language accurate — tell the model not to simplify to lay terms in the note itself.

See [`../series_ai_learning_path_4_one_win_per_role/healthcare_soap_note.md`](../series_ai_learning_path_4_one_win_per_role/healthcare_soap_note.md) for the fully structured template version with placeholders.
