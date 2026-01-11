# 🚀 Quick Start Guide

## Preview Your New Website

### 1. Start Jekyll Server

```bash
cd /Users/dmitry/Projects/style-transfer-lab.github.io
bundle exec jekyll serve
```

### 2. Open in Browser

Visit: `http://localhost:4000`

---

## 🎯 Immediate To-Do List

### Priority 1: Add Paper Links (5 minutes per paper)

Open each paper file in `_papers/` and uncomment the link lines:

```yaml
# Change this:
# arxiv: https://arxiv.org/abs/...

# To this:
arxiv: https://arxiv.org/abs/2501.12345
```

**Files to update:**
- `_papers/any-to-cloth-virtual-try-on.md`
- `_papers/color-conditional-generation.md`
- `_papers/color-transfer-modflows.md`
- `_papers/fbm-generative-inpainting.md`
- `_papers/hessian-geometry-latent-space.md`

### Priority 2: Update Team Info (10 minutes)

Edit `about.md`:

1. Replace placeholder bios with real ones:
```markdown
<p class="team-member-bio">
Your actual bio here (2-3 sentences about your research)
</p>
```

2. Add your links:
```html
<a href="https://scholar.google.com/citations?user=YOUR_ID" class="team-member-link" target="_blank">📚 Scholar</a>
<a href="https://github.com/yourusername" class="team-member-link" target="_blank">💻 GitHub</a>
```

### Priority 3: Add Contact Email (1 minute)

In `about.md`, find "Get in Touch" section and add:

```html
<p style="font-size: 1.1em; margin: 10px 0;">
📧 Email: <a href="mailto:youremail@example.com">youremail@example.com</a>
</p>
```

---

## 🎨 What's New

### Pages You Should Check:
1. **Homepage** (`/`) - New hero section and featured papers
2. **Research** (`/papers/`) - Filterable grid with search
3. **Themes** (`/research-themes/`) - Papers organized by topic
4. **Team** (`/about/`) - Professional team showcase
5. **Individual Papers** - Enhanced layout with resources

### Try These Features:
- 🔍 Search papers by keyword
- 🏷️ Filter by year or venue type
- 📋 Copy BibTeX citations (one-click)
- 📱 Test on mobile (fully responsive)
- ⬆️ Back-to-top button (appears when scrolling)
- 🎨 Smooth animations and transitions

---

## 📸 Optional: Add Team Photos

1. Create directory:
```bash
mkdir -p assets/images/team
```

2. Add photos (recommended: 300x300px, square):
```bash
# Copy your photos
cp ~/photo.jpg assets/images/team/alexander.jpg
```

3. Update `about.md`:
```html
<!-- Uncomment and update: -->
<img src="/assets/images/team/alexander.jpg" alt="Alexander Lobashev" class="team-member-photo">
```

---

## ✅ Quick Checklist

Before going live:
- [ ] Add arXiv/OpenReview links to all papers
- [ ] Add GitHub repository links
- [ ] Update team bios and research interests
- [ ] Add team member links (Scholar, GitHub)
- [ ] Add contact email in about page
- [ ] Test on Chrome, Firefox, Safari
- [ ] Test on mobile device
- [ ] Check all links work
- [ ] Proofread all text content

---

## 🚨 Common Issues

**Problem**: CSS not loading
**Solution**: Hard refresh (`Cmd+Shift+R` on Mac, `Ctrl+Shift+R` on Windows)

**Problem**: Papers not showing on homepage
**Solution**: Check that `featured: true` is set in paper frontmatter

**Problem**: Search/filter not working
**Solution**: Check browser console (F12) for JavaScript errors

**Problem**: Layout broken on mobile
**Solution**: Clear cache, check viewport meta tag exists

---

## 📝 Making Changes

### Update Site Description
Edit `_config.yml` - line 27:
```yaml
description: 'Your new description here'
```

### Change Colors
Edit `assets/styles/custom.css` - lines 10-15:
```css
--primary-blue: #2196F3;    /* Your color */
--accent-purple: #9C27B0;   /* Your color */
```

### Add New Paper
1. Create file: `_papers/new-paper.md`
2. Copy frontmatter from existing paper
3. Update all fields
4. Add image to `assets/images/`

---

## 🎉 You're Ready!

Your website has been completely redesigned with:
- Modern, professional appearance
- Full mobile responsiveness
- Search and filtering
- Interactive features
- Team showcase
- Research themes organization

**Next step**: Run `bundle exec jekyll serve` and preview at `http://localhost:4000`

For detailed information, see `IMPLEMENTATION_GUIDE.md`.

---

**Need help?** Check the comments in the code files - they have helpful hints!

Good luck with your research! 🔬✨
