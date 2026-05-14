# Project Manager — Meeting Notes to Stakeholder Update

From Post 2 of the Your AI Path series: the example prompt showing what Phase 1 looks like for a project manager.

The problem this solves: PMs spend an estimated 30–40% of their time on status reporting — summarising what happened for people who weren't in the room. This is transcription, not project management. This prompt turns 45 minutes of post-meeting admin into 4 minutes of reviewing.

## The prompt

```
Here are the notes from a 45-minute project sync meeting.

[paste raw meeting notes]

Extract:
1. Decisions made
2. Action items with owner and due date
3. Blockers that need escalation
4. A two-paragraph stakeholder update I can send by email
```

## How to use

Paste the raw notes — unedited, messy, however you captured them in the room. The model handles the structure. Specify who the stakeholder email is going to (exec level, client, team) so the tone is appropriate. If blockers need to go to a specific person or team, mention that in your follow-up.

Iterate: if the stakeholder update is too long or uses the wrong tone, reply with one specific instruction and run it again.

See [`../series_ai_learning_path_4_one_win_per_role/pm_meeting_notes_to_stakeholder_update.md`](../series_ai_learning_path_4_one_win_per_role/pm_meeting_notes_to_stakeholder_update.md) for the fully structured template version with placeholders.
