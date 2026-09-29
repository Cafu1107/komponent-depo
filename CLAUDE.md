# Komponent Depo

Electronic-parts inventory app. Everything lives in one `index.html` (HTML + CSS + vanilla JS) with **zero dependencies and no build step**. Data is stored in the browser's `localStorage`. Served from GitHub Pages on `main`.

## Rules

- Keep it a single file with no dependencies, frameworks or CDNs.
- Never change the `localStorage` data shape without a migration: users have real inventories saved. Old category names are mapped via `OLDCAT`.
- UI text goes in `const I18N={tr,en,de}` in all three languages, with identical `{placeholders}`. Category labels also need `CAT_EN`. Check with the `i18n-check` skill (`node ~/.claude/skills/i18n-check/check-komponent.mjs index.html`).
- Test by opening `index.html` in a browser at desktop and phone widths, in both themes.
- README is English first with a Turkish section. Screenshots live in `docs/`.
- The owner reads Turkish, so explain changes to them in Turkish. Commit identity: `Cafu1107 <179776180+Cafu1107@users.noreply.github.com>`.
