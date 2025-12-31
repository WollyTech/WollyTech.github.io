# Quick Reference Guide

## 🎯 Next Steps

### 1. Add Your Images
- [ ] Add project thumbnails (600x400px) to each project folder in `assets/img/`
- [ ] Add gallery screenshots (800x600px+) to project folders
- [ ] Create a `coming-soon.jpg` (600x400px) in `assets/img/`
- [ ] Add your `resume.pdf` to `assets/pdfs/`

### 2. Customize Content
- [ ] Update `index.md` with your personal bio and skills
- [ ] Edit project descriptions in `projects/*.md` files
- [ ] Update `resume.md` with your experience and education
- [ ] Customize colors in `assets/css/style.css` (optional)

### 3. Test Locally (Optional)
```bash
bundle install
bundle exec jekyll serve
# Visit http://localhost:4000
```

### 4. Deploy
```bash
git add .
git commit -m "Initial portfolio setup"
git push origin main
# Site will be live at https://WollyTech.github.io in 1-2 minutes
```

---

## 📝 Common Edits

### Add a new project
1. Edit `_data/projects.yml` - add entry under `published`, `school`, or `personal`
2. Create `projects/your-project-name.md` (copy an existing one as template)
3. Add images to `assets/img/your-project-name/`
4. Commit and push

### Update project description
1. Edit `projects/project-name.md`
2. Commit and push

### Change site colors
Edit `assets/css/style.css`, lines 20-28 (CSS variables)

### Add social links
Edit `_includes/footer.html`

---

## 🐛 Troubleshooting

**Images not showing?**
- Check file paths match exactly (case-sensitive)
- Ensure images are committed: `git add assets/img/ && git commit -m "Add images"`

**Site not updating?**
- Wait 2-3 minutes after pushing
- Check GitHub repo → Actions tab for build status

**Layout broken?**
- Check YAML front matter syntax (dashes, spacing)
- Ensure all required fields are present

---

## 📂 File Quick Reference

| File | Purpose |
|------|---------|
| `_data/projects.yml` | Project metadata - **edit this to add/modify projects** |
| `index.md` | Home page content |
| `projects.md` | Projects listing page |
| `resume.md` | Resume page content |
| `projects/*.md` | Individual project detail pages |
| `assets/css/style.css` | All styling |
| `_includes/nav.html` | Navigation bar |
| `_config.yml` | Site configuration |

---

## 🎨 Image Checklist

Each project needs:
- ✅ `thumbnail.jpg` (600x400px) - for project cards
- ✅ `screenshot1.jpg`, `screenshot2.jpg`, etc. - for gallery
- ⚠️ `hero.jpg` (1200x400px) - optional banner image

Common placeholder:
- ✅ `assets/img/coming-soon.jpg` - for projects in development

Resume:
- ✅ `assets/pdfs/resume.pdf` - your resume PDF

---

## 🚀 Deployment Checklist

Before your first push:
1. ✅ Replace placeholder content with your real content
2. ✅ Add all your project images
3. ✅ Add your resume PDF
4. ✅ Update bio and skills on home page
5. ✅ Test locally (optional but recommended)
6. ✅ Commit and push to `main` branch
7. ✅ Verify site is live at https://WollyTech.github.io
8. ✅ Enable GitHub Pages in repo settings if not already enabled

---

For detailed instructions, see the full **README.md** file.
