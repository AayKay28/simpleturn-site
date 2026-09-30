# SimpleTurn — simpleturn.ca

Static marketing site for SimpleTurn: AI ops systems for Canadian real estate agents.

Every page is a self-contained HTML file. Images, logos, fonts, scripts and styles are embedded, so nothing depends on external assets at runtime. No build step.

## Structure
- index.html — Home (/)
- checklist.html — Free AI Agent Starter Checklist (/checklist)
- founding.html — Founding Membership (/founding)
- library.html — Member library placeholder (/library)
- privacy.html, terms.html — Legal (/privacy, /terms)
- blog.html — Blog grid (/blog)
- blog/*.html — Posts (/blog/<slug>), each with Article + FAQPage + Breadcrumb schema
- brand/, images/ — Public copies used for Open Graph / social link previews and schema
- robots.txt, sitemap.xml, llms.txt — Search and AI crawler files
- vercel.json — Clean URLs (no .html)

## Deploy (GitHub → Vercel)
1. Push this folder's contents to the repo root.
2. In Vercel: New Project → import the repo → Framework preset "Other" → no build command, output directory `.` (root).
3. Project name: simpleturn. Add domain simpleturn.ca under Settings → Domains.

## Before launch
- Checkout buttons are Stripe (test) placeholders — connect Stripe Checkout links.
- Checklist and subscribe forms show a confirmation only — connect an email provider (CASL consent is captured on the checklist form).
- Add publish dates to blog posts to enable datePublished in schema.
