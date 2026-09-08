# Agentic AI for Knowledge Work: Invite the Attendees

### Learning Objectives

- Import a file into a Google Sheet through an agent.
- Ask an agent to describe who is on a list, and check its claims against the data.
- Send a batch of emails through an agent, after reviewing a draft.
- Verify what an agent sent by checking the result independently.
- Turn a set of messy replies into structured columns.

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
5. [From Inbox to Spreadsheet](#section5)

<a id='section1'></a>

# The Attendee List

The packet includes `attendees.csv`: fifteen people who want to come to your talk. Open it and look at the email addresses:

```
dlab-ai-workshop+alice@berkeley.edu
dlab-ai-workshop+ben@berkeley.edu
...
```

Note: these are all technically the **same inbox**. Gmail ignores everything after a `+` in an address, so every one of these delivers to `dlab-ai-workshop@berkeley.edu`, an account D-Lab set up for this workshop.

💡 **Tip:** The `+` trick works on your own account too. Give out `yourname+newsletters@gmail.com` and filter on it later.

Start a **new conversation**, and import the list:

```
Import packet/attendees.csv into a new Google Sheet called "Speaker Series - Attendees" in the Speaker Series folder. Keep all the columns, and add two empty columns at the end: "invited" and "rsvp". Give me the link.
```

✅ **Expected result:** A Google Sheet with 15 rows and 9 columns.

## Who Is Coming?

The sheet has more than names and emails. Before you ask the agent anything, skim it and write down one thing you notice.

```
Look at the attendee sheet. Who is coming? Give me three observations useful to the organizer, and say which rows each one rests on. Is any group missing or underrepresented?
```

🔔 **Question:** Did it find what you found? Did it claim anything the data can't support? Fifteen rows is a small sample. Watch for confident claims.

## 🥊 Challenge 3: Add the People in the Room

The fifteen people on your sheet can't reply to email. Let's add some who can.

In person: ask a few people around you for their emails. On Zoom: post your name and email in the chat if you're OK with receiving practice invitations. Only post an address you're happy for everyone in the workshop to see.

By signing up, you'll receive a real invitation from someone else's agent. Reply to it, but don't just say yes. Add a question, a maybe, or a dietary need. Their agent will have to make sense of it.

Now put three or four of the entries you collected into this prompt, exactly as people gave them to you. Copy them from the chat, or type them in as you jotted them down:

```
Here are some people from the workshop: [PASTE]. Add each of them to the attendee sheet. Leave the other columns blank. Tell me how many rows the sheet has now, and flag anything you weren't sure how to read.
```

Make sure you're on other people's lists, too. In a few minutes, you should receive their invitations.

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

Now make one change of your own. Check whether the agent kept your earlier changes when it applied the new one.

Once again: we're not advocating that you actually do this in your day-to-day practice. However, there are probably times where you need to do rote operations that can be better served by delegating to an agent.

<a id='section3'></a>

# Send the Invitations

Now, we're going to send out all the invitations. Use the following prompt:

```
Send the invitation to everyone on the attendee sheet, one email each. Then add all of them as guests on the calendar event. When you're done, mark each row's "invited" column with today's date, and tell me exactly how many emails you sent and to whom.
```

The agent will ask for approval, possibly more than once. Read each request. What is it about to send, and to whom?

✅ **Expected result:** The agent reports 15+ emails sent (from the packet, plus the people you added). The `invited` column is filled in. The calendar event has guests.

⚠️ **Warning:** If the agent proposes sending to an address that isn't on the sheet, deny it.

<a id='section4'></a>

# Did It Work?

The agent said it sent the emails. We should double check that it actually did so.

First, let's look in the D-Lab inbox to see if the instructor has received the invitations.

Next, check your own inbox for invitations from other participants. Reply to them now, with the wrinkle you promised in Challenge 3. These replies are real. Your agent has to find them in your inbox.

Then, use the following prompt to check for updates to *your* event:

```
Check my inbox for replies to the invitation. For each one, fill in the "rsvp" column on the attendee sheet with yes, no, or maybe. List anyone who hasn't replied.
```

✅ **Expected result:** The `rsvp` column filled in for anyone who has replied so far. The fifteen packet attendees listed as not yet replied. Nobody is reading that inbox as Alice.

If nobody has replied yet, that's expected. Other people are still sending. The skill you write in lesson 5 will catch them later.

💡 **Tip:** The people you added also got a calendar invitation. If they accepted or declined it, ask the agent whether the calendar responses match the email replies.

<a id='section5'></a>

# From Inbox to Spreadsheet

The packet attendees can't reply, so we wrote their replies for them. These replies are scripted so everyone gets the same hard cases. Open `packet/replies.md`. It looks like an inbox: some say yes, some say no, and several say something in between.

Before you hand it to the agent, decide for yourself: what does "I'll try to make it" count as? What about someone who asks whether the talk is hybrid?

```
Read packet/replies.md. These are replies to the invitation. For each one, fill in the "rsvp" column on the attendee sheet with yes, no, or maybe, and add two columns: "question" for anything they asked and "notes" for anything else the organizer should know. Don't add or remove rows. Then list every question that needs an answer, and anyone who replied who isn't on the sheet.
```

✅ **Expected result:** The `rsvp` column filled in for everyone who replied. Two new columns. A list of open questions, and one sender flagged as not on the sheet.

🔔 **Question:** Where did the agent's categories differ from yours? Did it try to add the two colleagues? What did it do with the person who asked to be removed?

# Key Points

- Agents can import, edit, and fill in **spreadsheets**.
- You can create multiple drafts and send out multiple emails using agents.
- Double check that the agent is doing what you think it is doing.
- Agents can turn messy text into a table. You decide the categories.
- Small data invites confident claims. Check them against the rows.
