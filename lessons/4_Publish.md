# Agentic AI for Knowledge Work: Publish

### Learning Objectives

- Explain what a skill is and where it lives.
- Install a published skill and use it to produce a flyer.
- Recognize that an agent can work on plain files with no plugin involved.
- Describe what ChatGPT Sites does and when it's available.

### Icons Used in This Notebook
🔔 **Question**: A quick question to help you understand what's going on.<br>
🥊 **Challenge**: Interactive exercise. We'll work through these in the workshop!<br>
💡 **Tip**: How to do something a bit more efficiently or effectively.<br>
⚠️ **Warning:** Heads-up about tricky stuff or common mistakes.<br>
✅ **Expected result**: What you should see if things went right. Small differences are fine; big ones are worth investigating.<br>

### Sections
1. [What Is a Skill?](#section1)
2. [Install a Skill: The Flyer](#section2)
3. [🎬 Demo: An Event Page With Sites](#section3)

<a id='section1'></a>

# What Is a Skill?

So far, every prompt you've written started from scratch: you described the task, the format, the tone. A **skill** is a way to write that description once and reuse it.

Concretely, a skill is a folder with a file called `SKILL.md` inside. The file says what the skill is for and how to do it: steps, rules, examples. Skills live in a folder on your computer (`~/.codex/skills/`). When you give the agent a task, it reads the descriptions of the skills it has and uses one if it matches. You can also name a skill directly.

That's it. A skill is instructions in a folder. Nobody programmed anything.

People publish skills the way they publish recipes. There are collections for making Word documents, slide decks, PDFs, charts, and designs. In this lesson you install one. In lesson 5, you write your own.

🔔 **Question:** `AGENTS.md` is also instructions in a file. What's the difference between a rule in `AGENTS.md` and a skill?

<a id='section2'></a>

# Install a Skill: The Flyer

Your talk needs a flyer. An agent can make one with no skill at all — but a design skill makes it better, and installing one shows you how skills work.

Start a **new conversation**:

```
Install the canvas-design skill from https://github.com/anthropics/skills into my Codex skills folder (~/.codex/skills/). Then list the skills I have available and tell me, in one sentence, what each one does.
```

<!-- TODO(pre-flight): confirm canvas-design produces a usable one-page flyer with the current
     Codex app. Fallback: the pptx skill from the same repo (one slide, exported to PDF). -->

✅ **Expected result:** The agent downloads the skill, and reports it in the list. Open `~/.codex/skills/canvas-design/SKILL.md` in any text editor — ask the agent for the path if you can't find it. Read the first twenty lines. That's the whole trick.

Now use it:

```
Using the canvas-design skill, make a one-page flyer for the talk in the event doc. Include the title, speaker, date, time, location, and a one-sentence hook from the abstract. Save it as flyer.pdf in this project folder, and put a copy in the Speaker Series folder in Drive.
```

Open `flyer.pdf`. A few volunteers will share theirs on the projector.

🔔 **Question:** Same skill, same event doc, different flyers. Where did the differences come from?

💡 **Tip:** Notice that this task never touched Gmail or Calendar. The agent read a Google Doc, then worked on a plain file on your computer. Most of what an agent does for you won't need a plugin at all.

<a id='section3'></a>

# 🎬 Demo: An Event Page With Sites

**ChatGPT Sites** builds and hosts a web page from a description. Click `Sites` in the sidebar, describe the page, and the agent builds it, shows you a preview, and publishes it at a URL when you say so.

⚠️ **Warning:** Sites requires a paid ChatGPT plan, so this part is a demo. If you're on a paid plan, follow along.

The instructor will run something like:

```
Build an event page for the talk in the event doc: title, speaker and bio, abstract, date, time, and location. Add an "RSVP" button that opens an email to me. Show me a preview before publishing.
```

Watch for the same pattern as every other task today: a draft (the preview), a review, and a deliberate "publish."

🔔 **Question:** Who would you send this page to? What would you need to change in the prompt before it was good enough for that?

# Key Points

- A **skill** is a folder with a `SKILL.md` file: reusable instructions for a kind of task.
- Skills are installed by copying a folder. The agent can do that for you.
- Agents work on plain files — PDFs, images, documents on your computer — with no plugin involved.
- Sites publishes a web page from a description, behind the same preview-then-publish pattern.
