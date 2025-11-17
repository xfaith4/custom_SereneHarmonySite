# Form Setup Instructions

The contact form has been configured to send submissions to **rleighc88b@gmail.com** using Formspree.

## Setup Steps

1. **Create a Formspree Account** (Free):
   - Go to https://formspree.io/
   - Sign up with the email address: rleighc88b@gmail.com
   - Verify your email address

2. **Create a New Form**:
   - In your Formspree dashboard, click "New Form"
   - Name it: "Peace Love and Body Work - Contact"
   - Copy your form endpoint ID (looks like: `xanybjql`)

3. **Update the Form** (if needed):
   - Open `index.html`
   - Find line 265: `action="https://formspree.io/f/xanybjql"`
   - Replace `xanybjql` with your actual Formspree form ID
   - Save the file

4. **Configure Email Settings** (in Formspree dashboard):
   - Set notification email to: rleighc88b@gmail.com
   - Enable email notifications for new submissions
   - Optional: Customize the email template
   - Optional: Set up auto-reply to submitters

5. **Test the Form**:
   - Visit your website
   - Fill out the contact form
   - Submit it
   - Check rleighc88b@gmail.com for the email
   - The user will see: "Thank you! Your assessment request has been received. Someone will reach out to you soon with available times and a suggested plan."

## Form Features

- **Anti-spam**: Includes honeypot field to prevent bot submissions
- **Validation**: All fields are validated before submission
- **User Feedback**: Success/error messages displayed after submission
- **Accessibility**: Form status updates are announced to screen readers

## Troubleshooting

- If emails aren't arriving, check your Formspree dashboard spam settings
- Ensure rleighc88b@gmail.com is verified in Formspree
- Check your Gmail spam folder
- The free Formspree plan has a limit of 50 submissions per month

## Alternative: Direct Mailto (Fallback)

If you prefer not to use Formspree, you can use a direct mailto link:
- This will open the user's email client
- Less seamless user experience
- No submission tracking
- See README.md for implementation details
