# Miss Crunch — website source migration

The owner supplied a 27 MB `miss-crunch.zip`, containing the existing Next.js website. It has now been recovered and updated locally with Hallacas and Empanadas Árabes in the main Shop and Saturdays section, both at **70,000 COP**.

**GitHub status:** The updated complete source export `miss-crunch-github-ready-2026-10-14.zip` was successfully created in ChatGPT on October 14, 2026. **The full 124-file source tree has not yet been pushed to this repository**. The current repository contains only migration records, not a deployable site. Do not connect this repository to the existing production Vercel project before the complete tree is imported and its build is verified.

## Verified recovered-source facts

- Original Saturday Hallacas are **10 units per package**.
- Arabic-style empanada package quantity has **not been verified**; display only “per package” until confirmed.
- Pasteles remain **85,000 COP**; their price was not changed.
- Main Shop and Saturday price data reference the same `saturdayPrices` constants in the prepared source.
- Five real user-provided Empanadas Árabes photographs are included.
- The restored source also retains Cocina, cart, delivery calculations and original photography/video.

## Migration instructions

1. Obtain the finished `miss-crunch-github-ready-2026-10-14.zip` from the ChatGPT conversation, unzip locally.
2. Copy its **contents** (not the ZIP as a single file) into a clone of `connectnarrative/miss-crunch`, preserving `.git` from the clone.
3. Commit and push to `main`. The ZIP includes `docs/GITHUB-TRANSFER.md` and `docs/SPECIALS-SHOP-RELEASE.md`.
4. Run `npm ci && npm run build`, then preview the Shop, Saturday reservation, cart and WhatsApp handoff.
5. Identify and compare the intended existing live website before connecting the GitHub repo to Vercel. Previous Vercel builds used direct source uploads and may differ from this recovered source.

The connected GitHub write tool supports commits and text/blob writes but cannot ingest the local binary ZIP or source directory directly from this working container. No production alias has been changed.

## October 14 pricing correction and domain

- **Hallacas:** 70,000 COP per 10-pack.
- **Empanadas Árabes:** **35,000 COP** per package (physical count still needs confirmation).
- **Pasteles:** 85,000 COP per 10-pack (unchanged).
- **Canonical production URL:** https://misscrunch.vercel.app/ (no hyphen).
- **Exact existing Vercel project:** `miss_crunch_vercel_website` / `prj_44zv4ruGCozopem0gLyprs8rdvRx`.
- **Complete updated source prepared:** `miss-crunch-github-ready-2026-10-14-35k.zip`, including `scripts/push-to-github.sh` to import the full files after extracting on the owner's computer.
- **GitHub repo is not yet deployable** until the complete extracted source is pushed. Do not link a partial repository to production.
