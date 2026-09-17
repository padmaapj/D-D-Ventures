# PHP → Vercel migration

Old architecture:
PHP + MySQL + PHPMailer + PHP sessions.

Vercel architecture:
Next.js + React + Node.js serverless route + Resend.

The public website and enquiry flow are migrated. The old PHP admin CMS is not copied because PHP sessions and PHP pages are not the right deployment model for a Vercel Next.js application.

Recommended next step for a full CMS:
- Neon/Supabase/Postgres
- Auth.js or another secure auth provider
- Vercel Blob/Cloudinary for portfolio images
- Protected `/admin` Next.js routes
