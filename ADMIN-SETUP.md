# Mustafa Travels Admin — setup

1. Supabase: verify the previously exposed `sb_secret_` key has been revoked.
2. Open `supabase-config.js`. Replace `PASTE_YOUR_SUPABASE_PROJECT_URL_HERE` with the **exact** Project URL shown under Supabase Project Overview / Connect, including `https://`.
3. Upload the updated `admin.html` and `supabase-config.js` to the **root** of your GitHub repository. Vercel should redeploy automatically.
4. Visit `https://YOUR-VERCEL-DOMAIN/admin.html` (not `/admin` unless routing is configured). Sign in with the email/password for the user you added to `public.admin_users`.
5. Admin role is checked against Supabase `admin_users`; table RLS controls writes. Test login, add a draft package, and refresh.
6. Remove old Admin Demo links from your published pages. `index.html` in this ZIP has the navigation link removed. Update the other pages as needed.
7. A published row is **stored in Supabase**, but public `umrah.html` and `blog.html` still use their original static content. Connecting the public pages is the next phase.

Never put `sb_secret_`, service_role keys, or database passwords into GitHub or HTML. Keep RLS enabled. Publishable keys are designed for browser use. This is a functional starter admin; verify RLS and user authorization before using real customer data. Automatic translation, file uploads, and flight management are not implemented in this version.
