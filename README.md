# FreeQuiz

Study your flashcard sets for free. Export a set from your flashcard site as a PDF, drop it into FreeQuiz, and study it with Learn mode, flashcards, or quizzes.

- **Learn:** adaptive rounds of 7 cards. New cards start as multiple choice, come back as typed questions once you get them right, and count as mastered when you type them correctly. Missed cards repeat later in the same round.
- **Flashcards:** flip cards, mark each one "Got it" or "Still learning", shuffle, and choose which side shows first.
- **Quiz:** multiple choice, typed answers, or a mix. Typed answers forgive missing accents and small typos, and you can retry the cards you missed.
- **Private:** the PDF is read in your browser. Nothing is uploaded, and there is no account or server.
- **Text import:** paste cards as `term<TAB>definition` lines if you don't have a PDF.

Your decks and progress are saved in your browser's local storage, so they stay on the device and browser you used.

## Use it online

Open the hosted version: **https://renukabhu.github.io/FreeQuiz/**

## Run it yourself

FreeQuiz is a single static page with no build step.

**Quickest:** download or clone this repo and open `index.html` in your browser.

```sh
git clone https://github.com/renukabhu/FreeQuiz.git
cd FreeQuiz
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows
```

**With a local web server** (recommended if your browser blocks local storage for files opened directly):

```sh
cd FreeQuiz
python3 -m http.server 8000
# then visit http://localhost:8000
```

An internet connection is needed the first time so the page can load the PDF reader ([pdf.js](https://mozilla.github.io/pdf.js/)) and fonts from public CDNs.

## Host your own copy

1. Fork this repo.
2. In your fork, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch", pick `main` and `/ (root)`, and save.
4. After a minute your copy is live at `https://<your-username>.github.io/FreeQuiz/`.

Any static host works too (Netlify, Cloudflare Pages, Vercel): upload the files as they are.

## Which PDFs work

FreeQuiz expects the standard flashcard-set PDF export: a numbered list with the term in the left column and the definition in the right column (`1.  la boca    mouth`). Terms and definitions that wrap onto several lines are joined back together. If a PDF can't be read, paste the cards as text instead.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole app: layout, styles, PDF reader, flashcards, and quiz. |
| `sample-deck.js` | The example deck shown on first visit. Delete it, and its `<script>` tag in `index.html`, to start with no decks. |

FreeQuiz is not affiliated with any flashcard website.
