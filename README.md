# AP CSP class site

A simple static site for GitHub Pages. No build step: just HTML files.

```
index.html                      class home page
lessons/analog-to-digital.html  "From wave to bits" lesson
lessons/lossless-compression.html  "Shrinking files" lesson
translator.html                 Python ⇄ AP pseudocode translator
```

## Put it online

1. On GitHub, create a new public repository (for example `apcsp`).
2. Click **Add file → Upload files** and drag in everything in this folder (keep the `lessons` folder intact). Commit.
3. Go to **Settings → Pages**. Under "Build and deployment," choose **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
4. After a minute or two the site is live at `https://physicsmroliva.github.io/apcsp/`.

## Add a lesson or tool later

1. Upload the new page (for example into `lessons/`).
2. Add one entry to `RESOURCES` in `index.html`:

```js
{
  idea: 4, kind: "Lesson",
  title: "How the internet routes packets",
  href: "lessons/packets.html",
  desc: "One sentence about what students do."
},
```

Add `quick: true` to also feature it in the boxes at the top of the page.

## Notes on the analog-to-digital lesson

- Student work is saved in their browser on that device, so they should finish on the same computer.
- "Download PDF" saves a file directly on GitHub Pages. "Print or save as PDF" is the backup.
- The page loads its fonts and PDF library from Google Fonts and cdnjs, so school filters must allow those.
