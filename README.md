# WollyTech Portfolio Site

A Jekyll-based portfolio website for game designer and developer Olawole Abayomi-Owodunni, hosted on GitHub Pages.

## 🚀 Quick Start

This site is automatically deployed to GitHub Pages from the `main` branch. Any changes pushed to `main` will be live within a few minutes.

**Live Site:** https://WollyTech.github.io

## 📁 Project Structure

```
WollyTech.github.io/
├── _config.yml              # Jekyll configuration
├── _layouts/                # Page templates
│   ├── default.html         # Main layout with header/footer
│   └── project.html         # Project detail page layout
├── _includes/               # Reusable components
│   ├── nav.html             # Navigation bar
│   └── footer.html          # Footer
├── _data/                   # Data files
│   └── projects.yml         # Project metadata (edit this!)
├── assets/
│   ├── css/
│   │   └── style.css        # Main stylesheet
│   ├── img/                 # Images
│   │   ├── operation-reclaim/
│   │   ├── experiment-vessel/
│   │   ├── wisteria/
│   │   ├── olis-cofferia/
│   │   └── coming-soon.png
│   └── pdfs/
│       └── resume.pdf       # Your resume (add this!)
├── projects/                # Project detail pages
│   ├── operation-reclaim.md
│   ├── experiment-vessel.md
│   ├── wisteria.md
│   ├── olis-cofferia.md
│   └── coming-soon.md
├── index.md                 # Home page
├── projects.md              # Projects listing page
├── resume.md                # Resume page
└── retrospective.md         # Retrospective page
```

## ✏️ How to Edit Content

### Adding a New Project

**Step 1: Add project metadata to `_data/projects.yml`**

```yaml
published:  # or 'school' or 'personal'
  - title: "Your Project Name"
    slug: "your-project-name"  # URL-friendly version
    description: "Brief description"
    youtube_id: "VIDEO_ID_HERE"  # or null if no video
    thumbnail: "/assets/img/your-project-name/thumbnail.png"
    category: "Published"  # or "School" or "Personal"
    coming_soon: false  # optional, set to true for placeholders
```

**Step 2: Create a project detail page in `projects/`**

Create `projects/your-project-name.md`:

```markdown
---
layout: project
title: "Your Project Name"
description: "Brief description"
youtube_id: "VIDEO_ID_HERE"  # optional
permalink: /projects/your-project-name/
hero_image: /assets/img/your-project-name/hero.png  # optional
roles:
  - Role 1
  - Role 2
  - Role 3
gallery:
  - url: /assets/img/your-project-name/screenshot1.png
    caption: "Description"
  - url: /assets/img/your-project-name/screenshot2.png
    caption: "Description"
---

## Overview

Write your project description here...

### Key Features

- Feature 1
- Feature 2

### Design Process

Describe your design process...
```

**Step 3: Add images**

Create a folder `assets/img/your-project-name/` and add:
- `thumbnail.png` (for project cards, recommended: 600x400px)
- `hero.png` (optional banner image, recommended: 1200x400px)
- `screenshot1.png`, `screenshot2.png`, etc. (gallery images)

### Updating Existing Pages

- **Home page:** Edit `index.md`
- **Projects listing:** Edit `projects.md` (or just update `_data/projects.yml`)
- **Resume:** Edit `resume.md` and replace `assets/pdfs/resume.pdf`
- **Retrospective:** Edit `retrospective.md`

### Editing Project Details

Edit the respective markdown file in `projects/` folder. You can update:
- Title and description
- YouTube video ID
- Roles and responsibilities
- Gallery images
- Main content

### Converting YouTube Links to IDs

From: `https://youtu.be/wuDB4yGGVdI` or `https://www.youtube.com/watch?v=wuDB4yGGVdI`  
Extract: `wuDB4yGGVdI`  
Use in YAML: `youtube_id: "wuDB4yGGVdI"`

## 🎨 Customizing Styles

Edit `assets/css/style.css` to change:
- Colors (see CSS variables at the top)
- Fonts
- Spacing
- Layout

Key CSS variables:
```css
--color-bg-main: #2a2a2a;        /* Main background */
--color-bg-dark: #1e1e1e;        /* Header/footer */
--color-bg-panel: #242424;       /* Content panels */
--color-accent: #4a9eff;         /* Accent color */
--color-text-primary: #e0e0e0;   /* Main text */
--color-text-secondary: #b0b0b0; /* Secondary text */
```

## 🖼️ Image Guidelines

**Recommended image sizes:**
- **Thumbnails:** 600x400px (3:2 aspect ratio)
- **Hero images:** 1200x400px (3:1 aspect ratio)
- **Gallery images:** 800x600px or larger
- **Coming soon placeholder:** 600x400px

**Format:** JPG or PNG (use JPG for photos, PNG for graphics with transparency)

## 🧪 Testing Locally (Optional)

To preview your site locally before pushing to GitHub:

1. **Install Ruby** (if not already installed)
   - Windows: https://rubyinstaller.org/
   - Mac: Ruby comes pre-installed
   - Linux: `sudo apt-get install ruby-full`

2. **Install Jekyll and dependencies:**
   ```bash
   gem install bundler
   bundle install
   ```

3. **Run the local server:**
   ```bash
   bundle exec jekyll serve
   ```

4. **View in browser:** http://localhost:4000

## 🚢 Deployment

Deployment is automatic! Just push to the `main` branch:

```bash
git add .
git commit -m "Update project details"
git push origin main
```

GitHub Pages will build and deploy your site within 1-2 minutes.

## 📝 Common Tasks

### Update Your Resume
1. Replace `assets/pdfs/resume.pdf` with your new PDF
2. Update text in `resume.md` if needed
3. Commit and push

### Add Gallery Images to Existing Project
1. Add images to `assets/img/project-name/`
2. Edit `projects/project-name.md`
3. Add image URLs to the `gallery` array in the front matter
4. Commit and push

### Change Navigation Links
Edit `_includes/nav.html` to add/remove/modify nav links

### Update Footer
Edit `_includes/footer.html`

### Change Site Title/Description
Edit `_config.yml`

## 🐛 Troubleshooting

**Site not updating after push?**
- Wait 2-3 minutes for GitHub Pages to rebuild
- Check repository Settings → Pages to ensure it's enabled
- Check Actions tab for build errors

**Images not showing?**
- Verify image paths start with `/assets/img/`
- Check image file names match exactly (case-sensitive)
- Ensure images are committed and pushed

**Layout broken?**
- Check for YAML syntax errors in front matter
- Ensure all required fields are present
- Validate markdown syntax

## 📚 Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)
- [YAML Syntax](https://yaml.org/spec/1.2/spec.html)

## 🎯 Future Enhancements

Consider adding:
- Blog functionality for retrospectives
- Search functionality
- Dark/light theme toggle
- Contact form
- Analytics (Google Analytics or similar)
- RSS feed for updates

## 📄 License

This portfolio site structure is available for personal use. Replace all content with your own work.

---

**Need help?** Check the [Jekyll documentation](https://jekyllrb.com/docs/) or reach out to the GitHub community.
