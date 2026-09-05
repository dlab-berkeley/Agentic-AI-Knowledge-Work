# Agentic AI for Knowledge Work: Beyond Plugins, and Automation

### Learning Objectives

- Connect an agent to a service that has no plugin, using an API token.
- Store a credential in a file the agent can use without revealing it.
- Create and collect a survey through an agent.
- Write a skill that turns today's tasks into one reusable command.

### Icons Used in This Notebook
🔔 **Question**: A quick question to help you understand what's going on.<br>
🥊 **Challenge**: Interactive exercise. We'll work through these in the workshop!<br>
💡 **Tip**: How to do something a bit more efficiently or effectively.<br>
⚠️ **Warning:** Heads-up about tricky stuff or common mistakes.<br>
✅ **Expected result**: What you should see if things went right.<br>

### Sections
1. [When There Is No Plugin](#section1)
2. [Your Qualtrics Token](#section2)
3. [Create the Survey](#section3)
4. [Collect Responses](#section4)
5. [Write Your Own Skill](#section5)
6. [Where to Go From Here](#section6)

<a id='section1'></a>

# When There Is No Plugin

The key to having an agent take actions for you is that it has a way of interfacing with the relevant product. OpenAI facilitates this in Codex with plugins: we installed the Gmail, Drive, and Calendar plugins. These plugins exposed the necessary functons the agent needed to take actions and complete tasks.

What if there is no plugin? What do we do? 

It doesn't matter. Almost every web service has an **API**: a way for programs to talk to it. Qualtrics publishes one, with documentation. If you give the agent a key to the door and tell it where the documentation is, it figures out the rest. You never see the code it writes to do so.

That's the point of this lesson: **plugins are a convenience, not a boundary.**

<a id='section2'></a>

# Your Qualtrics Token

An **API token** is a password for programs. You generate it once, and anything that has it can act as you in Qualtrics.

1. Log in to Qualtrics (Berkeley affiliates: [berkeley.qualtrics.com](https://berkeley.qualtrics.com); otherwise, the free account you created before the workshop).
2. Click your account icon (top right) → `Account Settings` → `Qualtrics IDs`.
3. Under `API`, click `Generate Token`. Copy it.
4. On the same page, note your **Datacenter ID** (something like `iad1`).

<!-- TODO(screenshot): the Qualtrics IDs page with the API token box and Datacenter ID visible.
     Save as images/qualtrics_ids.png and uncomment: -->
<!-- ![The Qualtrics IDs page: API token and Datacenter ID](../images/qualtrics_ids.png) -->

⚠️ **Warning:** If there is no `Generate Token` button, your account type doesn't have API access turned on. Pair up with someone who does for the rest of this section.

Now, where does the token go? **Not into the chat.** Anything you paste into a conversation is stored with that conversation. Instead, we put it in a file the agent can read. Start a **new conversation**:

```
Create a file called credentials.txt in this project with exactly this content:

QUALTRICS_API_TOKEN=PASTE_YOUR_TOKEN_HERE
QUALTRICS_DATACENTER=PASTE_YOUR_DATACENTER_HERE

Don't fill in the values; I'll do that myself.
```

Open `credentials.txt` in any text editor (ask the agent for the path), replace the two placeholders, and save. The `AGENTS.md` rule from lesson 1 already covers the rest: the agent reads this file when it needs to, and never prints it.

💡 **Tip:** For your own work, a password manager is nicer than a text file. 1Password (paid) can hand secrets to an agent with a fingerprint prompt each time. Free managers like Bitwarden can do similar things with more setup. A text file in a folder you control is the simplest thing that works — just don't share the folder.

<a id='section3'></a>

# Create the Survey

```
Using the Qualtrics API (credentials in credentials.txt; documentation at https://api.qualtrics.com), create a feedback survey called "Speaker Series Feedback - [TALK TITLE]" with three questions:

1. How useful was the talk? (1 to 5)
2. What was the most interesting point?
3. Who should we invite next?

Activate it, get the anonymous survey link, and add the link to the bottom of the event doc. Show me the link.
```

This is the most complex thing the agent has done today. Watch the steps: it reads the documentation, tries a request, maybe gets an error, reads more, tries again. You'll see it ask for approval to run commands. Those commands contain your token — that's why it lives in a file, not in the chat.

✅ **Expected result:** A new survey in your Qualtrics account (check in the browser), and a link in the event doc that opens it.

🔔 **Question:** Did the agent get it right the first time? If not, what did it do about it?

## 🥊 Challenge 5: Fill Out Your Neighbor's Survey

Get the survey link from the people near you — the same ones you invited — and fill out theirs. Make up answers. Be kind, or don't.

<a id='section4'></a>

# Collect Responses

```
Download all responses to the feedback survey. Summarize them: the average usefulness score, the main themes in the open answers, and every speaker suggestion. Add the summary as a new section at the bottom of the event doc.
```

✅ **Expected result:** A summary of your neighbors' responses in the event doc.

That's the full loop, without a plugin: create, distribute, collect, summarize.

⚠️ **Warning:** When you're done with the workshop, go back to `Qualtrics IDs` and generate a new token. That invalidates the old one. Do the same for any token you hand to any agent, ever, when the task is over.

<a id='section5'></a>

# Write Your Own Skill

Look at what you've done today: invite, check for replies, update a sheet, summarize a survey. Next week, you'd want to do the "check on things" part again. And the week after.

In lesson 4 you installed someone else's skill. Now write your own — by describing it.

```
Create a skill called event-status in ~/.codex/skills/event-status/SKILL.md. When I run it, it should:

1. Check my inbox for new replies mentioning "Speaker Series" since the last time it ran.
2. Update the "rsvp" column on the attendee sheet for anyone who replied.
3. Draft (don't send) a reply to anyone who asked a question.
4. Download any new feedback survey responses and append them to the summary in the event doc.
5. Report what changed, in five lines or fewer.

Include the rule that it never sends anything without my approval. Then show me the file.
```

Read `SKILL.md`. It's plain English. Change anything you'd do differently.

Now, the payoff. Everyone reply to one more invitation in your inbox — a new yes or a change of mind. Then:

```
Run the event-status skill.
```

✅ **Expected result:** A five-line report: one new reply found, one row updated, nothing sent.

🔔 **Question:** This took you one prompt to write and one word to run. What's the recurring chore in your own week that you'd write a skill for first?

💡 **Tip:** A reference version of this skill is in the workshop materials at `skills/event-status/SKILL.md`. Compare it with yours.

<a id='section6'></a>

# Where to Go From Here

Today you connected three plugins, one API, and wrote one skill. The pattern was the same every time:

1. **Give the agent context**: a template, a sheet, a rules file.
2. **Connect the tools** it needs: a plugin if one exists, an API key if not.
3. **Draft, review, approve** for anything that leaves your account.
4. **Verify** what it did.
5. **Write it down as a skill** once you'd do it again.

## 🥊 Take-Home: Your Own Recurring Task

Pick one recurring chore in your own work — literature alerts, weekly status emails, collecting forms, scheduling office hours. Sketch it as the five steps above. What would the context be? Which tools? Where does the draft-and-approve step go? Then, at home, try building it.

## More Plugins

The Codex plugin marketplace ([platform.openai.com/codex/plugins](https://platform.openai.com/codex/plugins)) has many more connections: Slack, Notion, Microsoft Outlook and Teams, GitHub, and dozens of others. Everything you learned today — rules, permissions, draft-first, verify — applies to every one of them.

- Bring your own workflow to [D-Lab consulting](https://dlab.berkeley.edu/consulting).
- For agents and research data, see [Agentic AI for Research Workflows](https://github.com/dlab-berkeley/Agentic-AI-Research-Workflows).

# Key Points

- No plugin is not a blocker. An API token and a link to the documentation are enough.
- Credentials go in a file the agent can read, never into the chat. Revoke them when you're done.
- An agent can run a full survey loop: create, link, collect, summarize.
- A **skill** you write yourself turns today's prompts into one reusable command.
- The pattern transfers: context, tools, draft-and-approve, verify, write it down.
