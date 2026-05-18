# Xiangyuan (Shawn) Mo — Personal Academic Website

**Live at:** https://xiangyuan-mo.github.io

---

## File Structure

```
xiangyuan-mo.github.io/
├── index.html          ← Home page (About, News, Contact)
├── research.html       ← Research papers and projects
├── cv.html             ← Full CV in text form
├── assets/
│   ├── style.css       ← All styles (colors, fonts, layout)
│   └── photo.jpg       ← Profile photo (left panel)
└── README.md           ← This file
```

There is **no Jekyll** — this is pure static HTML. Everything works directly in any browser.

---

## How to Edit Each Part

### Change your photo
Replace `assets/photo.jpg` with a new file. Keep the filename the same, or update the `src="assets/photo.jpg"` in **all three HTML files** (index, research, cv).

### Edit the About Me text (Home page)
Open `index.html`. Find the `<section>` under `<h2>About Me</h2>` and edit the `<p>` paragraphs.

### Add a news item
Open `index.html`. Find `<h2>News</h2>`. Copy one of these blocks and paste it in:
```html
<div class="news-item">
  <span class="news-date">Mon YYYY</span>
  <span>Your news text here.</span>
</div>
```

### Add a research paper
Open `research.html`. Copy this template into the relevant `<section>`:
```html
<div class="paper">
  <div class="paper-title">Paper Title Here</div>
  <div class="paper-meta">
    with Co-Author (Institution) · <em>Working Paper</em>, 2026
  </div>
  <div class="paper-abstract">
    Abstract text here.
  </div>
  <div class="paper-links">
    <a href="URL" target="_blank">PDF</a>
    <a href="URL" target="_blank">GitHub</a>
  </div>
</div>
```

### Add a CV entry
Open `cv.html`. Copy this template into the relevant `<section>`:
```html
<div class="cv-item">
  <div class="cv-header">
    <span class="cv-place">Organization Name — Your Role</span>
    <span class="cv-date">Month YYYY – Month YYYY</span>
  </div>
  <div class="cv-role">Department / Location</div>
  <ul class="cv-list">
    <li>Bullet point one</li>
    <li>Bullet point two</li>
  </ul>
</div>
```

### Add a new page (e.g., teaching.html)
1. Copy `cv.html` as a starting point, rename it `teaching.html`
2. Update the page `<title>` tag
3. In the `<nav class="topnav">` block, add a link:
   ```html
   <a href="teaching.html">Teaching</a>
   ```
4. Add the same link to the nav bar in **all other HTML files** too (index, research, cv)

### Change colors or fonts
Open `assets/style.css`. At the very top, edit the `:root` block:
```css
:root {
  --navy:       #1a2744;   /* sidebar/heading color */
  --gold:       #b8962e;   /* accent color */
  --cream:      #faf8f4;   /* page background */
  --photo-w:    280px;     /* width of the left photo panel */
}
```
Font choices are loaded from Google Fonts. To change them, edit the `@import` line at the top of `style.css` and update `font-family` references.

---

## Local Preview

No build step needed — just open the HTML files in a browser:

```bash
# Option 1: simplest (double-click index.html in Finder/Explorer)
open index.html

# Option 2: local server (avoids any CORS quirks)
python3 -m http.server 8000
# Then open http://localhost:8000 in your browser

# Option 3: VS Code Live Server extension
# Install "Live Server" → right-click index.html → Open with Live Server
```

---

## Deploying Updates to GitHub Pages

After editing files locally:

```bash
git add .
git commit -m "update research page"
git push origin main
```

Changes go live at https://xiangyuan-mo.github.io within ~1 minute.

To edit directly on GitHub (no local setup needed): go to the file on GitHub → click the pencil icon → edit → click **Commit changes**.
