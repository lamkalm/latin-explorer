# Latin Explorer

Live site: https://lamkalm.github.io/latin-explorer/
GitHub repo: https://github.com/lamkalm/latin-explorer

Interactive Latin learning tools built as standalone HTML pages (no framework, no build step, no backend).

## Public overview (short)

Latin Explorer is a browser-first set of classroom tools for learning Latin through roots, text study, and short writing.

Use these pages:

1. [Vocabulary Roots](roots.html)
2. [Georgics I Close Reader](georgics-reader.html)
3. [Graffiti Wall](graffiti.html)

Everything runs as static HTML/CSS/JS and is served on GitHub Pages.

## Collaborator guide (detailed)

### Current live experience

The homepage currently links these tools:

1. [Vocabulary Roots](roots.html)
2. [Georgics I Close Reader](georgics-reader.html)
3. [Graffiti Wall](graffiti.html)

## Page overview

### [index.html](index.html)

- Landing page for Latin Explorer.
- Links to the three active tools listed above.
- Includes small thumbnail previews and Wikipedia-image loading for visual cards.

### [roots.html](roots.html)

- Topic-based Latin roots explorer (currently Colors, Weather, Emotions).
- Click-to-reveal root cards with meanings and English derivatives.
- Students can add and remove derivative chips on each card.
- Topic selection is persisted in browser localStorage.
- Includes reveal reset and topic switching aligned with the graffiti prompt themes.

### [georgics-reader.html](georgics-reader.html)

- Bilingual/interlinear close reader for Virgil, *Georgics* 1.1-42.
- Latin view with inline annotations and note tagging.
- Interlinear mode for student-entered translations.
- Margin notes with local auto-save, plus JSON export/import.
- Optional AI assistant settings with provider/key saved only in localStorage.
- Built-in note filters by type and line to support classroom review.

### [graffiti.html](graffiti.html)

- Topic-based class wall for short Latin posts and replies.
- Prompts rotate by topic and align with roots topics.
- Posts and replies are stored locally in the browser.
- Includes one-time migration from older single-topic storage.

### How to work on this project

1. Edit the HTML file directly.
2. Open it in a browser for testing.
3. Commit and push to update GitHub Pages.

**Deploying changes:**
```
git add .
git commit -m "your message"
git push
```
GitHub Pages will update at https://lamkalm.github.io/latin-explorer/ within ~60 seconds.

### Data and persistence model

- No server database is used.
- Student-entered content is stored in each user's browser via localStorage.
- JSON export/import exists for Georgics notes (and interlinear translation download).
- Content is device/browser-local unless manually exported and shared.

## Other files in this repo

- [pronunciation.html](pronunciation.html) and [virgil.html](virgil.html) are present in the repository but are not linked from the current homepage.
- [BRAINSTORM.md](BRAINSTORM.md) contains longer-term ideas.
- [TODO.md](TODO.md) contains active project notes.

## Technical notes

- Pure HTML, CSS, and JavaScript.
- No npm packages or build tooling required.
- Designed to run directly in the browser and on GitHub Pages.
- Best tested in modern Chrome/Edge for browser API compatibility.
