# Miss Crunch — GitHub source migration

**Status:** Migration staging only. The original running Miss Crunch website source has **not** been imported yet. This repository must **not** be connected to the public Vercel production domain until a complete source tree and successful build are verified.

## Why this repository exists
Move the existing Miss Crunch site under version control so future Shop, Saturday Specials, Cocina, delivery and ordering updates can deploy safely without rebuilding the website.

The GitHub repository was newly created and empty on 14 October 2026. The inspected Vercel project `miss-crunch` uses a source-upload (`drop`) deployment rather than a connected Git repository. Its source-file API truncates larger files, so the available connector response **does not supply a complete recoverable codebase**. A separate Vercel project serves `misscrunch.vercel.app` and requires authorization to read/reconnect. The uploaded screenshots and product assets do not substitute for full source code.

## Approved Shop changes (pending source import)
- Show Hallacas on the main Shop page at **70,000 COP**, while keeping the existing Saturdays entry.
- Show Empanadas Árabes on the main Shop page at **70,000 COP**, while keeping the existing Saturdays entry.
- Reuse both Saturday product identities, stock IDs, pack sizes and preparation information: **do not create duplicate inventory or invent quantities**.
- Use the seven user-supplied real Empanadas Árabes photos; five optimized WebP selections are prepared in the attached transfer kit. Do not substitute AI photography.
- Make sure search/categories, add-to-cart totals and WhatsApp handoff use the Shop price and current unit quantity.
- Preserve the established Miss Crunch design, Cocina, delivery calculations, existing routes and ordering flows.

The implementation manifest is in [migration/catalogue-additions.json](migration/catalogue-additions.json). It is **not an importable source-code patch**; adapt only after reviewing the real product TypeScript schema and Saturday listing implementation.

## Release safeguards
1. Obtain the complete existing Miss Crunch source ZIP/export from the website builder or a complete authorized production Vercel export.
2. Import its source, assets, package manifest and lockfile into this repo; exclude `.env*` secrets, `node_modules`, build output, private credentials and production customer information.
3. Compare current Saturday product data to the two manifest entries, use the same SKUs and confirmed pack sizes, and integrate the five user-approved WebP images.
4. Build and test full site, Shop cart, WhatsApp checkout, Saturdays, Cocina and responsive pages in preview.
5. Link **the intended production site** to this GitHub repository only after the preview passes and the current domain/project is positively identified. Production should not be redirected to an incomplete project.

Current prepared transfer kit: `miss_crunch_shop_catalogue_update_assets.zip` (shared in the ChatGPT conversation). Photos are **not yet present in this GitHub repository**; its source ZIP must be imported before production deployment.
