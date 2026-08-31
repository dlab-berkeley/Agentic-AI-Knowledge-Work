# Agentic AI for Knowledge Work: Invite the Attendees

### Learning Objectives

- Import a file into a Google Sheet through an agent.
- Send a batch of emails through an agent, after reviewing a draft.
- Verify what an agent sent by checking the result independently.
- Explain why practice emails must only go to addresses you control.

### Icons Used in This Notebook
🔔 **Question**: A quick question to help you understand what's going on.<br>
🥊 **Challenge**: Interactive exercise. We'll work through these in the workshop!<br>
💡 **Tip**: How to do something a bit more efficiently or effectively.<br>
⚠️ **Warning:** Heads-up about tricky stuff or common mistakes.<br>
✅ **Expected result**: What you should see if things went right. Small differences are fine; big ones are worth investigating.<br>

### Sections
1. [The Attendee List](#section1)
2. [Draft the Invitation](#section2)
3. [Send It](#section3)
4. [Did It Work?](#section4)

<a id='section1'></a>

# The Attendee List

The packet includes `attendees.csv`: fifteen people who want to come to your talk. Open it and look at the email addresses:

```
dlab-ai-workshop+alice@berkeley.edu
dlab-ai-workshop+ben@berkeley.edu
...
```

These are all the **same inbox**. Gmail ignores everything after a `+` in an address, so every one of these delivers to `dlab-ai-workshop@berkeley.edu` — an account D-Lab set up for this workshop. When you send fifteen invitations, fifteen emails land in that inbox, and nobody else's.

⚠️ **Warning:** This is why the list looks the way it does. Never put made-up addresses at a real domain into a sheet an agent will email. `alice@gmail.com` belongs to a real person, and the agent will happily send to it.

💡 **Tip:** The `+` trick works on your own account too. Give out `yourname+newsletters@gmail.com` and filter on it later.

Start a **new conversation**, and import the list:

```
Import packet/attendees.csv into a new Google Sheet called "Speaker Series - Attendees" in the Speaker Series folder. Keep all the columns, and add two empty columns at the end: "invited" and "rsvp". Give me the link.
```

✅ **Expected result:** A Google Sheet with 15 rows and 6 columns.

## 🥊 Challenge 3: Add the People Around You

Fifteen fake attendees are fine for practice, but a real person in the loop is better. Turn to the two or three people nearest you and ask whether you can invite them. Then:

```
Add these people to the attendee sheet: [NAME, EMAIL; NAME, EMAIL; ...]. Leave dietary needs blank. Tell me how many rows the sheet has now.
```

Make sure you're on someone else's list, too. In a few minutes, you'll receive their invitation — and that's how you'll know their agent did its job.

<a id='section2'></a>

# Draft the Invitation

Same pattern as the speaker email: draft, show me, wait.

```
Draft an invitation email to the attendees for this talk, using the event doc. Include the title, speaker, date, time, and location, and ask them to reply with a yes or no. Keep it short. Show me the draft and wait.
```

Read it. Fix it by talking to it:

```
Shorter. Put the date and time in bold. Add a line that lunch will be provided.
```

🔔 **Question:** The agent is about to send this to everyone on the sheet, from your account, with your name on it. Is there anything in the draft you'd be embarrassed by? That's the bar.

<a id='section3'></a>

# Send It

This is the moment the workshop has been building toward. Until now, the agent sent one email to one person who expected it. Now it sends a batch, to a list, from your account.

```
Send the invitation to everyone on the attendee sheet, one email each. Then add all of them as guests on the calendar event. When you're done, mark each row's "invited" column with today's date, and tell me exactly how many emails you sent and to whom.
```

The agent will ask for approval — possibly more than once. Read each request. What is it about to send, and to whom?

✅ **Expected result:** The agent reports 17–18 emails sent (15 from the packet plus your neighbors). The `invited` column is filled in. The calendar event has guests.

⚠️ **Warning:** If the agent proposes sending to an address that isn't on the sheet, deny it. That's the `AGENTS.md` rule; the approval prompt is your chance to enforce it.

<a id='section4'></a>

# Did It Work?

The agent said it sent 17 emails. Don't take its word for it. Check two ways.

**On the projector:** the instructor opens `dlab-ai-workshop@berkeley.edu`. Every invitation from every participant in the room is arriving there right now. Find yours.

**In your own inbox:** your neighbors' invitations should have arrived. Reply to each one — a yes, a no, or a maybe. Then:

```
Check my inbox for replies to the invitation. For each one, fill in the "rsvp" column on the attendee sheet with yes, no, or maybe. List anyone who hasn't replied.
```

✅ **Expected result:** The `rsvp` column filled in for your neighbors. The fifteen packet attendees listed as not yet replied — they never will; nobody is reading that inbox as Alice.

🔔 **Question:** The agent told you what it sent. Then you checked. Did the two match? In what situation would you *not* bother checking?

💡 **Tip:** "Act, then verify" is the habit. It costs one extra prompt. The agent can do the verifying for you — the point is that you ask for it.

# Key Points

- Agents can import, edit, and fill in **spreadsheets** through conversation.
- Practice emails go only to addresses you control. The `+` trick makes a whole list deliver to one inbox.
- The approval prompt is where `AGENTS.md` rules become real: you see each send before it happens.
- **Act, then verify.** The agent's report of what it did is a claim, not a receipt.
