# GitHub Pages Deployment Guide

## Quick Start

This repository is ready to be deployed to GitHub Pages. Follow these simple steps:

## Step 1: Enable GitHub Pages

1. Go to your repository on GitHub: `https://github.com/xfaith4/custom_SereneHarmonySite`
2. Click on **Settings** (top navigation bar)
3. Scroll down and click on **Pages** (left sidebar)
4. Under **Source**, select:
   - **Deploy from a branch**
   - Branch: `main` (or `master`)
   - Folder: `/ (root)`
5. Click **Save**

## Step 2: Wait for Deployment

- GitHub will automatically build and deploy your site (takes 1-2 minutes)
- You'll see a message: "Your site is live at `https://xfaith4.github.io/custom_SereneHarmonySite/`"
- A green checkmark will appear when deployment is complete

## Step 3: Access Your Site

Your site will be available at:
```
https://xfaith4.github.io/custom_SereneHarmonySite/
```

## Step 4: Verify Deployment

Open your site and check:
- ✅ All pages load correctly (index.html, privacy.html)
- ✅ Images and assets display properly
- ✅ Navigation links work
- ✅ Contact form is functional
- ✅ HTTPS is enabled (automatic with GitHub Pages)

## Automatic Updates

Once GitHub Pages is enabled:
- Any changes you push to the `main` branch will automatically redeploy
- No manual build process needed
- Updates typically appear within 1-2 minutes

## Custom Domain (Optional)

To use your own domain name:

### Step 1: Configure DNS
Add these DNS records at your domain provider:

**For apex domain (example.com):**
```
Type: A
Name: @
Value: 185.199.108.153
Value: 185.199.109.153
Value: 185.199.110.153
Value: 185.199.111.153
```

**For www subdomain (www.example.com):**
```
Type: CNAME
Name: www
Value: xfaith4.github.io
```

### Step 2: Add Custom Domain in GitHub
1. Go to repository **Settings** → **Pages**
2. Under **Custom domain**, enter your domain (e.g., `example.com` or `www.example.com`)
3. Click **Save**
4. Wait for DNS check to complete (can take up to 24 hours)

### Step 3: Enable HTTPS
1. Once DNS is verified, check **Enforce HTTPS**
2. GitHub will automatically provision an SSL certificate (free)
3. Your site will be accessible via secure HTTPS

## Troubleshooting

### Site not loading?
- Wait 1-2 minutes after enabling Pages
- Check that the branch name is correct (`main` or `master`)
- Verify files are in the root directory (not in a subfolder)

### Images not displaying?
- Make sure `assets/` folder is in the root directory
- Check that `.nojekyll` file exists (prevents Jekyll processing)

### Form not working?
- Netlify Forms requires deployment on Netlify (not GitHub Pages)
- Alternative: Switch to Formspree (see README.md)
- For GitHub Pages, consider: Formspree, Getform, or Web3Forms

### Custom domain not working?
- Wait up to 24 hours for DNS propagation
- Verify DNS records with: `dig example.com` or `nslookup example.com`
- Check DNS configuration at your domain provider

## Files Configured for GitHub Pages

The following files ensure proper GitHub Pages deployment:

- **`.nojekyll`** - Prevents Jekyll processing (allows files starting with underscore)
- **`index.html`** - Main landing page (must be in root)
- **`privacy.html`** - Privacy policy page
- **`assets/`** - Images and SVG files
- **`README.md`** - Repository documentation

## Contact Form Considerations

**Important:** The contact form currently uses Netlify Forms, which only works on Netlify hosting.

### Option A: Keep Netlify Forms (Recommended)
Deploy to Netlify instead of GitHub Pages:
1. Go to [netlify.com](https://www.netlify.com)
2. Click "Add new site" → "Import an existing project"
3. Connect your GitHub repository
4. Deploy (automatic form detection)

### Option B: Switch to Formspree (Works on GitHub Pages)
1. Create a free account at [formspree.io](https://formspree.io)
2. Create a new form and get your endpoint
3. Update `index.html` form tag:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" class="stack">
   ```
4. Remove `data-netlify` and `netlify-honeypot` attributes

### Option C: Use Web3Forms (Free, No Account Needed)
1. Get free access key at [web3forms.com](https://web3forms.com)
2. Add hidden field to form:
   ```html
   <input type="hidden" name="access_key" value="YOUR_ACCESS_KEY">
   ```
3. Update form action:
   ```html
   <form action="https://api.web3forms.com/submit" method="POST" class="stack">
   ```

## Security Features

Already implemented:
- ✅ HTTPS (automatic with GitHub Pages)
- ✅ Form honeypot spam protection
- ✅ Input validation (HTML5)
- ✅ Privacy policy page
- ✅ Consent checkbox (GDPR compliant)
- ✅ Referrer policy meta tag
- ✅ No sensitive data collection

## Performance

GitHub Pages provides:
- Global CDN (Content Delivery Network)
- Fast page loads
- Automatic compression
- 99.9% uptime
- No cost (free hosting)

## Next Steps After Deployment

1. **Test everything:** Click through all links and test the contact form
2. **Replace placeholders:** Update SVG images with actual photos (see CODE_REVIEW.md)
3. **Add testimonials:** Replace example quotes with real client feedback
4. **Update content:** Customize text for your specific services
5. **Share your site:** Add URL to social media and business cards
6. **Monitor form submissions:** Check Netlify dashboard or Formspree inbox

## Need Help?

- **GitHub Pages Documentation:** https://docs.github.com/en/pages
- **Formspree Documentation:** https://help.formspree.io/
- **Web3Forms Documentation:** https://docs.web3forms.com/

## Maintenance

- **Update content:** Edit files, commit, and push to GitHub
- **Check form submissions:** Log into Netlify/Formspree dashboard
- **Monitor site:** GitHub provides analytics in Settings → Insights
- **Backup:** Your code is already backed up on GitHub

---

**Your site is ready to go live! 🚀**

Just enable GitHub Pages in Settings and you'll be online in minutes.
