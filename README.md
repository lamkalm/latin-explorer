# Latin Explorer

**Live site:** https://ohiomathteacher.github.io/latin-explorer/

Interactive apps for learning Latin as a living, spoken language — built for an independent study project at Miami University. No frameworks, no build step, no login. Just HTML files that open in a browser.

---

## What's here

| App | Status | Description |
|---|---|---|
| [Speak Latin](pronunciation.html) | ✅ Live | Hear Caesar, Cicero, Finnish radio, and the Vatican. Record yourself and compare. |
| Conversation Coach | Coming soon | Talk with a Latin avatar in scripted real-world dialogues. |
| Latin Roots & Derivatives | Coming soon | Explore how Latin roots became half of English. |

See [BRAINSTORM.md](BRAINSTORM.md) for the full vision and [TODO.md](TODO.md) for the project roadmap.

---

## For Lucas — Getting Started with Claude Code

This project is built using **Claude Code**, an AI coding assistant. The workflow is simple: you describe what you want in plain English, and Claude writes the code. No programming knowledge required — your job is to be the designer and educator, not the developer.

Here's everything you need to know to start building.

---

### What is Claude Code?

Claude Code is a command-line tool that lets you have a conversation with Claude about building software. You describe the experience you want — what students see, what they can click, how it should feel — and Claude writes working HTML/JavaScript and edits it based on your feedback.

Think of it like pair programming with someone who can type 500 lines a minute but needs you to make every decision about what to actually build.

---

### The Mindset Shift

The hardest thing to unlearn: **you don't need to think about code.**

You are the **product owner and educator**. Your job is to describe:
- What a student sees on screen
- What happens when they tap or click something
- What words, phrases, or Latin content appear
- How it should feel (fast? slow? playful? serious?)

Claude's job is to figure out how to build it.

---

### Starting a Project

Open Claude Code in your terminal in the project folder and start a conversation. Your first message should describe the *experience*, not the technology:

**Good first messages:**
> "I want to build an app where a student picks a Latin verb like *amare* and sees all six present-tense forms laid out on screen. When they tap a form, they hear it spoken aloud. Each form should show its English meaning."

> "Build a flashcard app for Latin greetings. One side shows the Latin phrase, the other shows the English and a phonetic pronunciation guide. The student taps to flip. There should be 10 cards and a progress counter."

> "I want a conversation simulator where a Roman marketplace vendor (named Marcus) greets the student in Latin and asks what they want to buy. The student picks from three options. Marcus responds in Latin to whatever they choose."

**Avoid starting with:**
> "Can you code a React component that..."  *(you don't need to specify technology)*
> "Write a JavaScript function that..."  *(describe the experience, not the implementation)*

---

### The Iteration Loop

Building an app is a conversation, not a single request. A typical session looks like:

1. **Describe** what you want → Claude builds a first version
2. **Open** the HTML file in your browser and try it
3. **Give feedback** in plain English → Claude revises
4. Repeat until it feels right

Feedback examples that work well:
- *"The button is too small on my phone — make it bigger and move it higher on the screen"*
- *"Add Virgil as a fourth character with these three phrases: [paste phrases]"*
- *"The pronunciation guide should appear before the Latin text, not after"*
- *"When the recording stops, automatically play it back — don't make the student click a second button"*

You can be as specific or as vague as you like. If you're vague, Claude will make a choice and you can adjust it.

---

### What Makes a Great Prompt

**Describe the user experience, not the code.**
Instead of "add a boolean variable," say "show a green checkmark after the student answers correctly."

**Give real content.**
Paste actual Latin phrases, character names, and English translations. The app is only as good as the content you put in it. Claude can suggest content too, but you know your pedagogical goals.

**Reference things you've seen.**
"Like the pronunciation page we already built, but for verbs instead of phrases" is a perfectly valid prompt. Claude can see the existing code and build on it.

**Say what you don't want.**
"No grammar jargon — don't use words like 'nominative' or 'accusative'" is useful. "Keep it playful, not academic" is useful. Constraints help.

---

### Getting Your App on the Web

Every HTML file you build goes live automatically when you push to this repo. GitHub Pages serves the whole repo as a website.

**The workflow:**
1. Claude builds or edits a file (e.g., `conversation.html`)
2. In the terminal: `git add conversation.html && git commit -m "Add conversation coach" && git push`
3. Wait ~60 seconds, then visit `https://ohiomathteacher.github.io/latin-explorer/conversation.html`

That's it. Every push updates the live site.

---

### Latin App Ideas to Explore

These are all buildable as single HTML files with no server or database:

- **Verb conjugation explorer** — pick a verb and tense, see all six forms, hear each one
- **Dialogue simulator** — a scripted back-and-forth with a Roman character in a real setting (market, school, senate)
- **Latin news reader** — short "broadcast" style clips in Latin, like Nuntii Latini; student reads along and taps unknown words for definitions
- **Pronunciation comparison** — classical vs. ecclesiastical side by side; the same phrase, two traditions
- **Phrasebook builder** — student collects phrases they've learned; personal review mode
- **Grammar through famous sentences** — *Veni, vidi, vici* teaches the perfect tense; *Amor vincit omnia* teaches word order; context before rules
- **Roman persona creator** — student picks a Roman name, tribe, and occupation; the app generates a short Latin self-introduction they can practice saying

---

### Questions to Bring to the First Meeting

Before building, it helps to have answers to:

1. **Who is the student?** True beginner, intermediate reader, advanced speaker?
2. **Classical or ecclesiastical pronunciation** — or both, contrasted?
3. **Is there a text or vocabulary list** to anchor the content to?
4. **What does "done" look like** for the semester? One polished app, or a collection of demos?
5. **What's the most important thing** a student should be able to *do* after using these tools — that they couldn't do before?

---

## Technical Notes

- Pure HTML/CSS/JavaScript — zero dependencies, zero build step
- Web Speech API for text-to-speech and (in future apps) speech recognition
- MediaRecorder API for audio capture
- Hosted on GitHub Pages — every push to `master` updates the live site
- Works on phones, tablets, and desktop browsers (Chrome and Edge recommended for best speech support)

---

*Built with [Claude Code](https://claude.ai/code) (Anthropic) · Miami University · Spring 2026*
