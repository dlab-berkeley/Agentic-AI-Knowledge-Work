---
name: event-status
description: Check on a D-Lab Speaker Series talk — find new RSVP replies, update the attendee sheet, draft replies to questions, pull new feedback survey responses, and report what changed. Use when the user asks for an event status, RSVP update, or "check on the talk."
---

# Event Status

Reference solution for lesson 5. Participants write their own version by describing it to the agent; this one is here for comparison.

## What this skill needs

- A Google Sheet named "Speaker Series - Attendees" with columns `name`, `email`, `invited`, `rsvp`.
- A Google Doc in the "Speaker Series" Drive folder with the event details and, optionally, a "Feedback summary" section.
- `credentials.txt` in the project folder, if a Qualtrics survey exists.

## Rules

- Never send anything. Drafts only. The user approves and sends.
- Only read emails that mention "Speaker Series".
- Never print the contents of `credentials.txt`.

## Steps

1. **Find new replies.** Search the inbox for emails mentioning "Speaker Series" received since the last run. If there is no record of a last run, use the `invited` date on the sheet. Keep track of the run time by appending a line to `event_status_log.txt` in the project folder.
2. **Update the sheet.** For each reply from an address on the attendee sheet, set `rsvp` to `yes`, `no`, or `maybe` based on what they said. If a reply is ambiguous, set `maybe` and flag it in the report.
3. **Draft replies to questions.** If a reply asks a question (about parking, Zoom, timing, food), draft an answer using the event doc. Save each draft in Gmail as a draft. Do not send.
4. **Pull survey responses.** If the event doc contains a Qualtrics survey link, download any responses newer than the last run using the credentials in `credentials.txt`. Append them to the "Feedback summary" section of the event doc: updated average score, new themes, new speaker suggestions.
5. **Report.** Five lines or fewer:
   - How many new replies, and the yes/no/maybe counts on the sheet now.
   - Who asked a question, and that a draft is waiting.
   - How many new survey responses.
   - Anyone on the sheet who still hasn't replied.
   - Anything that went wrong.

## Example report

```
3 new replies. Sheet now: 6 yes, 1 no, 2 maybe, 9 no reply.
Grace Lin asked about parking — draft saved in Gmail.
2 new survey responses; average usefulness now 4.3.
Still no reply: Ben, Dev, Farid, Hugo, Jonas, Luis, Maya, Noah, Priya.
Nothing sent.
```
