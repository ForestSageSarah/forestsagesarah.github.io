# Planned Upgrades (Zodiarks Embrace)

Future work only. Do not implement until the clean baseline is stable and deployed. Add one feature at a time behind a small PR, with a build check after each.

---

## 1. FAQ schema blocks

- Add JSON-LD FAQ schema for rich snippets.
- Render conditionally when a post includes `faq: true` (or similar) in front matter.
- Use an include (e.g. `_includes/faq-schema.html`) with a standard structure; no custom layout required at first.

---

## 2. Internal linking block component

- Enforce: every post links to at least 2 related posts where possible.
- Pillar posts link to cluster posts; cluster posts link back to pillar.
- Add a reusable block (e.g. “Related guides” / “See also”) that can be filled via front matter or a simple related-posts pattern.

---

## 3. Monetization (AdSense + affiliate)

- Integrate Google AdSense (client ID and ad slots in config or env).
- Add affiliate disclosure and optional affiliate links where appropriate.
- Keep implementation minimal (e.g. single include or layout addition) and behind config flags.

---

## 4. Performance pass

- Image compression (e.g. convert key images to WebP where appropriate).
- Lazy loading for images (native `loading="lazy"` or minimal JS).
- No new heavy scripts; keep Lighthouse targets (e.g. 90+ mobile, 95+ desktop) in mind.

---

## 5. Content templates

- **Job guides:** Template (front matter + structure) for job/role guides (e.g. White Mage leveling 2026).
- **Crafting guides:** Template for crafting and gathering guides.
- **Systems guides:** Template for systems content (deep dungeons, raids, etc.).
- Use a dedicated layout (e.g. `guide`) or a clear front-matter convention; avoid one-off custom layouts until patterns are stable.

---

## Constraints

- Do not add new features until the baseline build is green and the site is deployed.
- Each upgrade should be a small, reviewable change with a passing build (e.g. `bundle exec jekyll build` and any CI checks).
