# Image Preparation Guide

## 📐 Required Image Specifications

### Project Thumbnails
- **Size:** 600 x 400 pixels (3:2 aspect ratio)
- **Format:** JPG (preferred) or PNG
- **Quality:** High quality, web-optimized
- **Purpose:** Shown on project cards on the Projects page and Home page
- **Content:** Should clearly represent the project - gameplay screenshot, logo, or key visual

**Files needed:**
- `assets/img/operation-reclaim/thumbnail.jpg`
- `assets/img/experiment-vessel/thumbnail.jpg`
- `assets/img/wisteria/thumbnail.jpg`
- `assets/img/olis-cofferia/thumbnail.jpg`

### Gallery Screenshots
- **Size:** 800 x 600 pixels minimum (4:3 ratio), or larger
- **Format:** JPG or PNG
- **Quality:** High quality for detail viewing
- **Purpose:** Displayed in project detail page galleries
- **Content:** Gameplay screenshots, UI examples, environment shots, character art

**Files needed per project:**
- At least 3 screenshots per project
- Name them: `screenshot1.jpg`, `screenshot2.jpg`, `screenshot3.jpg`, etc.

### Hero/Banner Images (Optional)
- **Size:** 1200 x 400 pixels (3:1 aspect ratio)
- **Format:** JPG
- **Purpose:** Large banner at top of project detail pages
- **Content:** Wide landscape shot of game environment or key art

**Current usage:**
- Wisteria has a hero image configured
- Optional for other projects

### Coming Soon Placeholder
- **Size:** 600 x 400 pixels (3:2 aspect ratio)
- **Format:** JPG or PNG
- **Content:** Generic placeholder - could be:
  - Your logo on dark background
  - "Coming Soon" text with subtle graphics
  - Abstract game-related imagery

**File needed:**
- `assets/img/coming-soon.jpg`

---

## 🎨 Quick Image Editing Tips

### Using Online Tools (Free)

**Resize Images:**
- [Photopea](https://www.photopea.com/) - Free online Photoshop alternative
- [Canva](https://www.canva.com/) - Easy templates and resizing
- [GIMP](https://www.gimp.org/) - Free desktop software

**Batch Resize:**
- [Bulk Resize Photos](https://bulkresizephotos.com/)
- [ILoveIMG](https://www.iloveimg.com/resize-image)

### Taking Screenshots from YouTube

For projects with YouTube videos:
1. Open video at https://youtube.com/watch?v=VIDEO_ID
2. Pause at a good moment
3. Full screen (F key)
4. Screenshot (Print Screen or Snipping Tool on Windows)
5. Crop and resize to required dimensions

### Creating a Coming Soon Image

**Option 1: Simple Text**
```
1. Open Canva or Photopea
2. Create 600x400px canvas
3. Set background to #242424 (or dark color)
4. Add "COMING SOON" text in white or #4a9eff
5. Export as JPG
```

**Option 2: Use a Logo**
```
1. Place your logo/brand on dark background
2. Ensure 600x400px dimensions
3. Keep it clean and simple
```

---

## 📸 Screenshot Best Practices

### What Makes a Good Screenshot

✅ **Good:**
- Clear, in-focus visuals
- Interesting composition
- Shows key gameplay or features
- Good lighting/visibility
- No UI clutter (unless showcasing UI)

❌ **Avoid:**
- Blurry or low-resolution images
- Dark/hard to see content
- Debug text or watermarks
- Boring or empty scenes

### Capturing from Unity

If you have Unity projects:
```csharp
// Add this script to capture high-res screenshots
void Update() {
    if (Input.GetKeyDown(KeyCode.F12)) {
        ScreenCapture.CaptureScreenshot("screenshot.png", 2); // 2x resolution
    }
}
```

### Organizing Your Captures

1. Create a folder for raw screenshots
2. Select best 3-5 per project
3. Crop and resize to specs
4. Rename clearly (screenshot1.jpg, screenshot2.jpg)
5. Place in correct project folder

---

## 🔄 Image Optimization

Before uploading, optimize images for web:

**Online Tools:**
- [TinyPNG](https://tinypng.com/) - Compress PNG/JPG
- [Squoosh](https://squoosh.app/) - Google's image optimizer
- [ImageOptim](https://imageoptim.com/) - Mac app

**Goal:** Reduce file size while maintaining visual quality
- Thumbnails: Aim for under 200KB each
- Screenshots: Aim for under 500KB each
- Total all images: Try to keep under 5MB total

---

## 📋 Image Checklist

### Operation Reclaim
- [ ] thumbnail.jpg (600x400)
- [ ] screenshot1.jpg (800x600+)
- [ ] screenshot2.jpg (800x600+)
- [ ] screenshot3.jpg (800x600+)

### Experiment Vessel
- [ ] thumbnail.jpg (600x400)
- [ ] screenshot1.jpg (800x600+)
- [ ] screenshot2.jpg (800x600+)
- [ ] screenshot3.jpg (800x600+)

### Wisteria
- [ ] thumbnail.jpg (600x400)
- [ ] hero.jpg (1200x400) - Optional banner
- [ ] screenshot1.jpg (800x600+)
- [ ] screenshot2.jpg (800x600+)
- [ ] screenshot3.jpg (800x600+)
- [ ] screenshot4.jpg (800x600+)

### Oli's Cofferia
- [ ] thumbnail.jpg (600x400)
- [ ] screenshot1.jpg (800x600+)
- [ ] screenshot2.jpg (800x600+)
- [ ] screenshot3.jpg (800x600+)

### General
- [ ] coming-soon.jpg (600x400)

---

## 🚀 After Adding Images

1. Place files in correct folders
2. Verify filenames match exactly (case-sensitive!)
3. Test locally: `bundle exec jekyll serve`
4. Commit and push:
   ```bash
   git add assets/img/
   git commit -m "Add project images"
   git push origin main
   ```
5. Wait 1-2 minutes for deployment
6. Check live site

---

## 🐛 Troubleshooting

**Images not showing?**
- Check file extension (.jpg vs .jpeg)
- Verify folder structure
- Ensure images are committed and pushed
- Check browser console for 404 errors

**Images look bad/stretched?**
- Verify aspect ratios match specifications
- Check that original image quality is good
- Try re-exporting at higher quality

**Site loads slowly?**
- Optimize images (use TinyPNG)
- Reduce file sizes
- Consider using WebP format (requires code changes)

---

Need help with image editing? Check out the free tools listed above or ask for assistance!
