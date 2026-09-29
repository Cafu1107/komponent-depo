---
version: 1
slug: "index-html"
primary_target: "index.html"
related_targets: []
---

# Surface brief: index.html (the app)

Scope: the whole single-page app (parts inventory, projects, sheets, command palette, labels). Mode: Operate.
Audience/job: makers tracking their electronic parts; add in seconds, find instantly, see low/out stock, plan projects, print drawer labels.
Constraints: single file, no dependencies/CDNs, localStorage data must migrate, EN/TR/DE text in sync.

## Direction contract

THESIS: The inventory is a bench instrument's front panel, not a web dashboard: ruled rows of labeled drawers, each count in fixed tabular slots and each stock state a lit indicator. It refuses the rainbow-gradient card dashboard with a hero-metric row.

OWN-WORLD: Graphite ground (#0f1012 dark, #f6f6f4 light), 1px ruled panels, one amber accent (#f2a93b) spent only on the primary action, selection and focus. Stock state = indicator LEDs (green/orange/red) with designed unlit ghosts. Categories = small desaturated swatches. System UI sans, tabular numerals, monospace only for location codes. Authored 1.5px-stroke SVG icons; no emoji.

STORY: The maker sees what is low at a glance, finds a part with / or Ctrl+K, adjusts counts at the bench, checks whether a project's parts are in stock and builds it, then prints QR labels for the drawers.

FIRST VIEWPORT: 56px top bar (mark + name, Parts/Projects tabs, Ctrl+K search trigger, cart count, settings, amber New part). One inline status strip of LED readouts (types, pieces, low, out, value; low/out filter). Category swatch chips, then a toolbar (search, stock filter, sort, grid/list, Select). Then the part grid.

FORM: owner-pinned "professional tool" direction (overrides the roll); seed key c77c7e34. Raise (seven-segment family): unlit states are designed; numerals never reflow; out-of-stock indicator blinks slowly like an unset 12:00. Raise (starship terminal): every location is a stenciled code tag, the same tag printed on QR labels.

Signature interaction: command palette (instant, keyboard-first) + count stepper whose LED changes state. Motion: 150-250ms ease-out; sheets slide with the drawer curve; view switch and theme change via View Transitions.

FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance
