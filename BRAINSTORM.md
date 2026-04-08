# Latin Explorer — Brainstorm

**Project leads:** Todd Edwards & Lucas Lamka, Miami University
**Context:** Independent study — Latin as a living, spoken language
**Platform:** Pure HTML/CSS/JS apps, hosted on GitHub Pages
**Development approach:** Agentic coding with Claude Code (no programming required)

---

## Core Vision

Latin is not a dead language — it is a sleeping one, and the goal of this project is to wake it up for students. The apps we build should make Latin feel *immediate*, *speakable*, and *alive* rather than ancient, dusty, or purely grammatical.

**The guiding question:** What would Duolingo look like if it was designed by a Latin teacher who actually cared about speaking the language?

---

## The Coaching Arc (Full Architecture)

The full system would work in three phases, each building on the last:

```
Phase 1 — Word Lab
  Hear a word from a character → see phonetic guide → record yourself → compare

Phase 2 — Phrase Builder
  Same words assembled into phrases → hear → record → compare

Phase 3 — Conversation with the Avatar
  A Latin "talking head" greets you in Latin, uses the words you've drilled,
  waits for your response → scripted branching dialogue
```

Each phase feeds the next. Words practiced in Phase 1 appear in Phase 2 phrases, which appear in Phase 3 conversations. The system builds communicative competence progressively.

---

## The "Ancient & Modern" Framework

**The killer insight:** showing that Latin is still spoken today — not just studied — makes the most powerful argument for it as a living language.

The app would have two wings of characters:

### The Ancients
Real historical figures, famous phrases, classical pronunciation.

| Character | Dates | Why them |
|---|---|---|
| Julius Caesar | 100–44 BCE | Most famous Latin, military genius, wrote his own commentaries |
| Cicero | 106–43 BCE | Rome's greatest orator; crafted Latin as sound as much as meaning |
| Virgil | 70–19 BCE | The Aeneid — Latin's national epic; *Arma virumque cano* |
| Augustus | 63 BCE–14 CE | First emperor; *Festina lente* — speed and care together |
| Seneca | 4 BCE–65 CE | Stoic philosopher; letters on living well are startlingly modern |
| Ovid | 43 BCE–17 CE | Love poetry; made Latin playful and accessible |

### The Moderns (Latin Right Now)
Contemporary or near-contemporary figures showing Latin as a living institution.

| Character | Context | Why them |
|---|---|---|
| **Nuntii Latini** (Finnish Radio) | 1989–2019 | Weekly Latin news broadcast — real journalists speaking Latin about modern events |
| **The Vatican** | 27 BCE–present | Latin is still the official language of the Holy See; every papal document |
| **Reginald Foster** | d. 2020 | "The Pope's Latinist" — legendary for teaching Latin as a spoken language; held outdoor classes in Rome in jeans, just talking |
| **Paideia Institute** | Present | Runs immersion Latin programs in Rome; students converse entirely in Latin |
| **A modern student** | Present | Fictional peer character — someone Lucas's students could identify with |

**The contrast is the lesson:** a Roman general and a Finnish radio host use the *same language*. 2,000 years apart. Still mutually intelligible.

---

## App Ideas

### 1. Pronunciation Trainer — "Speak with the Ancients" *(Demo app)*
- Character selector (ancient + modern)
- Animated SVG talking head (mouth moves during TTS)
- Vocabulary word → phonetic guide → hear it → record yourself → play back
- Progression: single word → short phrase → famous sentence
- Pronunciation rules reference panel

### 2. Conversation Coach — "Say It to Caesar"
- Scripted dialogue with a character avatar
- Character speaks in Latin (TTS), student responds
- Speech recognition checks for key vocabulary
- Branching responses based on what student says
- Multiple scenarios: greetings, market, school, forum

### 3. Vocabulary Builder — "Latin Lives"
- Words presented in context (images + sentences), not isolation
- Same word shown in classical Latin AND a modern usage
- Etymology connections: Latin word → English descendants
- Spaced repetition cycling words back

### 4. Latin News Reader — "Nuntii Vivi" (The Living News)
- Short "broadcast" style clips (TTS) reading Latin sentences about modern topics
- Student reads along, highlights unknown words
- Vocabulary pop-up on click
- Based on the Nuntii Latini model

### 5. Phrase Collector — "My Phrasebook"
- Student builds a personal phrasebook session by session
- Practice mode: hear phrase, try to recall it before seeing
- Can share phrasebook as a link

### 6. Grammar through Use — "Why Did Caesar Say That?"
- Grammar explained through famous sentences, not abstract rules
- *Veni, vidi, vici* → what is the perfect tense and why does it matter here?
- No paradigm tables. Context first, pattern second.

---

## Technical Possibilities

**What pure HTML/JS can do (no server needed):**
- Text-to-speech (Web Speech API) — works on Chrome, Edge, Safari
- Speech recognition (Web Speech API) — keyword detection, Chrome best
- Audio recording & playback (MediaRecorder API)
- Animated SVG avatars (mouth animation synced to TTS)
- Local session storage (save progress within a visit)
- Shareable state via URL parameters

**What would need a backend or API:**
- AI-powered open conversation (Claude API)
- Persistent user accounts / progress saving
- Real pronunciation scoring (phoneme analysis)
- Generated content (custom vocabulary lists)

**The Claude API possibility:** A future version of the conversation coach could use the Claude API to power genuinely open-ended Latin dialogue — the student types or speaks anything, and the character responds in Latin. This would be a significant leap in capability.

---

## Pedagogical Principles

1. **Speaking over parsing** — Every app prioritizes production (saying things) over analysis (identifying forms). Students speak first; grammar emerges from use.

2. **Context before rules** — Present Latin in meaningful situations before explaining the rules behind it. *Veni, vidi, vici* before the perfect tense.

3. **Ancient AND modern** — Constantly connect classical Latin to contemporary usage. Shatters the "dead language" myth at every turn.

4. **Low stakes, high repetition** — Recording yourself and playing back is private, not graded. Students will try more when they're not performing for evaluation.

5. **Characters, not textbooks** — Every interaction is mediated through a person with a story. Caesar's one-liner means more when you know he was writing home after a three-hour battle.

---

## Pronunciation Notes (Classical vs. Ecclesiastical)

This is a real decision to make: which Latin pronunciation does the app teach?

| Feature | Classical (Republican/Imperial) | Ecclesiastical (Church) |
|---|---|---|
| V | W sound (*veni* = "WAY-nee") | V sound (*veni* = "VEE-nee") |
| C before e/i | K (*Cicero* = "KEE-kay-roh") | Ch (*Cicero* = "CHEE-chay-roh") |
| AE | "eye" sound | "ay" sound |
| G before e/i | Hard G | Soft G (like J) |

**Recommendation:** Teach both, label them clearly. The Vatican character naturally demonstrates ecclesiastical; Caesar demonstrates classical. The contrast is itself educational.

---

## Questions to Resolve (For Tonight's Meeting)

1. What is Lucas's primary use case — his own learning, or building tools for his future students?
2. Which phase of the coaching arc is most valuable to build first?
3. What level of Latin should the app target — true beginners, intermediate readers, or advanced speakers?
4. Should we use classical or ecclesiastical pronunciation (or both)?
5. Who are the most compelling modern Latin figures to include?
6. Is there a specific text, textbook, or vocabulary list we should anchor to?
7. What would a "finished" semester project look like — a single polished app, or a collection of demos?
