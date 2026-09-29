---
name: Komponent Depo
description: Inventory for electronic parts, drawn as a bench instrument's front panel.
colors:
  graphite-ground: "#0f1012"
  graphite-panel: "#141517"
  graphite-surface: "#17181b"
  graphite-raised: "#1f2024"
  graphite-step: "#2a2b30"
  ink: "#ececee"
  ink-muted: "#a8a8b0"
  ink-faint: "#8f8f99"
  solder-amber: "#f2a93b"
  solder-amber-hover: "#ffbb55"
  solder-amber-ink: "#1c1304"
  led-green: "#3ecf8e"
  led-orange: "#f28c3b"
  led-red: "#f0506e"
  paper-ground: "#f6f6f4"
  paper-panel: "#fcfcfb"
  paper-surface: "#ffffff"
  paper-raised: "#f0f0ec"
  paper-ink: "#17171a"
  paper-ink-muted: "#51515a"
  paper-ink-faint: "#6c6c75"
  paper-amber-text: "#955b00"
typography:
  headline:
    fontFamily: "Segoe UI Variable Text, Segoe UI, system-ui, -apple-system, SF Pro Text, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "22px"
    fontWeight: 650
    lineHeight: 1.2
    letterSpacing: "-0.02em"
  title:
    fontFamily: "Segoe UI Variable Text, Segoe UI, system-ui, -apple-system, SF Pro Text, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "15px"
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Segoe UI Variable Text, Segoe UI, system-ui, -apple-system, SF Pro Text, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "Segoe UI Variable Text, Segoe UI, system-ui, -apple-system, SF Pro Text, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "12.5px"
    fontWeight: 550
    lineHeight: 1.4
  readout:
    fontFamily: "Segoe UI Variable Text, Segoe UI, system-ui, -apple-system, SF Pro Text, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "17px"
    fontWeight: 650
    letterSpacing: "-0.02em"
    fontFeature: "tnum"
  code-tag:
    fontFamily: "ui-monospace, Cascadia Mono, SF Mono, Consolas, Liberation Mono, monospace"
    fontSize: "10.5px"
    fontWeight: 600
    letterSpacing: "0.04em"
rounded:
  sm: "6px"
  md: "9px"
  lg: "13px"
spacing:
  xs: "6px"
  sm: "8px"
  md: "12px"
  lg: "16px"
  xl: "20px"
components:
  button-primary:
    backgroundColor: "{colors.solder-amber}"
    textColor: "{colors.solder-amber-ink}"
    rounded: "{rounded.md}"
    height: "34px"
    padding: "0 12px"
  button-primary-hover:
    backgroundColor: "{colors.solder-amber-hover}"
  button-secondary:
    backgroundColor: "{colors.graphite-surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
    height: "34px"
    padding: "0 12px"
  button-secondary-hover:
    backgroundColor: "{colors.graphite-raised}"
  input:
    backgroundColor: "{colors.graphite-surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
    height: "34px"
    padding: "0 10px"
  chip:
    textColor: "{colors.ink-muted}"
    rounded: "{rounded.md}"
    height: "30px"
    padding: "0 10px"
  chip-selected:
    backgroundColor: "{colors.graphite-raised}"
    textColor: "{colors.ink}"
  part-card:
    backgroundColor: "{colors.graphite-surface}"
    rounded: "{rounded.lg}"
  code-tag:
    backgroundColor: "{colors.graphite-raised}"
    textColor: "{colors.ink-muted}"
    typography: "{typography.code-tag}"
    rounded: "4px"
    padding: "3px 5px"
  sheet:
    backgroundColor: "{colors.graphite-panel}"
    width: "560px"
---

# Design System: Komponent Depo

## Overview

**Creative North Star: "The Bench Instrument"**

Komponent Depo is drawn as the front panel of a piece of bench equipment, not as a web dashboard. The inventory reads as ruled rows of labeled drawers: every count sits in fixed tabular slots, and every stock state is a small indicator light. Unlit states are designed too. A drawer with nothing in it shows a ghost cell, not an empty space.

