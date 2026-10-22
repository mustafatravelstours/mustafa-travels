# Mustafa Travels — coordinated fix

1. In GitHub repository root, replace `umrah-builder.html`, `umrah-detail.js`, `umrah-public.js` with these files. Do NOT overwrite `supabase-config.js`.
2. Commit; wait for Vercel Ready; hard-refresh browser.
3. Admin → Umrah Builder → Edit existing package → enter final Single/Double/Triple/Quad/Quint adult rates plus child/infant rates → tick Publish → Save Package to Supabase. The form now stays open and saves sharing rates in the same action.
4. Confirm in Supabase Table Editor that `umrah_sharing_rates` has a row with matching `package_id`.
5. Open the public Umrah listing and detail page; check prices and all hotel stays.

IMPORTANT: For the public hotel stays to appear, the `umrah_public` view must include the `hotel_stays` column from `umrah_quotes`. If it does not, run this SQL to inspect the view first: `select pg_get_viewdef('public.umrah_public'::regclass, true);` and update the view carefully, preserving its published filter and excluding private costs. Do not grant public SELECT on private cost columns.

Brochure image still requires a valid HTTPS image URL. This patch does not add an image uploader or validate actual airline/hotel availability. Public rates are manually entered final selling prices, not inferred from the selected private room cost.
