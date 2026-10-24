# Hotel photos via Google Drive

1. In Google Drive, open the hotel image, choose Share > General access > Anyone with the link > Viewer.
2. Open Admin > Umrah Package & Brochure Builder and edit the package.
3. Under each Hotel Stay, paste one Google Drive photo sharing URL per line in **Hotel Photo Links**.
4. The first URL becomes the large hotel card image; additional URLs appear as clickable thumbnails.
5. Save Package to Supabase and open the public package detail page.

The photos are stored as URL strings inside the existing `hotel_stays` JSON data, not as files. No database migration is needed if `hotel_stays` is a JSON/JSONB column.

**Caution:** Google Drive does not guarantee hotlinking; images may fail despite public sharing. Use stable public image hosting (e.g. Supabase Storage) for production if this occurs. Existing package pricing, dates and room calculations are untouched.
