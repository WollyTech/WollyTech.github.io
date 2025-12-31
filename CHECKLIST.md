# 📋 Pre-Launch Checklist

Use this checklist to ensure everything is ready before deploying your portfolio.

## ✅ Content Checklist

### Images (Required)
- [ ] `assets/img/operation-reclaim/thumbnail.jpg` (600x400px)
- [ ] `assets/img/experiment-vessel/thumbnail.jpg` (600x400px)
- [ ] `assets/img/wisteria/thumbnail.jpg` (600x400px)
- [ ] `assets/img/olis-cofferia/thumbnail.jpg` (600x400px)
- [ ] `assets/img/coming-soon.jpg` (600x400px)

### Gallery Images (Recommended)
- [ ] Operation Reclaim: 3+ screenshots in `assets/img/operation-reclaim/`
- [ ] Experiment Vessel: 3+ screenshots in `assets/img/experiment-vessel/`
- [ ] Wisteria: 4+ screenshots in `assets/img/wisteria/`
- [ ] Oli's Cofferia: 3+ screenshots in `assets/img/olis-cofferia/`

### Documents
- [ ] `assets/pdfs/resume.pdf` - Your current resume

### Page Content
- [ ] `index.md` - Updated bio and skills section
- [ ] `resume.md` - Added experience and education
- [ ] `projects/operation-reclaim.md` - Reviewed and enhanced
- [ ] `projects/experiment-vessel.md` - Reviewed and enhanced
- [ ] `projects/wisteria.md` - Reviewed and enhanced
- [ ] `projects/olis-cofferia.md` - Reviewed and enhanced

## 🎨 Design Customization (Optional)

- [ ] Updated accent color in `assets/css/style.css` (line 24)
- [ ] Reviewed and adjusted other colors if needed
- [ ] Added social links to `_includes/footer.html`
- [ ] Customized navigation brand text if desired

## 🧪 Testing

### Local Testing (Recommended)
- [ ] Ran `bundle install` successfully
- [ ] Ran `bundle exec jekyll serve` successfully
- [ ] Visited http://localhost:4000
- [ ] Checked home page loads correctly
- [ ] Checked all navigation links work
- [ ] Checked project cards appear with images
- [ ] Clicked into each project detail page
- [ ] Verified YouTube embeds work (if videos load)
- [ ] Tested on mobile view (browser dev tools)
- [ ] Checked resume PDF download link works

### Content Review
- [ ] Spell-checked all content
- [ ] Verified all links are correct
- [ ] Checked image paths are correct
- [ ] Reviewed project descriptions for accuracy
- [ ] Ensured no placeholder text remains (except where intended)

## 📤 Git & Deployment

### Before First Push
- [ ] All files saved
- [ ] Images added to correct folders
- [ ] Resume PDF added
- [ ] No sensitive information in files

### Git Commands
```bash
# Check status
git status

# Add all files
git add .

# Commit with message
git commit -m "Complete portfolio migration from Weebly"

# Push to GitHub
git push origin main
```

### GitHub Pages Setup
- [ ] Went to https://github.com/WollyTech/WollyTech.github.io/settings/pages
- [ ] Source set to: "Deploy from a branch"
- [ ] Branch set to: "main"
- [ ] Folder set to: "/ (root)"
- [ ] Clicked "Save"

### Post-Deployment
- [ ] Waited 2-3 minutes for build
- [ ] Visited https://WollyTech.github.io
- [ ] Home page loads correctly
- [ ] Navigation works
- [ ] All images display
- [ ] Project pages load
- [ ] YouTube videos embed correctly
- [ ] Resume PDF downloads
- [ ] Mobile view looks good
- [ ] No broken links

## 🐛 Troubleshooting

### If images don't show:
1. Check file paths in `_data/projects.yml` and project `.md` files
2. Verify filenames match exactly (case-sensitive)
3. Ensure images were committed: `git status`
4. Check browser console for 404 errors
5. Try hard refresh (Ctrl+F5 or Cmd+Shift+R)

### If site doesn't build:
1. Check GitHub Actions tab in repo for errors
2. Verify YAML syntax in files (spacing matters!)
3. Check `_config.yml` for errors
4. Look for typos in front matter

### If layout is broken:
1. Check for missing closing tags in HTML files
2. Verify CSS file is loading (check browser dev tools)
3. Clear browser cache
4. Check for JavaScript errors in console

## 📝 Post-Launch Tasks

### Immediate
- [ ] Share URL with friends for feedback
- [ ] Test on different devices (phone, tablet)
- [ ] Test on different browsers (Chrome, Firefox, Safari)
- [ ] Check loading speed

### Soon
- [ ] Add more projects as they're completed
- [ ] Update retrospective section with articles
- [ ] Consider adding blog functionality
- [ ] Add analytics (Google Analytics) if desired
- [ ] Create social media cards (OpenGraph images)

### Ongoing Maintenance
- [ ] Update resume when experience changes
- [ ] Add new projects to `_data/projects.yml`
- [ ] Keep content fresh and current
- [ ] Fix any reported issues
- [ ] Optimize images if site loads slowly

## 🎯 Success Criteria

Your portfolio is ready to launch when:

✅ All required images are present and display correctly
✅ All navigation links work
✅ Project pages load with YouTube embeds (where applicable)
✅ Resume PDF downloads successfully
✅ Site is mobile-responsive
✅ No broken links or 404 errors
✅ Content is spell-checked and accurate
✅ Site builds successfully on GitHub Pages

## 🚀 Launch!

Once all items are checked off:

1. Make final commit
2. Push to main branch
3. Enable GitHub Pages (if not already done)
4. Wait for build (1-2 minutes)
5. Visit https://WollyTech.github.io
6. Celebrate! 🎉

---

**Need help?** Check the documentation:
- START_HERE.txt - Overview and quick start
- README.md - Comprehensive guide
- QUICK_START.md - Common tasks reference
- IMAGE_GUIDE.md - Image specifications

**Last updated:** December 20, 2025
