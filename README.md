# Peace Love and Body Work — Professional Stretchology Site

This package contains a mobile-friendly, single-file website for a professional Stretchology practice, featuring industry-specific terminology, evidence-based methodologies (FST, PNF, myofascial release), elegant typography, and a subtle paisley texture. The site emphasizes one-on-one certified professional services with customized treatment plans.

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

## Lead Capture - Formspree Configuration

**Current Setup:** The contact form is configured to use Formspree and send submissions to **rleighc88b@gmail.com**.

### Setup Steps (Required)

1. **Create a Formspree Account** (Free):
   - Go to https://formspree.io/
   - Sign up with the email address: **rleighc88b@gmail.com**
   - Verify your email address

2. **Create a New Form**:
   - In your Formspree dashboard, click "New Form"
   - Name it: "Peace Love and Body Work - Contact"
   - Copy your form endpoint ID (looks like: `xanybjql`)

3. **Update the Form Endpoint** (if needed):
   - Open `index.html`
   - Find line 265: `action="https://formspree.io/f/xanybjql"`
   - Replace `xanybjql` with your actual Formspree form ID
   - Save the file

4. **Configure Email Settings** (in Formspree dashboard):
   - Set notification email to: **rleighc88b@gmail.com**
   - Enable email notifications for new submissions
   - Optional: Customize the email template
   - Optional: Set up auto-reply to submitters

5. **Test the Form**:
   - Visit your deployed website
   - Fill out and submit the contact form
   - Check **rleighc88b@gmail.com** for the email
   - Users will see: "✓ Thank you! Your assessment request has been received. Someone will reach out to you soon with available times and a suggested plan."

### Form Features

- **JavaScript-enhanced submission**: Shows success/error messages without page reload
- **Anti-spam protection**: Includes honeypot field to prevent bot submissions
- **Form validation**: All required fields validated before submission
- **User feedback**: Success/error messages displayed after submission
- **Accessibility**: Form status updates are announced to screen readers

See `FORM_SETUP.md` for detailed setup instructions and troubleshooting.

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
