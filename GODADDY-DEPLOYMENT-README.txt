MUSTAFA TRAVELS — DEPLOYMENT GUIDE

This is a complete static site built from the supplied GitHub ZIP, with the premium Umrah detail files merged.

RECOMMENDED (keep Vercel hosting; use GoDaddy only for the domain):
1. Back up your existing GoDaddy website and DNS records. Do not remove existing MX/email records.
2. Upload the files in this ZIP to your GitHub repository root (not a nested folder). Commit.
3. Wait for Vercel deployment Ready and test https://mustafa-travels.vercel.app/umrah.html and a published package detail.
4. Vercel > Project > Settings > Domains > Add mustafatravels.com and www.mustafatravels.com.
5. Follow the EXACT DNS records shown by Vercel in GoDaddy DNS Management. Do not guess DNS targets.
6. Verify HTTPS and all pages, and only then switch production traffic.

ALTERNATIVE (GoDaddy cPanel static hosting):
Upload contents of this folder into public_html (NOT the enclosing folder). Back up existing public_html first. Confirm your GoDaddy plan supports file hosting; Website Builder-only plans may not support direct HTML uploads.

IMPORTANT: This site uses browser-side Supabase and external CDN assets; Supabase RLS must remain enabled. NEVER upload sb_secret keys to website files. The publishable key and project URL are in supabase-config.js. Real-time inventory/checkout are not integrated. Hero and stay photos use Unsplash URLs and require internet; replace with licensed brand assets before final launch. Some legacy sections of the supplied site may still contain demo content. Test thoroughly before public launch.
