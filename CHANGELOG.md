# Changelog

All notable changes to Komponent Depo. Dates are YYYY-MM-DD.

## [Unreleased]

## [2.0.0] - 2026-09-29

### Added
- **Command palette** (<kbd>Ctrl</kbd>/<kbd>⌘</kbd> <kbd>K</kbd>): jump to any part or project, filter, switch theme or language, print labels, back up.
- **Projects**: parts lists with need vs. have per part, coverage cells, “ready to build ×N”, and **Build ×1** that takes the parts out of stock (with undo). Shortages of planned projects appear in the shopping list.
- **Bulk selection**: select parts (Shift-click for ranges, Ctrl+A for all), then move, recategorize, favorite, print labels or delete them together.
- **QR labels**: A4 sheets, 3 × 7 (63.5 × 38.1 mm) with name, category, location code and a QR code that opens the part. The QR encoder is built in.
- Stock lights with designed unlit states, a 10-cell level bar, and “used in projects” on each part.
- Link parameters `tab` and `q`; the location field suggests existing locations.
- Backups now include projects (older array backups still import).

### Changed
- **New look**: calm graphite surface with one amber accent, authored SVG icons (no emoji), circuit-symbol category icons, new logo.
- Details, the part form, settings, the shopping list and projects open in side sheets (bottom sheets on phones).
- Motion: drawer-curve sheets, short stagger on filter changes, a theme switch reveal, grid/list crossfade; everything respects reduced motion. The command palette opens instantly.
- Phone layout: status strip as a grid, larger touch targets, no input zoom, safe-area aware.
- Photo suggestion tiles are real buttons with a loading shimmer; card photos keep their placeholder until loaded.

## [1.0.0] - 2026-09-28

First public version: parts with photos found by name, photo editor, shopping list, stock history, three languages.

[Unreleased]: https://github.com/Cafu1107/komponent-depo/compare/v2.0.0...HEAD
[2.0.0]: https://github.com/Cafu1107/komponent-depo/releases/tag/v2.0.0
[1.0.0]: https://github.com/Cafu1107/komponent-depo/commits/549b6d7
