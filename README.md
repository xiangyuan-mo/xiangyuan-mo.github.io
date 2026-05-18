# Xiangyuan (Shawn) Mo — Personal Academic Website

Live at: [https://xiangyuan-mo.github.io](https://xiangyuan-mo.github.io)

## Structure

- `index.html` — Home page (about, news, contact)
- `research.html` — Research papers and projects
- `assets/style.css` — All styles (fonts, colors, layout)
- `assets/photo.jpg` — Profile photo
- `assets/CV_Xiangyuan_Mo.pdf` — CV (update by replacing this file)
- `_includes/config.html` — Sidebar navigation
- `_config.yml` — Jekyll config (do not modify)

## Updating

**To update your CV**: Replace `assets/CV_Xiangyuan_Mo.pdf` with a new version (keep the same filename).

**To add a paper**: Copy a `<div class="paper">...</div>` block in `research.html`.

**To change colors/fonts**: Edit the CSS variables at the top of `assets/style.css`.

**To add a new page**: Create `newpage.html` following the same template, then add a nav link in `_includes/config.html`.

## Local Preview

```bash
gem install bundler jekyll
bundle init
bundle add jekyll
bundle exec jekyll serve
# → http://localhost:4000
```
