---
name: bilingual-meeting-minutes
description: Turns a meeting transcript, recording summary or rough notes into concise minutes in English, Arabic or both - decisions, action items with owner and due date, open questions and a parking lot - without inventing anything that was not said. Handles mixed Arabic-English speech. Use when someone pastes a transcript or notes and asks for minutes, a recap email, action items, or "what did we decide".
---

# Bilingual Meeting Minutes

Minutes exist so that people who were not in the room can act. Optimise for decisions and actions, not for a record of who said what.

## When to use
- A transcript (auto-generated or manual), chat log or bullet notes needs to become minutes.
- A recap email must go out after a call.
- The meeting mixed Arabic and English and the minutes are needed in one or both.

## Inputs to confirm
- Meeting title, date, attendees (and absentees if relevant).
- Output language: EN, AR, or both (side by side or one after the other).
- Audience: internal team, client-facing, or executives (affects detail and tone).
If attendees are not listed, infer them from speakers and mark the list "(from transcript)".

## Method
1. **Clean pass.** Ignore small talk, repeated points and transcription noise. Merge statements that the same speaker repeats.
2. **Find decisions.** A decision is a commitment the group accepted: "we will...", "agreed", "let's go with", "خلاص نعتمد", "اتفقنا". A proposal nobody accepted is an open question, not a decision.
3. **Find actions.** Look for verbs of commitment plus a person: "I'll send", "Ahmed will check", "هبعتلك", "سأرسل". For each, capture owner, action, due date. If no date was said, write `due: not set` - do not invent one.
4. **Find open questions.** Anything asked and not resolved, or explicitly deferred ("let's confirm with finance").
5. **Parking lot.** Topics raised but out of scope for this meeting.
6. **Risks or blockers** only if someone stated them.
7. **Verify.** Every decision and action should be traceable to a line in the source. If unsure who owns something, write `owner: unclear` and list it in open questions.

## Language handling
- Speakers often switch languages mid-sentence. Capture meaning, not wording.
- Arabic minutes use Modern Standard Arabic even if the speech was colloquial (Gulf, Egyptian, Levantine). Keep names, product names and acronyms in their original script.
- Dates: write in an unambiguous form (e.g. 12 Nov 2026 / ١٢ نوفمبر ٢٠٢٦). Note the timezone if attendees were in different ones.
- Bilingual output: produce each language natively; do not align sentence by sentence.

## Output format
```
# <Meeting title> - <date>
Attendees: ...
Purpose: one line

## Decisions
1. ...

## Action items
| # | Action | Owner | Due |
|---|---|---|---|

## Open questions
- ... (who will answer, if known)

## Parking lot
- ...

## Next meeting
date / not set
```
Arabic headings: القرارات، المهام، أسئلة مفتوحة، مواضيع مؤجلة، الاجتماع القادم.
Target length: one screen. Decisions and actions first; no narrative summary unless asked.

## Worked example
Source excerpt: "Nora: so we launch the pilot on the 15th? Omar: yes, agreed. Omar: I'll share the test accounts by Sunday. Layla: what about pricing for the second phase? Nora: let's leave that for finance."
- Decision: Pilot launches on 15 Nov.
- Action: Omar - share test accounts - due Sunday (date to confirm).
- Open question: Phase 2 pricing - finance to advise.

## Pitfalls
- Recording discussions as decisions.
- Assigning actions to "the team" - push for a named owner or flag it.
- Inventing deadlines to make the table look complete.
- Translating colloquial phrases literally into the Arabic minutes.
- Including sensitive side remarks (personal, HR) that do not belong in shared minutes - leave them out and mention to the requester that you did.
