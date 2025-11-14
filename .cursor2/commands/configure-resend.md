# Configure Resend

Configures Resend for sending transactional emails in your project. Sets up API keys, email templates, and email sending utilities.

1. **Check prerequisites**
   - Verify Resend account exists (user needs to create account at resend.com)
   - Check if Resend API key is already configured
   - Verify project structure (Next.js project with package.json)

2. **Install Resend SDK**
   - Install `resend` package: `pnpm add resend`
   - Verify installation completed successfully

3. **Set up Resend account**
   - **If no account:** Guide user to create account at resend.com
   - **If account exists:** Ask for API key or guide to find it in dashboard
   - Verify API key is valid (test connection)

4. **Configure environment variables**
   - Check if `.env.local` exists, create if not
   - Add Resend environment variables:
     - `RESEND_API_KEY` - Your Resend API key
   - Add to `.env.example` (without actual values) for reference
   - Verify variables are set correctly

5. **Set up Resend client utilities**
   - Create `lib/resend.ts` or `lib/email.ts` for Resend client initialization
   - Set up email sending utilities
   - Create email templates (if using templates)
   - Set up TypeScript types for emails

6. **Configure email templates (optional)**
   - Set up email templates in Resend dashboard (if using)
   - Or create template functions in code
   - Set up email rendering (React Email or plain HTML)

7. **Set up email sending functions**
   - Create email sending utilities:
     - Transactional emails (welcome, password reset, etc.)
     - Notification emails
     - Marketing emails (if needed)
   - Set up error handling for email sending
   - Set up email logging (optional)

8. **Configure domain (if sending from custom domain)**
   - Guide through adding domain in Resend dashboard
   - Configure DNS settings (SPF, DKIM, DMARC)
   - Verify domain is verified
   - Set up domain in environment variables (if needed)

9. **Test email sending**
   - Test sending a simple email
   - Verify email is received
   - Test error handling
   - Verify email formatting
   - Check Resend dashboard for delivery status

10. **Document configuration**
    - Create `doc/` folder if it doesn't exist
    - Create file: `doc/configure-resend-YYYY-MM-DD.md`
    - Document: API key configured, email utilities created, templates set up, domain configured (if any)

## What to Tell the User

- Start: "I'll help you configure Resend for sending emails. Do you have a Resend account? If not, you'll need to create one at resend.com."
- If no account: "Please create a Resend account at resend.com, then provide your API key."
- If account exists: "Please provide your Resend API key, or I can help you find it in your Resend dashboard."
- During setup: "Installing Resend SDK...", "Configuring environment variables...", "Setting up email utilities..."
- After configuration: "Resend is configured! I've set up email sending utilities. Test it by sending a test email."
- If errors: Explain what went wrong and how to fix it

## See Also

### Related Services
- **[Configure Supabase](.cursor/commands/configure-supabase.md)**: Auth, Database, Storage, Realtime
- **[Configure Vercel](.cursor/commands/configure-vercel.md)**: Hosting and deployment
- **[Configure Trigger.dev](.cursor/commands/configure-trigger-dev.md)**: Background jobs

### Technical Guidelines
- **[Resend Documentation](https://resend.com/docs)**: Official Resend docs
- **[React Email](https://react.email)**: For building email templates with React




