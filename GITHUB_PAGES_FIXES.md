# GitHub Pages Build Fixes

## Issues Fixed

### ✅ Issue 1: Gemfile/Jekyll Version Mismatch

**Problem**: Your Gemfile requested Jekyll 4.1, but GitHub Pages only supports Jekyll 3.10.0.

**Solution**: Updated `Gemfile` to use the `github-pages` gem, which automatically includes all compatible versions of Jekyll and plugins that GitHub Pages supports.

**Before**:
```ruby
gem "jekyll", "~> 4.1"
gem "jekyll-sitemap", "~> 1.4.0"
# ... individual plugins
```

**After**:
```ruby
gem "github-pages", group: :jekyll_plugins
gem "jekyll-remote-theme"
```

### ✅ Issue 2: Layout Recursion / Stack Level Too Deep

**Problem**: The `paper.html` layout was manually including `site-header.html` and `site-footer.html`, but the Alembic theme's `default` layout already handles these, potentially causing conflicts or recursion.

**Solution**: Removed manual includes since the `default` layout already wraps content with header and footer.

**Changes Made**:
- Removed `{% include site-header.html %}` from top of paper.html
- Removed `{% include site-footer.html %}` from bottom of paper.html
- Optimized the related papers loop to be more efficient

### ✅ Issue 3: Include Recursion Issues

**Problem**: Liquid "stack level too deep" error when using includes in paper.html layout.

**Solution**: Inlined the resource links and BibTeX citation code directly into the paper.html layout instead of using separate include files. This completely eliminates any potential circular include issues that can occur with theme interactions.

---

## What to Do Next

### 1. Update Your Local Environment

Run these commands to update your local gems:

```bash
cd /Users/dmitry/Projects/style-transfer-lab.github.io

# Remove old Gemfile.lock
rm Gemfile.lock

# Install the correct versions
bundle install

# Test locally
bundle exec jekyll serve
```

### 2. Commit and Push

```bash
git add Gemfile _layouts/paper.html _includes/
git commit -m "Fix GitHub Pages compatibility issues"
git push origin main
```

### 3. Monitor the Build

- Go to your repository on GitHub
- Click "Actions" tab
- Watch the build process
- It should complete successfully now! ✅

---

## What Changed

### Files Modified:

1. **Gemfile** - Updated to use `github-pages` gem
2. **_layouts/paper.html** - Removed redundant header/footer includes, inlined resource links and BibTeX sections, optimized loops
3. **_includes/resource-links.html** - Kept for reference but not used in paper layout (inlined instead)
4. **_includes/bibtex-citation.html** - Kept for reference but not used in paper layout (inlined instead)
5. **_includes/image-gallery.html** - Simplified to use `page.*` directly
6. **_includes/paper-card.html** - Still used in papers index and homepage

---

## GitHub Pages Compatibility Notes

### Supported Jekyll Version
- **Jekyll 3.10.0** (not 4.x)
- Using the `github-pages` gem ensures you always have compatible versions

### Supported Plugins
GitHub Pages only supports certain plugins. The `github-pages` gem includes:
- jekyll-sitemap
- jekyll-mentions
- jekyll-paginate
- jekyll-seo-tag
- jekyll-redirect-from
- jekyll-feed
- jekyll-commonmark
- jekyll-include-cache
- jemoji
- jekyll-remote-theme
- And more...

### Remote Theme
The Alembic theme works via `jekyll-remote-theme`, which is supported.

---

## Testing Locally

To ensure your site works exactly like it will on GitHub Pages:

```bash
# Clean build
bundle exec jekyll clean
bundle exec jekyll build

# Serve locally
bundle exec jekyll serve

# Visit http://localhost:4000
```

---

## Common Build Errors & Solutions

### Error: "Bundler can't satisfy dependencies"
**Solution**: Delete `Gemfile.lock` and run `bundle install`

### Error: "Liquid Exception: nesting too deep"
**Solution**: Already fixed! Includes now use `page.*` directly

### Error: "Layout not found"
**Solution**: Make sure `layout: default` (not `layout: paper`) is used correctly

### Error: "Unknown tag 'include'"
**Solution**: Check Liquid syntax - might be a typo or unclosed tag

---

## Verification Checklist

After pushing, verify:
- [ ] GitHub Actions build completes (green checkmark)
- [ ] Site deploys to `https://style-transfer-lab.github.io`
- [ ] Homepage loads correctly
- [ ] Papers page loads with grid layout
- [ ] Individual paper pages show properly
- [ ] Navigation works between pages
- [ ] Custom CSS loads (check gradient hero, colored badges)
- [ ] Search/filter works on papers page
- [ ] Mobile responsive (test on phone or DevTools)

---

## If Build Still Fails

1. **Check the Actions tab** on GitHub for detailed error logs
2. **Look for the specific error message** - it will point to the problematic file
3. **Common culprits**:
   - Liquid syntax errors (unclosed tags, typos)
   - YAML frontmatter formatting (indentation, colons)
   - Missing files referenced in includes
   - Invalid markdown syntax

4. **Quick fixes**:
   - Validate YAML: https://www.yamllint.com/
   - Check Liquid syntax in any custom includes
   - Ensure all referenced images exist in `assets/images/`

---

## Additional Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Pages Dependency Versions](https://pages.github.com/versions/)
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Alembic Theme Docs](https://alembic.darn.es/)

---

## Success! 🎉

Your site should now build successfully on GitHub Pages. The fixes ensure:
- Compatible Jekyll and plugin versions
- No layout recursion issues
- Simplified, efficient Liquid includes
- Full compatibility with GitHub Pages' build environment

**Next**: After the build succeeds, add your paper links and team information as described in `QUICK_START.md`!
