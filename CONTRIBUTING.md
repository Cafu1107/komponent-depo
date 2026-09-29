# Contributing to Komponent Depo

Thanks for helping. The app is one file, so contributing is simple.

## Reporting a bug or idea

Open an [issue](https://github.com/Cafu1107/komponent-depo/issues). For a bug, include:

- what you did, what you expected, what happened;
- browser and device (e.g. Chrome 130 on Windows, Safari on iPhone);
- the language and theme you were using.

Issues in Turkish, English or German are all fine.

## Changing the code

Everything lives in [`index.html`](index.html): HTML, CSS and vanilla JavaScript.

Ground rules:

1. **No dependencies.** No frameworks, CDNs or build step. The file must keep working when opened straight from disk.
2. **Don’t lose anyone’s inventory.** Parts are stored in `localStorage` (`komponent_depo`) and projects in `kd_projects`. If you change the data shape, extend `migrate()` / `migProj()` so old data still loads.
3. **Three languages.** Every visible string goes in `const I18N={en,tr,de}` with the same `{placeholders}` in all three. Singular forms use a `_1` key (e.g. `partsN_1`).
4. **Accessible and calm.** Keep keyboard access and visible focus, respect `prefers-reduced-motion`, and don’t animate keyboard-driven actions such as the command palette.

Test by opening `index.html` in a browser at desktop and phone widths, in both themes, and in at least two languages.

## Pull requests

Keep them focused on one change and describe what you tested. Screenshots help for anything visual.

By contributing you agree that your contribution is licensed under the [MIT License](LICENSE).
