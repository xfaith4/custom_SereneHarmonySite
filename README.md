# Serene Harmony — Stretch Professional Site (Starter)

This package contains a mobile-friendly, single-file website tailored for a stretching professional, with on-brand colors, elegant typography, soft edges, and a subtle paisley texture.

## Contents
- `index.html` — the site
- `assets/paisley.svg` — light seamless-style background (decorative pattern)
- `assets/living-marvel.svg` — ⚠️ PLACEHOLDER image (currently used in site)
- `assets/sacred-balance.svg` — ⚠️ PLACEHOLDER image (NOT currently used - can be removed or added to site)
- `assets/conclusion.svg` — ⚠️ PLACEHOLDER image (NOT currently used - can be removed or added to site)
- `CODE_REVIEW.md` — comprehensive security and code review documentation
- `.nojekyll` — GitHub Pages configuration file

## Customize
- Replace the three section images in `/assets/` with your own photos (keep names or update the `src` paths in `index.html`).
- To adjust the paisley texture strength, edit `opacity` in the `body::before` CSS (0.18–0.35 recommended).

## Lead Capture (Two Options)

### A) Netlify Forms (zero JS)
1. Drag-drop this folder into Netlify (or connect a repo).
2. Visit the deployed site once; Netlify will auto-detect the form named `stretch-contact`.
3. In Netlify → Forms, enable notifications as desired.

### B) Formspree (works anywhere)
1. Create a Formspree form → get your endpoint ID.
2. In `index.html`, change the `<form>` tag to:
   ```html
   <form action="https://formspree.io/f/YOUR_ID" method="POST" class="stack">
   ```
3. Remove `data-netlify` and the hidden `form-name` + honeypot if you like.

## Hosting

### GitHub Pages (Recommended Setup)
This repository is configured for GitHub Pages deployment:

1. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Navigate to **Settings** → **Pages**
   - Under "Source", select **Deploy from a branch**
   - Choose branch: `main` (or `master`)
   - Choose folder: `/ (root)`
   - Click **Save**

2. **Access your site:**
   - Your site will be available at: `https://[username].github.io/[repository-name]/`
   - For this repo: `https://xfaith4.github.io/custom_SereneHarmonySite/`
   - GitHub Pages will automatically rebuild when you push changes

3. **Custom Domain (Optional):**
   - In Pages settings, add your custom domain
   - Configure DNS with your domain provider
   - GitHub provides free HTTPS certificates

### Alternative Hosting Options
- **Netlify / Cloudflare Pages / Vercel**: drag-and-drop or connect your repo. No build step required.

## Squarespace (optional)
- Copy each section’s text into Squarespace sections.
- Add the small Custom CSS snippet (paisley layer + soft edges).
- Use Squarespace’s native Form block for submissions.

## Security & Code Review

A comprehensive code review has been completed. See `CODE_REVIEW.md` for full details.

**Summary:**
- ✅ No broken links found
- ✅ Form security implemented (honeypot, consent checkbox, input validation)
- ✅ Accessibility best practices followed
- ✅ No authentication system (not needed for this static site)
- ⚠️ Placeholder images should be replaced with actual photographs
- ⚠️ Consider adding a Privacy Policy page for form compliance

**Note on Login/Authentication:**
This is a static website with no login functionality. For a stretching professional's public website, this is the correct and secure approach. Contact form submissions are handled securely by Netlify Forms.

## Placeholder Assets

The following SVG files are **text-based placeholders** that should be replaced with actual photographs:
- `assets/living-marvel.svg` - Currently visible on the site
- `assets/sacred-balance.svg` - Not used (can be removed or integrated)
- `assets/conclusion.svg` - Not used (can be removed or integrated)

To replace: Upload your own images (JPG, PNG, or WebP) and update the `src` paths in `index.html`.

## License
You can use and modify this for personal or client work. Replace images as needed.
