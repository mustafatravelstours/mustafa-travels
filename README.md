# Mustafa Travels & Tours S.L. — website starter

This is the **first deployable static website milestone**, adapted from the supplied travel agency HTML concept. It is **not** a finished booking platform.

## Preview
Open `index.html` locally or serve this directory with `python -m http.server 8000` and visit `http://localhost:8000`.

## Publish safely
1. Create a **new private GitHub repository** (do not upload credentials).
2. Upload the contents of this folder to the repository root.
3. Import the GitHub repository into Vercel, select **Other** framework, leave build command empty, and set output directory to `.`.
4. Use the generated Vercel preview URL for testing. **Do not change GoDaddy DNS** until all pages are approved.
5. Later, add `mustafatravels.com` as a custom domain in Vercel and follow its exact DNS instructions in GoDaddy; verify before switching.

## Status / limitations
- Landing page, standalone services pages, travel journal and admin **UI preview** included.
- Flight search is **not connected to Travelport**; do not collect card payments or claim live ticket availability.
- Admin is **not authenticated or persistent**. Never use its preview for private business data.
- Blog language options are hand-authored samples, **not automatic translation**.
- Background slides are still images, **not licensed video assets**.
- External images/fonts require network access; replace with appropriately licensed local assets before production.
- Review every sample package, hotel, testimonial, rating, price, contact detail and legal claim before launch.

## Next development milestone
Build authenticated CMS (e.g. Supabase Auth + database + storage), editable packages/blogs, multilingual publication workflow, and then Travelport integration with a server-side backend. API keys must never be embedded in frontend code.
