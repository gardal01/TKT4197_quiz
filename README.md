# TKT4197 Study Lab — mobile quiz website

A mobile-first, no-account study app for **TKT4197 Nonlinear Finite Element Analysis**, based on the original **347-card Anki deck** generated from the uploaded lecture notes, exercises and 2019–2025 exams.

## Features

- All 347 questions, split into 13 course topic collections
- **Multiple choice:** four answer options, instant correctness feedback, original explanation and sources
- **Mixed:** 80% multiple-choice and 20% self-graded recall
- **Recall:** reveal full answer then mark whether you knew it
- 5/10/20/all question sessions; smart mix, unseen, missed, and due reviews
- Progress saved in *this browser* using localStorage; export/import JSON backup
- Installable to phone home screen after GitHub Pages hosting; app shell can work offline after installation
- No build tools, server, app account, or data submission needed

**Quality note:** 163 questions have individually curated multiple-choice alternatives. The other 184 have automated distractors chosen from different answers in the same topic. For exam preparation, focus on explaining why an answer is correct rather than using MC recognition alone. Original question, explanation, and source are retained for all 347 questions.

## Publish free on GitHub Pages (recommended for iPhone / Android)

1. Create a free account at <https://github.com> if you do not have one.
2. Create a new **public** repository, for example named `tkt4197-quiz`.
3. **Extract the ZIP file** provided with this package on your computer.
4. On your new repository, choose **Add file → Upload files**, and upload the *contents* of the extracted folder, not the folder itself and not the ZIP. You should see `index.html` at the top level, alongside `app.js`, `questions.js`, `styles.css`, and the icons. Commit the upload to the `main` branch.
5. Open repository **Settings → Pages → Build and deployment**. Choose **Source: Deploy from a branch**, **Branch: main**, **Folder: /(root)**. Select **Save**.
6. Once GitHub reports the site has been published, use **Settings → Pages → Visit site**. It will typically be at `https://YOUR-USERNAME.github.io/tkt4197-quiz/`.
7. Open that URL on your phone. On **iPhone**: Safari → Share → **Add to Home Screen**. On **Android**: Chrome → menu → **Add to Home screen / Install app**.

Publishing documentation: <https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site>

## Preview on your computer

Double-click `index.html`. The question data is in `questions.js`, so the app can run directly from local files in a desktop browser. A separate `TKT4197_Quiz_Standalone.html` is also supplied; it packs the CSS and question data into a single file. For the best phone experience, publish the website via HTTPS rather than relying on the phone's local file preview.

## Data privacy and device limits

- No login or analytics; no answers or progress are uploaded.
- Browser progress is **not synchronized** between PC and phone or between different browsers on the same phone.
- Use **Export backup** and **Import backup** to move or preserve progress.
- Resetting browser site data or using private/incognito mode may lose progress.
- Math formulas are rendered by MathJax when an internet connection is available. If the rendering script is unavailable offline, the questions and original math source remain readable as LaTeX text.

## Files

- `index.html` — main page
- `styles.css` — responsive design
- `app.js` — quiz, review, local progress, backup
- `questions.js` — all 347 questions, answer options, sources
- `manifest.webmanifest`, `sw.js`, `icon-*.png` — home-screen app support and offline app shell
- `.nojekyll` — tells GitHub Pages to publish static files without Jekyll processing

Original Anki deck and original PDFs remain separate. This site is an unofficial independent study tool, not an NTNU-hosted site.