The surface is calm graphite with fine one-pixel rules and a single warm accent, solder amber, spent only on the primary action, the current selection and keyboard focus. Photos of real parts carry all the color that isn't signal. Density is that of a tool the maker keeps open all day: compact controls (34px), system type, no decoration that doesn't report state.

Motion is fast and functional. Panels slide in with a drawer curve, results settle with a short stagger when the filter changes, and an out-of-stock light blinks slowly like an unset clock. Anything the keyboard triggers, such as the command palette, appears instantly.

**Key Characteristics:**
- Graphite ground, 1px ruled panels, one amber accent.
- Stock state as indicator lights (green / orange / red) with designed unlit ghosts.
- Tabular numerals everywhere a count appears; monospace only for location codes.
- Authored 1.5px-stroke line icons; circuit-symbol icons for categories.
- Dark and light themes share the same structure; light swaps graphite for paper.

## Colors

Neutral graphite (or paper in light theme) with one warm accent and three signal colors that mean only stock state.

### Primary
- **Solder Amber** (`solder-amber`): the primary button (New part, Add, Build), the selected-part outline and checkbox, the active tab underline, the text caret, focus rings and text selection. In light theme, amber text uses the darker `paper-amber-text` for contrast.

### Tertiary
- **LED Green / LED Orange / LED Red** (`led-green`, `led-orange`, `led-red`): stock state only (in stock, low, out). They light the indicator dots, the 10-cell level bar and project coverage cells. Never used for decoration or buttons, except red for destructive text.

