# Agentic AI for Knowledge Work: Invite the Attendees

### Learning Objectives

- Import a file into a Google Sheet through an agent.
- Send a batch of emails through an agent, after reviewing a draft.
- Verify what an agent sent by checking the result independently.

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

Note: these are all technicaly the **same inbox**. Gmail ignores everything after a `+` in an address, so every one of these delivers to `dlab-ai-workshop@berkeley.edu`, an account D-Lab set up for this workshop.

💡 **Tip:** The `+` trick works on your own account too. Give out `yourname+newsletters@gmail.com` and filter on it later.

Start a **new conversation**, and import the list:

```
Import packet/attendees.csv into a new Google Sheet called "Speaker Series - Attendees" in the Speaker Series folder. Keep all the columns, and add two empty columns at the end: "invited" and "rsvp". Give me the link.
```

✅ **Expected result:** A Google Sheet with 15 rows and 6 columns.

## 🥊 Challenge 3: Add the People Around You

Let's add some more attendees to our event. Ask a few people around you for their emails (if they're OK receiving an invitation); then, add them to the following prompt:

```
Add these people to the attendee sheet: [NAME, EMAIL; NAME, EMAIL; ...]. Leave dietary needs blank. Tell me how many rows the sheet has now.
```

Make sure you're on someone else's list, too. In a few minutes, you should receive their invitation.

<a id='section2'></a>

# Draft the Invitation

Now, let's draft an invitation email to the new attendees. Use the following prompt:

```
Draft an invitation email to the attendees for this talk, using the event document. Include the title, speaker, date, time, and location, and ask them to reply with a yes or no. Keep it short. Show me the draft and wait.
```

Read it. Try asking the agent to make changes:

```
Shorter. Put the date and time in bold. Add a line that lunch will be provided.
```

Once again: we're not advocating that you actually do this in your day-to-day practice. However, there are probably times where you need to do rote operations that can be better served by delegating to an agent.

<a id='section3'></a>

# Send the Invitations

Now, we're going to send out all the invitations. Use the following prompt:

```
Send the invitation to everyone on the attendee sheet, one email each. Then add all of them as guests on the calendar event. When you're done, mark each row's "invited" column with today's date, and tell me exactly how many emails you sent and to whom.
```

The agent will ask for approval, possibly more than once. Read each request. What is it about to send, and to whom?

✅ **Expected result:** The agent reports 17–18 emails sent (15 from the packet plus your neighbors). The `invited` column is filled in. The calendar event has guests.

⚠️ **Warning:** If the agent proposes sending to an address that isn't on the sheet, deny it.

<a id='section4'></a>

# Did It Work?

The agent said it sent 17 emails. We should double check that it actually did so.

First, let's look in the D-Lab inbox to see if the instructor has received the invitations.

Next, check your own inbox for your neighbors' invitations. Go ahead and reply to the invitations (maybe ask your agent to!).

Then, use the following prompt to check for updates to *your* event:

```
Check my inbox for replies to the invitation. For each one, fill in the "rsvp" column on the attendee sheet with yes, no, or maybe. List anyone who hasn't replied.
```

✅ **Expected result:** The `rsvp` column filled in for your neighbors. The fifteen packet attendees listed as not yet replied — they never will; nobody is reading that inbox as Alice.

# Key Points

- Agents can import, edit, and fill in **spreadsheets**.
- You can create multiple drafts and send out multiple emails using agents.
- Double check that the agent is doing what you think it is doing.
