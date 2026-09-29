# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Electronics hobbyists and makers who keep a personal stock of parts (microcontroller boards, sensors, resistors, LEDs, cables, tools). The public GitHub Pages site is the primary audience: anyone who finds the repo and wants a free inventory for their own workbench. They use it on a laptop at the desk and on a phone next to the drawers or while shopping for parts.

## Product Purpose

Know what you have, where it is, and what to buy. Success: a maker can add a part in seconds (typing the name is enough; the photo is found automatically), find it again instantly, and see at a glance what is low or out of stock before starting a project.

## Positioning

A zero-install, zero-account, single-file inventory that finds real photos of electronic parts by name (ESP32, HC-SR04, BC547) and keeps all data in the visitor's own browser.

## Operating Context

- Workbench use: counting parts while building, decrementing as parts are used.
- Planning: checking whether a project's parts are in stock before starting.
- Shopping: a generated list of what to reorder, with suggested quantities.
- Storage: parts live in drawers, boxes and shelves; the "location" field names them.
- Data portability: JSON backup/restore and CSV export for Excel.

## Capabilities and Constraints

- Single `index.html` (HTML + CSS + vanilla JS), no dependencies, frameworks, CDNs or build step. Served from GitHub Pages on `main`.
- Data lives in `localStorage` (`komponent_depo`); users have real inventories saved, so any data-shape change needs a migration (`migrate()`).
- UI text in English (default on the public site), Turkish and German via `I18N`; all three kept in sync.
- Photo search uses public APIs only: Wikimedia Commons, Wikipedia, Openverse. No API keys.
- Features: parts with category, quantity, alert threshold, location, package, price, link, notes, photo with crop/zoom/rotate editor; stock history; favorites; shopping list; search/filter/sort; grid/list views; dark/light theme; currencies TRY/USD/EUR/GBP.
- Planned in this update (user-confirmed): command palette (Ctrl+K), projects / bill of materials, bulk selection and editing, printable QR labels.

## Brand Commitments

- Name: "Komponent Depo" (English UI: "Component Vault"; German: "Bauteil-Lager").
- The owner explicitly allowed changing the logo and the visual identity; nothing from the current look is binding.
- Direction chosen by the owner: a professional tool look (calm dark surface, one accent color, fine lines, crisp typography, fast fluid motion) instead of the previous rainbow gradients.

## Evidence on Hand

- Real app and demo data (Arduino Uno R3, ESP32 DevKit, 10kΩ resistor, DHT22, HC-SR04, 5mm LED).
- Screenshots in `docs/`, banner `docs/banner.svg`, README in English with a Turkish section.
- No users, testimonials, download counts or benchmarks exist; do not invent them.

## Product Principles

1. Adding a part must take seconds; the name alone should be enough.
2. The inventory is the user's data: local-first, exportable, never lost to an update.
3. Show stock state (ok / low / out) before anything decorative.
4. Works equally at the desk and on a phone next to the drawers.
5. Stay one file anyone can download and open.

## Accessibility & Inclusion

Keyboard operable throughout (shortcuts, command palette, focus management in overlays), visible focus, WCAG AA contrast in both themes, `prefers-reduced-motion` respected. Three UI languages.
