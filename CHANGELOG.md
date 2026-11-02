# Changelog

User-visible changes to TeXEq. TeXEq is closed-source; this file tracks releases, not commits.

## 2.2.15 — 2026-11-02

- New **Feedback & Suggestions** entry in the app (bug report, feature request or other), with optional contact information and automatic version / system details.
- Fixed: license, update and permission dialogs could open behind the editor window.
- Improved: keyboard focus and text input in dialog windows.
- Includes the fixes shipped in earlier 2.2.x builds: Word insertion and double-click reliability, license compatibility with older licenses, transparent backgrounds for colored equations, and faster double-click response.

## 2.2.11 — 2026-11-02

- Word: fixed insertion being interrupted by click capture; inline, display and numbered insertion restored.
- Ribbon finalized: PowerPoint — Insert Equation / Inline Equation; Word — Inline / Display / Numbered.
- Colored equations: removed the white background from SVG output.
- Double-click speed-up: single-macro fast path with automatic fallback.
- License: existing licenses issued under the previous product name are recognized again.

## 2.2.1 — 2026-11-02

- New domain `texeq.rancholab.cn` for the website, downloads and version API.
- PowerPoint: double-click editing, inline equations and update progress fixes.
- Upgrades keep the existing license; no reactivation required.

## 2.2.0 — 2026-11-02

- Rebranded to **TeXEq** across the app, Office ribbon, installer and website.
- The installer removes the previous app; existing account and license are preserved.

## 2.1.0 — 2026-11-01

- Redesigned editor: live preview, LaTeX source, formula library and symbol panel in one window.
- Built-in symbol dictionary with 689 entries in 29 categories, searchable and insertable.
- Editing keeps the original equation's size and font scale.
- Automatic update check with download progress and restart.

## 2.0.x — 2026-11-01

- 7-day full-feature trial and license activation; no Keychain prompts.
- Faster double-click response (about 1.8 s → 0.6 s).
- Automatic update checks.

## 1.x — earlier

- PowerPoint add-in prototype, double-click gateway, Word template and bridge.
- SVG output for PowerPoint equations and legacy equation conversion.