### Neutral
- **Graphite Ground** (`graphite-ground`): page background, dark theme.
- **Graphite Panel / Surface / Raised / Step** (`graphite-panel` → `graphite-step`): sheets and status strip, cards and inputs, hover and pressed fills, the scrollbar thumb. Depth is carried by these steps.
- **Ink / Ink Muted / Ink Faint** (`ink`, `ink-muted`, `ink-faint`): primary text, secondary labels, meta and placeholders. Ink Faint holds at least 4.5:1 on Graphite Raised.
- **Paper** (`paper-*`): the same roles in the light theme.
- **Category swatches**: twelve desaturated hues (e.g. capacitor #5fb3c9, resistor #c9955f, module #6f95d9) appear only as 8px squares, the category distribution bar and a faint tint behind an empty photo slot.

### Named Rules
**The One Amber Rule.** Amber marks what you can act on next or what is selected. If it is neither, it isn't amber.

**The Signal Colors Rule.** Green, orange and red mean stock state. They are never used as brand color, decoration or chart palette.

## Typography

**Body Font:** Segoe UI Variable Text (system stack, with SF Pro Text, Roboto, Helvetica Neue, Arial)
**Label/Mono Font:** ui-monospace (Cascadia Mono, SF Mono, Consolas), for location codes and key caps only

**Character:** One workhorse system sans carries every role; hierarchy comes from weight (400 / 550 / 600 / 650) and small size steps. Numbers are tabular so counts never jiggle.

### Hierarchy
- **Headline** (650, 22px, 1.2, -0.02em): view titles such as Projects.
- **Title** (600, 14.5–15.5px, 1.3): part names on cards, sheet titles.
- **Readout** (650, 17px, tabular): status-strip values and the quantity stepper.
- **Body** (400, 14px, 1.5): descriptions and notes, max about 65ch.
- **Label** (550, 12–12.5px): field labels, meta lines, section labels in sheets.
- **Code tag** (mono 600, 10.5px, +0.04em, uppercase): location codes such as SHELF 1, identical on screen and on printed labels.

### Named Rules
**The Tabular Rule.** Every count, price and readout uses tabular numerals; digits never shift width as they change.

## Layout

A 1280px centered column with 16px gutters (safe-area aware). The parts view stacks: status strip, category chips with a proportional 4px distribution bar, toolbar (search, stock filter, sort, grid/list switch, Select), then the grid. Cards auto-fill at a 228px minimum with 12px gaps. List view becomes one ruled table. Below 640px: two columns of 158px cards, the status strip becomes a 3-column grid, sheets become bottom sheets (full width, 16px top radius, drag handle), header actions collapse to icons.

Spacing follows a small rhythm of 6, 8, 12, 16 and 20px; more space sits above a section label than below it.

## Elevation & Depth

Flat by default. Depth comes from tonal steps (ground → panel → surface → raised) and 1px rules at 7%, 11% and 20% white (8/13/24% ink in light). Shadows appear only on floating layers: sheets, the command palette, the bulk bar and toasts.

### Shadow Vocabulary
- **Floating** (`0 28px 70px -18px rgba(0,0,0,.75), 0 4px 12px -4px rgba(0,0,0,.4)`): sheet, palette, bulk bar, toast.
- **Raised** (`0 14px 32px -14px rgba(0,0,0,.7), 0 2px 6px -2px rgba(0,0,0,.45)`): the project picker dropdown.

### Named Rules
**The Flat Panel Rule.** Cards don't lift on hover; their rule brightens. Only layers that float above the page cast a shadow.

## Shapes

Softly squared corners in three steps: 6px for small controls and tags, 9px for buttons, inputs and chips, 13px for cards and panels. Location codes are 4px-radius outlined tags. Stock lights are 7–8px circles with a highlight and 1px rim; level bars are ten 1px-radius cells.

## Components

### Buttons
- **Shape:** gently squared (9px), 34px tall (30px small).
- **Primary:** amber fill, dark ink, 1px inner highlight; one per view.
- **Secondary:** graphite surface with a 1px rule; hover steps to raised and brightens the rule.
- **Ghost / Danger:** transparent; danger text is LED red and fills faintly red on hover.
- **Press:** scale 0.97 over 100ms on every pressable; hover styles only on fine pointers.

### Chips
- **Style:** transparent with a 1px rule, 8px category swatch, count in faint ink.
- **State:** selected chips fill with graphite raised and full ink.

### Cards / Containers
- **Corner Style:** 13px.
- **Background:** graphite surface with a 1px rule; the photo slot is 4:3 with a white (or dark) backdrop once the photo loads.
- **Overlay:** a translucent state tag (light + label) top-left, a favorite star top-right.
- **Footer:** quantity stepper and quiet icon actions; a 10-cell level bar sits above.

### Inputs / Fields
- **Style:** graphite surface, 1px rule, 9px radius, 34px tall; 16px text on touch devices.
- **Focus:** amber-tinted border plus a 3px soft amber ring.

### Navigation
- **Top bar:** 56px, translucent graphite with blur, logo mark + name, Parts / Projects tabs with an amber underline that slides between them, a command-palette trigger showing its shortcut, icon actions, the amber New button.

### Quantity Stepper (signature)
Minus / count / plus in one ruled capsule. Holding a button repeats and accelerates; Shift steps by 10. The count changes instantly; the stock light and level bar react, and a light that changes state pops once.

### Command Palette (signature)
Centered at 14vh, 620px wide, grouped results (parts, projects, commands) with stock lights and code tags. Opens and closes with no animation.

## Do's and Don'ts

### Do:
- **Do** keep amber for the primary action, selection and focus only.
- **Do** show stock state with the indicator light and level cells, including their unlit ghost state.
- **Do** use tabular numerals for every count and price.
- **Do** use the authored line-icon set (1.5–1.6px stroke) and circuit-symbol category icons.
- **Do** slide sheets with the drawer curve `cubic-bezier(0.32,0.72,0,1)` and keep other UI motion at 150–250ms ease-out.
- **Do** gate hover styles behind `(hover:hover) and (pointer:fine)` and respect reduced motion.

### Don't:
- **Don't** use emoji or Unicode glyphs as icons.
- **Don't** lift cards on hover or give resting surfaces shadows.
- **Don't** put glowing halos around the stock lights; they are lit by a highlight and a rim.
- **Don't** use gradient text, rainbow gradients or a second accent color.
- **Don't** animate the command palette or other keyboard-triggered actions.
- **Don't** mark selection with a thick colored stripe on one side of a row; outline it.
