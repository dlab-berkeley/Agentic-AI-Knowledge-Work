# Agentic AI for Knowledge Work: Plan the Talk

### Learning Objectives

- Delegate document creation to an agent and review the result.
- Send a first email through an agent, with a draft-and-approve step.
- Use an agent to find free time on a calendar and create an event.
- Identify decisions the agent made that you did not ask for.

### Icons Used in This Notebook
🔔 **Question**: A quick question to help you understand what's going on.<br>
🥊 **Challenge**: Interactive exercise. We'll work through these in the workshop!<br>
💡 **Tip**: How to do something a bit more efficiently or effectively.<br>
⚠️ **Warning:** Heads-up about tricky stuff or common mistakes.<br>
✅ **Expected result**: What you should see if things went right. Small differences are fine; big ones are worth investigating.<br>

### Sections
1. [Pick a Speaker](#section1)
2. [The Event Doc](#section2)
3. [Invite the Speaker](#section3)
4. [Find a Time](#section4)
5. [Has the Speaker Replied?](#section5)

<a id='section1'></a>

# Pick a Speaker

Today's scenario: you are organizing a talk in the **D-Lab Speaker Series**. Every task in this workshop is something a real organizer does — and every one of them can be handed to an agent.

First, you need a speaker. The speaker has to be someone who can actually reply to an email during this workshop, so pick one of these:

- **Someone sitting near you.** Ask them. They get a real invitation and reply to it. This is the best option.
- **The fake speaker.** Use the address `dlab-ai-workshop+speaker@berkeley.edu`. Invitations go to the instructor's inbox; we'll reply to a few of them on the projector.
- **Yourself**, if you're on a fresh throwaway account.

⚠️ **Warning:** Do not invite a real researcher who isn't in the room. Today's emails are practice. An unexpected invitation to a real person's inbox is not.

Agree on a topic with your speaker — anything they could plausibly give a talk about. "How I organize my fieldwork notes" is a fine talk.

<a id='section2'></a>

# The Event Doc

Start a **new conversation**. Then fill in the event template:

```
Read packet/event_template.md. Fill it in for a talk by [SPEAKER NAME] ([SPEAKER EMAIL]) on [TOPIC]. Write a short bio, a title, and an abstract. Leave the date and time blank for now. I am the organizer; use my name and email.

Save the result as a Google Doc called "Speaker Series - [SPEAKER NAME]" inside a Drive folder called "Speaker Series". Give me the link.
```

The agent will ask for approval before it touches your Drive. Read what it proposes, then approve.

✅ **Expected result:** A new folder in your Google Drive, with a filled-in event doc inside it. Open the link and read it.

🔔 **Question:** The agent wrote a bio and an abstract from two sentences of input. Is anything in the doc untrue? How would a reader know which parts were invented?

💡 **Tip:** If the speaker is a public researcher, the agent can search the web for their actual work: add "Look up their recent work online first" to the prompt. For a neighbor, just tell it two things about them.

<a id='section3'></a>

# Invite the Speaker

This is the first email of the day. Notice the shape of the prompt: **draft, show me, then wait.**

```
Draft an email to the speaker inviting them to give this talk, based on the event doc. Keep it under 150 words. Mention that we'll confirm the date once we've checked calendars. Show me the draft and wait for my approval before sending.
```

Read the draft. Change anything you like, in plain language: "Make it warmer." "Don't call it an honor." "Sign it with my first name only." Then:

```
Send it.
```

The agent asks for approval one more time — this is the `Ask for approval` setting doing its job — and the email goes out.

✅ **Expected result:** One sent email in your Gmail. Your speaker has it in their inbox.

🔔 **Question:** You read the draft before it went. Would you have, if the rule in `AGENTS.md` hadn't forced it? What would it take for you to trust the agent to send without showing you?

<a id='section4'></a>

# Find a Time

The speaker doesn't know the date yet because we haven't picked one. Let the agent read your calendar.

💡 **Tip:** On a fresh account with an empty calendar, this task is too easy. First, ask the agent to add the commitments listed in `packet/calendar_commitments.md` to your calendar.

```
Look at my calendar for the next three weeks. Suggest three slots for a 90-minute talk on a weekday afternoon that don't conflict with anything. Tell me what you had to work around.
```

Pick one. Then:

```
Create a calendar event called "D-Lab Speaker Series: [TALK TITLE]" at [YOUR CHOSEN SLOT], at the location in the event doc. Don't add any attendees yet. Then update the event doc with the date and time.
```

✅ **Expected result:** An event on your calendar, and the date filled in on the Google Doc.

<a id='section5'></a>

# Has the Speaker Replied?

By now, your neighbor has an invitation sitting in their inbox. Reply to the one you received — a yes, a no, or a question. Then ask your agent to check yours:

```
Has the speaker replied to my invitation yet? If so, summarize what they said. If they asked anything, draft a reply for me to look at.
```

This is the first time the agent has *read* your inbox rather than written to it. Look at what it did: which emails it searched, and which it opened.

🔔 **Question:** Look at the steps the agent took to find the reply. Did it search for "Speaker Series" like the rules say, or did it look more widely?

## 🥊 Challenge 2: What Did the Agent Decide?

Scroll back through this lesson's conversations. List three things the agent decided that you did not ask for. Some places to look:

- The abstract: what claims did it make about the talk?
- The invitation: what tone, what sign-off, what subject line?
- The calendar: what counts as "afternoon"? Did it leave buffer time around your other meetings?

Share one with the room. The point isn't that these decisions were wrong. It's that they were invisible until you looked.

# Key Points

- An agent can turn a template and two sentences into a finished document — including parts it invented.
- **Draft, show me, wait** is the pattern for anything that leaves your account.
- The agent can read your calendar and inbox, not just write to them. Check *how* it looked.
- Every prompt leaves decisions unspecified. The agent makes them silently. Go find them.
