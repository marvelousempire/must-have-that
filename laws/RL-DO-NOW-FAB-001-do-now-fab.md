# RL-DO-NOW-FAB-001 — DO-NOW Security FAB

**Status:** cleared, 2026-10-08

## What it is

An alert-bell FAB that mounts into the fo-fab-stack on every Father projection. Visible only while a DO-NOW lock is active. Opens the do-now-security cassette desk.

## Where it lives

- Source: `scripts/apple/resources/family-office-kit/fo-do-now-fab.js` in marvelousempire/nephew
- Styles: `scripts/apple/resources/family-office-kit/fo-do-now-fab.css`
- Rule: `.claude/rules/do-now-security-cassette-fab.md`

## Rules

1. Polls same-origin `/api/v1/do-now` and `/api/do-now` every 20 seconds.
2. A 404 from every same-origin endpoint latches feature-absent. Transient failures do not latch.
3. Security locks pulse red. Order locks pulse amber.
4. Click opens the desk with CTAs. No long-press.
5. Component id `briefcase.fab`, variant `do-now-security`.
6. It is a must-have: every Father console gets it by default.

## Relations

- operator-chrome-swap-bar (sibling)
- call-nephew-fab (sibling)
- fo-fab-stack (the mount point)
