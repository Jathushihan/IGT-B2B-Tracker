# iGT B2B Hub — MVP preview

A responsive, single-page prototype for the AIESEC in Ruhuna Winter 26.27 B2B company workflow.

## Run it

Open index.html in a modern browser. No build tools are required.

## Demo features

- Switch between Member, TL, Manager, Specialist and LCVP preview roles.
- Members can submit companies and see their own demo records.
- Duplicate-name checks warn for existing companies. Previously rejected companies show the rejection reason.
- CRM review is available to non-member roles. Rejection requires a reason.
- TL preview is scoped to Team A. Manager, Specialist and LCVP previews show the organisation.
- Members can log calls only against CRM-approved companies.
- The side navigation can be collapsed to icons on desktop. Its preference is saved in the browser. On smaller screens it opens as a drawer.
- Synthetic sample records support workflow testing. Sample company, member and contact values are placeholders, and email addresses use the reserved .invalid domain.

## Data and privacy

The public demo contains synthetic sample records only. It does not contain records imported from the Team Jathushihan worksheet. The source workbook was not available in the editing workspace, so no worksheet records were added.

This is a front-end MVP, not production CRM software. Data is stored in the current browser's localStorage. The app has no real login, shared database, server-side authorization, audit-grade security or live multi-user sync. Role switching is a demo control, not authentication. The public GitHub Pages app is for synthetic test values only. Do not enter real company or personal contact information.

For a production system, connect Supabase Auth and PostgreSQL, enforce permissions with Row Level Security (RLS), and import only data that is approved for the intended users. Never put database service-role keys or private records in frontend code or a public repository.

## Deploy with GitHub Pages

1. In Settings → Pages, choose Deploy from a branch, select main and / (root), then Save.
2. GitHub will show the published URL under Settings → Pages.

GitHub Pages hosts the static frontend only. A production multi-user app needs a secure backend.
