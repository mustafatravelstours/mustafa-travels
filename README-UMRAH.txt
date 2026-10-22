MUSTAFA TRAVELS UMRAH BUILDER UPGRADE

1. Supabase SQL Editor: Run UMRAH-BUILDER-SQL.sql ONCE (in the same project).
2. GitHub root: upload/replace admin.html and umrah.html, and upload NEW umrah-builder.html and umrah-public.js.
3. DO NOT replace your existing supabase-config.js. Keep your working URL and publishable key.
4. Wait for Vercel Ready. Open /admin.html, log in, click "Umrah Brochure Builder".
5. Enter hotels, distances, shuttle, costs and markup. The calculator shows total and per person.
6. Save draft, edit, preview, print/save PDF, then publish. Public /umrah.html displays brochure cards.
7. Costs are stored in umrah_quotes with admin-only RLS. Public reads umrah_public, which has NO internal costs.
8. Hotel names are free-text in this version, not a live hotel API. Image is HTTPS URL, not upload.
9. Brochure print uses your browser Print > Save as PDF. No PDF file is generated on server.
10. Existing old Umrah packages are not migrated automatically; they remain in umrah_packages.
11. Existing site_entries Umrah cards still appear on Umrah page if published. Manage them in Website Pages & Photography tab.
12. Never put sb_secret keys in public files.
