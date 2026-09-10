# D-Lab Agentic AI for Knowledge Work Workshop

[![Open Slides](https://img.shields.io/badge/open-slides%20-purple)](https://dlab-berkeley.github.io/Agentic-AI-Knowledge-Work/slides/)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

This repository contains the materials for D-Lab's Agentic AI for Knowledge Work workshop.

In two hours, you'll hand the everyday work of organizing an event to an AI agent — writing the event doc, inviting the speaker, finding a time, emailing attendees, making a flyer, running a feedback survey — and learn where to keep a hand on the wheel. No code is written or read.

## Prerequisites

No programming experience is required. If you've used ChatGPT or a similar chatbot before, you have all the background you need.

Check out D-Lab's [Workshop Catalog](https://dlab-berkeley.github.io/dlab-workshops/) to browse all workshops, see what's running now, and review prerequisites.

## Workshop Goals

AI agents can now do real knowledge work: read your inbox, write to your Drive, manage your calendar, and talk to services like Qualtrics through their APIs. That power comes with a catch: you are handing over access to your accounts, and every detail you don't specify, the agent decides for you.

In this workshop, we organize one event — a talk in the D-Lab Speaker Series — end to end, as a series of small tasks. Each task hands the agent a little more autonomy: first it drafts, then it sends, then it publishes, and finally it runs on its own as a reusable skill. Along the way we practice the habits that make agent-assisted work trustworthy: reading what access you grant, drafting before sending, verifying what was done, and writing rules the agent follows.

## Learning Objectives

After this workshop, you will be able to:

- Explain what an agent is, how it differs from a chatbot, and when to use which.
- Connect an agent to Gmail, Google Calendar, and Google Drive, and explain what access that grants.
- Set up written rules (`AGENTS.md`) and permission settings so the agent drafts before it sends.
- Delegate document, spreadsheet, calendar, and email tasks to an agent and verify the results.
- Connect an agent to a service with no plugin (Qualtrics) using an API token stored safely.
- Install a published skill, and write your own to turn a recurring task into one command.
- Decide how much autonomy a task needs, and when more compute is worth it.

This workshop does not cover:

- Programming. The agent writes any code it needs; we never look at it.
- Agents for data analysis and research pipelines. See D-Lab's [Agentic AI for Research Workflows](https://github.com/dlab-berkeley/Agentic-AI-Research-Workflows) workshop.

## Installation Instructions

We use the **Codex app** (OpenAI's agent, bundled with the ChatGPT app). A free account is enough for the workshop. Before the session:

1. Download and install the [Codex/ChatGPT app](https://chatgpt.com/codex) (macOS or Windows), and sign in with an OpenAI account (create a free one if needed).
2. Download these workshop materials:
    - Click the green `Code` button in the top right of this page.
    - Click `Download ZIP`.
    - Extract the folder to your Desktop.
3. Decide which **Google account** you'll connect to the agent. If you'd rather not connect your everyday account to an AI product, [create a fresh Gmail account](https://accounts.google.com/signup) now — Google may ask for phone verification, which is easier to do at home than in the workshop.
4. Make sure you can log in to **Qualtrics**: Berkeley affiliates at [berkeley.qualtrics.com](https://berkeley.qualtrics.com); everyone else can [create a free account](https://www.qualtrics.com/free-account/).

## How the Workshop Runs

The workshop is hands-on: you follow along on your own machine, working in the Codex app.

Several steps involve other participants: you invite each other, reply to each other's invitations, and fill out each other's surveys. In person, that means the people near you. On Zoom, the chat is the room: post there, and pick from what others posted.

First, open this [slide deck](https://dlab-berkeley.github.io/Agentic-AI-Knowledge-Work/slides/).

The [lessons](lessons/) folder has the rest of the workshop materials. Keep them open in a browser tab and copy-paste the prompts as we go:

1. [Introduction and Setup](lessons/1_Introduction_and_Setup.md)
2. [Plan the Talk](lessons/2_Plan_a_Talk.md)
3. [Invite the Attendees](lessons/3_Invite_the_Attendees.md)
4. [Publish Your Event](lessons/4_Publish_Your_Event.md)
5. [Beyond Plugins, and Automation](lessons/5_Beyond_Plugins_and_Automation.md)

The [packet](packet/) folder holds the starter materials the lessons use: an event template, an attendee list, a set of simulated replies, a rules file, and calendar commitments and preferences. The [skills](skills/) folder has a reference version of the skill you write in lesson 5.

# Additional Resources

- [Codex plugins](https://platform.openai.com/codex/plugins) — the marketplace of one-click connections (Gmail, Drive, Slack, Notion, and more).
- [AGENTS.md](https://agents.md/) — the convention for giving agents project rules.
- [Qualtrics API documentation](https://api.qualtrics.com/) — what the agent reads in lesson 5.
- [Google account permissions](https://myaccount.google.com/permissions) — where to review and revoke the access you grant today.

# About the UC Berkeley D-Lab

D-Lab works with Berkeley faculty, research staff, and students to advance data-intensive social science and humanities research. Our goal at D-Lab is to provide practical training, staff support, resources, and space to enable you to use data science in your own research applications. Our services cater to all skill levels and no programming, statistical, or computer science backgrounds are necessary. We offer these services in the form of workshops, one-to-one consulting, and working groups that cover a variety of research topics, digital tools, and programming languages.

Visit the [D-Lab homepage](https://dlab.berkeley.edu/) to learn more about us. You can view our [calendar](https://dlab.berkeley.edu/events/calendar) for upcoming events, learn about how to utilize our [consulting](https://dlab.berkeley.edu/consulting) and [data](https://dlab.berkeley.edu/data) services, and check out upcoming [workshops](https://dlab.berkeley.edu/events/workshops).

# Other D-Lab Workshops

Interested in the tools behind today's workshop?

- [Agentic AI for Research Workflows](https://github.com/dlab-berkeley/Agentic-AI-Research-Workflows)
- [GPT Fundamentals](https://github.com/dlab-berkeley/GPT-Fundamentals)
- [Python Fundamentals](https://github.com/dlab-berkeley/Python-Fundamentals)

# Contributors

- [Pratik Sachdeva](https://dlab.berkeley.edu/people/pratik-sachdeva)
- Tom van Nuenen
- AI Agents: Codex and Claude Code
