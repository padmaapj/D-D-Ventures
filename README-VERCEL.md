# D&D Ventures — Vercel Edition

This is a clean Next.js conversion of the D&D Ventures site for Vercel.

Vercel is designed for Next.js and supports server-side functionality through Vercel Functions. This build therefore replaces the original PHP/MySQL/PHPMailer architecture with:
- Next.js App Router
- React
- Vercel Node.js Function for enquiries
- Resend for email delivery
- Environment variables for production configuration

## Deploy

1. Create a GitHub repository and upload this project.
2. Import the repository into Vercel.
3. Vercel should detect Next.js automatically.
4. Add the variables from `.env.example` in Vercel Project Settings → Environment Variables.
5. Set `NEXT_PUBLIC_SITE_URL` to the final HTTPS domain.
6. Set `RESEND_API_KEY`, `ENQUIRY_TO_EMAIL` and `ENQUIRY_FROM_EMAIL`.
7. Deploy.
8. Test `/`, `/about`, `/services`, `/portfolio`, `/contact`, every service page, `/privacy`, `/terms`, `/sitemap.xml` and `/robots.txt`.
9. Submit a test enquiry.
10. Connect the custom domain in Vercel.

## Email

The enquiry API uses Resend. Before production, verify the sending domain in Resend and use an email address from that verified domain as `ENQUIRY_FROM_EMAIL`.

## Important

The portfolio images included here are demo assets from the earlier development build. Replace them with approved real work before publishing.

This Vercel version intentionally does not carry over the PHP admin dashboard. A proper Vercel-native admin/CMS should be added separately using a database + authentication provider rather than trying to run the PHP admin on Vercel.
