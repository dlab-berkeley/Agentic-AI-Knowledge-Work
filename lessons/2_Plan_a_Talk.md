# Agentic AI for Knowledge Work: Plan the Talk

### Learning Objectives

- Delegate document creation to an agent and review the result.
- Send an email with an agent.
- Use an agent to find free time on a calendar and create an event.
- Identify decisions the agent made that you did not ask for.

### Icons Used in This Notebook
🔔 **Question**: A quick question to help you understand what's going on.<br>
🥊 **Challenge**: Interactive exercise. We'll work through these in the workshop!<br>
💡 **Tip**: How to do something a bit more efficiently or effectively.<br>
⚠️ **Warning:** Heads-up about tricky stuff or common mistakes.<br>
✅ **Expected result**: What you should see if things went right. Small differences are fine. Big ones are worth investigating.<br>

### Sections
1. [Pick a Speaker](#section1)
2. [The Event Document](#section2)
3. [Invite the Speaker](#section3)
4. [Find a Time](#section4)
5. [Has the Speaker Replied?](#section5)

<a id='section1'></a>

# Pick a Speaker

Today's scenario: you are organizing a talk in the **D-Lab Speaker Series**. Every task in this workshop is something you might actually do while planning an event. An agent can handle many of these tasks, to varying degrees.

First, you will choose a "speaker". For the purposes of this workshop, the speaker has to be someone who can actually reply to an email in the next hour or so, so pick one of these:

- **Someone sitting near you.** Ask for their email, and have them pretend to be your speaker. Make sure they're OK with receiving an email from an agent.
- **A fake speaker.** Choose a `[SPEAKER NAME]`. Then use the address `dlab-ai-workshop+[SPEAKER NAME]@berkeley.edu` (no spaces). We control this inbox, so we can respond to some of the invitations.

⚠️ **Warning:** **Do not invite someone who isn't in the room!** This is not a real event. Today's emails are just practice.

<a id='section2'></a>

# The Event Document

Along with your speaker, choose a topic for the event. It can be silly; just make it distinct. For the next step, you should have the following on hand:
- `[SPEAKER NAME]`: The name of your speaker.
- `[SPEAKER EMAIL]`: Your speaker's email.
- `[TOPIC]`: The topic of the talk.

Now, start a **new conversation**. Copy the following prompt, filling in the information above:

```
Read packet/event_template.md. Fill it in for a talk by [SPEAKER NAME] ([SPEAKER EMAIL]) on [TOPIC]. Write a short bio, a title, and an abstract. Leave the date and time blank for now. I am the organizer. Use my name and email.

Save the result as a Google Doc called "Speaker Series - [SPEAKER NAME]" inside a Drive folder called "Speaker Series". Give me the link.
```

The agent will ask for approval before it touches your Drive. Read what it proposes, then approve.

✅ **Expected result:** A new folder in your Google Drive, with a filled-in event doc inside it. Open the link and read it.

🔔 **Question:** Did the agent get your name and email right? If so, how did it know this information?

🔔 **Question:** The agent wrote a bio and an abstract from two sentences of input. Is anything in the doc untrue? How would a reader know which parts were invented?

💡 **Tip:** If the speaker is a public researcher, the agent can search the web for their actual work. Add "Look up their recent work online first" to the prompt.

<a id='section3'></a>

# Invite the Speaker

Next, we're actually going to send an email. Use the following prompt:

```
Draft an email to the speaker inviting them to give this talk, based on the event document. Keep it under 150 words. Mention that we'll confirm the date once we've checked calendars. Show me the draft and wait for my approval before sending.
```

Read the draft. Change anything you like, in plain language. Then:

```
Send it.
```

The agent asks for approval one more time, provided you have the correct approval setting. Once it receives approval, it will send the email.

✅ **Expected result:** One sent email in your Gmail. Your speaker has it in their inbox.

🔔 **Question:** You read the draft before it went. Would you have, if the rule in `AGENTS.md` hadn't forced it? What would it take for you to trust the agent to send without showing you?

⚠️ **Warning:** We're not actually advocating that you completely hand off all aspects of communication to an agent. In fact, we recommend the opposite: it's better to write your own emails, especially when you have a working relationship with the recipient. The purpose of this exercise is to demonstrate how to send an email with an agent.

For example, one use case for this might be to write an email draft yourself that needs to go out to 5 people, and have an agent create email drafts for each recipient, changing the names accordingly. Using the agent in this way will save you time, but still maintain your voice in workplace communications.

<a id='section4'></a>

# Find a Time

Let's pick a time for the event by having the agent look at the calendar.

This can go one of two ways. If you connected your real calendar, you can ask the agent to look through it for an opening.

If you made a fresh account, then your calendar will be empty. Ask the agent to add the commitments in `packet/calendar_commitments.md` to your calendar:

```
Read packet/calendar_commitments.md and add each commitment to my calendar.
```

Next, use the following prompt:

```
Look at my calendar for the next three weeks. Suggest three slots for a 90-minute talk on a weekday afternoon where I am free. Tell me what you had to work around.
```

Pick one slot. Then fill it in below and use the following prompt:

```
Create a calendar event called "D-Lab Speaker Series: [TALK TITLE]" at [YOUR CHOSEN SLOT], at the location in the event doc. Don't add any attendees yet. Then update the event doc with the date and time.
```

✅ **Expected result:** An event on your calendar, and the date filled in on the Google Doc.

<a id='section5'></a>

# Has the Speaker Replied?

By now, your speaker has an invitation sitting in their inbox. If you are someone else's speaker, reply to their email now. Then ask your agent to check your inbox:

```
Has the speaker replied to my invitation yet? If so, summarize what they said. If they asked anything, draft a reply for me to look at.
```

This is the first time the agent has *read* your inbox rather than written to it.

🔔 **Question:** What steps did the agent take to look for the reply? Did it search for "Speaker Series" like the rules say, or did it look more widely?

## 🥊 Challenge 2: What Did the Agent Decide?

Scroll back through this lesson's conversations. List three things the agent decided that you did not ask for. Some places to look:

- The abstract: what claims did it make about the talk?
- The invitation: what tone, what sign-off, what subject line?
- The calendar: what counts as "afternoon"? Did it leave buffer time around your other meetings?

How would you do the above steps differently in the real world? Where would you exert more control, and where would you cede decision-making to the agent? *Would you use the agent at all?*

# Key Points

- An agent can take actions in your email, documents, and calendar.
- Agents can both read and write in your workspaces, and you can set rules for how they do so.
- Every prompt leaves decisions unspecified. Agents will often make assumptions in these cases.
