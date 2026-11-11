# iGT B2B Hub — MVP preview

A responsive, single-page prototype for the AIESEC in Ruhuna Winter 26.27 B2B company workflow.

## Run it

Open `index.html` in a modern browser. No build tools are required.

## Demo features

- Switch between Member, TL, Manager, Specialist and LCVP preview roles.
- Members can submit companies and see only their own demo records.
- Duplicate-name checks warn for existing companies; previously rejected companies trigger a specific warning.
- CRM review is available to non-member roles; rejection requires a reason.
- TL preview is scoped to Team A; Manager, Specialist and LCVP previews show the organisation.
- Members can log calls only against CRM-approved companies.
- Data is saved in browser localStorage for this prototype.

## Important limitations

This is a front-end MVP, not production CRM software. It has no real login, shared database, server-side authorization, audit-grade security, or live multi-user sync. Role switching is a demo control, not authentication. Do not enter real personal or company contact information. The next production step is to connect Supabase Auth + PostgreSQL and enforce permissions with Row Level Security (RLS), then import the cleaned workbook data.

## Deploy with GitHub Pages

1. Create a GitHub repository (preferably **private** while preparing real data; Pages availability for private repositories depends on your GitHub plan/settings).
2. Upload `index.html` and `README.md` to the repository root.
3. In **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
4. GitHub will show the published URL under Settings → Pages.

GitHub Pages hosts the static frontend only. A production multi-user app needs a backend such as Supabase; never put database service-role keys or private records in frontend code or a public repository.
