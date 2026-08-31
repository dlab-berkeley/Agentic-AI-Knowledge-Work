<img class="logo" src="assets/dlab-bubble-logo-2025-final-margin.png" alt="D-Lab">

# Agentic AI for Knowledge Work

<p class="subtitle">UC Berkeley D-Lab</p>

Note:
Welcome. Don't linger here; go straight to the demo.

---

## A demo

Note:
Two minutes, no more. Show the finished state from the instructor account: the event doc in Drive, the sent invitations in Gmail, the calendar event with guests, the flyer, the survey link. Click through them. Don't explain how yet. This is what everyone will have built by the end.

---

## The prompt

```text
Organize a D-Lab Speaker Series talk with Alice Nakamura:
fill in the event doc, invite her, find a time, email the
attendee list, make a flyer, and set up a feedback survey.
```

Nothing was typed into Gmail, Calendar, Drive, or Qualtrics by hand.

Note:
Reveal the prompt only after the demo. The gap between one sentence and the finished event is the hook. Today we do it step by step — and lesson 5 sends everyone home with the pattern to apply to their own recurring work.

---

## Chatbots

<div class="chat">
  <div class="msg user">Write an email inviting my lab to Thursday's talk.</div>
  <div class="msg bot">
    <div class="codebox"><div class="codebar"><span>email</span><span>Copy</span></div><pre>Subject: Talk this Thursday

Hi all — please join us Thursday at 2 pm for ...</pre></div>
    Let me know if you'd like a different tone!
  </div>
  <div class="msg user">Great. Now send it to everyone on my list and put it on the calendar.</div>
  <div class="msg bot">I can't send emails or access your calendar, but here's how you can do that yourself ...</div>
</div>

Nothing happens unless you make it happen.

Note:
Most of the room has used ChatGPT for drafts. Name the copy-paste loop: the chatbot writes, you ferry it to Gmail, you fix the names, you add it to the calendar. The tell is the "Copy" button. The model can't see your accounts.

---

## Agents

<div class="appwin">
  <div class="titlebar"><span class="dots"><i></i><i></i><i></i></span><span>Codex — speaker-series</span></div>
  <div class="appbody">
    <div class="sidebar">
      <div class="thread active">Invite attendees</div>
      <div class="thread">New thread</div>
    </div>
    <div class="mainpane">
      <div class="msg user">Invite everyone on the attendee sheet to Thursday's talk.</div>
      <div class="step">Read <code>Speaker Series - Attendees</code> · 17 rows</div>
      <div class="step">Read event doc · title, date, location</div>
      <div class="step">Drafted invitation · waiting for approval</div>
      <div class="step ok">Sent 17 emails · added 17 guests to calendar event</div>
      <div class="reply">Done. 17 invitations sent; the <code>invited</code> column is filled in. Nobody has replied yet.</div>
    </div>
  </div>
</div>

Same model. It read the sheet, drafted, waited for you, then did it.

Note:
Point at the mock: the agent read the sheet and the doc itself, drafted, and — this is the line to point at — waited for approval before sending. Rule of thumb: chatbot for a draft you'll copy; agent when the work involves your actual email, calendar, or files.

---

## Knowledge work with agents

1. Give the agent context
2. Have it draft
3. Review and approve
4. Verify what it did
5. Go to step 1

You approve anything that leaves your account.

Note:
The one concept that makes everything else make sense: an agent is a model with tools and permission to keep going. The brake is the approval gate. Today's `AGENTS.md` rule is "always draft first" and the permission setting is "ask for approval" — belt and suspenders. Lesson 1 covers both hands-on.

---

## What are you handing over?

> Read, compose, send, and permanently delete all your email from Gmail

> See, edit, create, and delete all of your Google Drive files

This is the consent screen. Most people don't read it.

Note:
Put the real consent screen on the projector when we connect plugins in lesson 1 and read it aloud. This is the honest answer to "what am I giving ChatGPT?" Two things make it OK: the approval setting is what stands between "can" and "does", and you can revoke it afterward (Google account → Security → third-party connections). People who'd rather not connect their real account were told to make a fresh one — that's fine too.

---

## One prompt, a hundred decisions

Whatever you don't specify, the agent decides for you.

Note:
Go back to the demo prompt: what tone for the invitation? Which afternoon? What's in the abstract? Who gets the flyer? The prompt said none of it and the agent decided all of it. None of the decisions were wrong; all of them were invisible. Every lesson today ends with the same question: what did the agent decide that you didn't specify?

---

## From draft to autopilot

| Lesson | The agent... | You... |
|---|---|---|
| 2 | drafts a doc, sends one email | read it first |
| 3 | emails a whole list | approve each send |
| 4 | publishes a flyer and a page | preview, then publish |
| 5 | runs a survey, then runs itself | wrote the rules |

Note:
The arc of the day. Each lesson hands the agent a bit more autonomy, and each time there's a deliberate moment where you decide it's earned it. By lesson 5, "run the event-status skill" does in one word what took all afternoon — because you spent the afternoon learning what it takes to trust it.

---

## The agent explains itself

<img class="screenshot" src="assets/mollick-agent-status.png" alt="A dense, jargon-filled agent status report">

Is the work unclear, or just the explanation? <span class="muted">(via Ethan Mollick)</span>

Note:
A real agent status report after a long autonomous stretch (shared by Ethan Mollick). On long tasks agents drift into private jargon. If you're nodding along without understanding, stop and ask: "explain what you just did, plainly." Speed is the default; comprehension is a choice you keep making. That's also why every lesson today has a verify step.

---

## Not just Codex

| | |
|---|---|
| **Codex** | free ChatGPT account · Gmail, Drive, Calendar plugins |
| **Claude** | Cowork and Claude Code · connectors and skills |
| **Gemini** | inside Google Workspace · Gmail, Docs, Calendar built in |

The habits transfer: rules, draft-first, verify.

Note:
We use Codex today because the free tier covers the workshop and the plugins are one click. Claude's Cowork and Claude Code do the same job with connectors; Gemini lives inside Workspace already. Pricing and features shift every few months — true as of August 2026. Everything today transfers.

---

## Structure of today's workshop

Today, we will use an agent to:

1. Plan a D-Lab Speaker Series talk and invite the speaker,
2. Email the attendee list and track replies,
3. Make a flyer and an event page, and
4. Run a feedback survey — then wrap it all into one reusable skill.

Let's begin by opening lesson 1 (`lessons/1_Introduction_and_Setup.md`) in your browser.

Note:
Drop the materials link in the chat and check everyone has it open before leaving this slide. Five lessons, one event; the slides end here and the rest of the session lives in Codex and the lesson pages. The demo prompt returns in lesson 5 as the take-home: apply the pattern to your own recurring work.
