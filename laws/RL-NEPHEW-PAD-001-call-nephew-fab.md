# RL-NEPHEW-PAD-001 — Call Nephew FAB

**Status:** cleared, 2026-10-08

## What it is

In-product Hello Nephew pad. Auto-mounts a Call Nephew FAB, or opens via ⌘-semicolon or any `[data-nephew-pad-open]` control. Text chat, product drive, voice, vision, Four Suits. Copilot modes: ask, plan, act. Default load shell is the Resident Agent.

## Where it lives

- Source: `scripts/apple/resources/family-office-kit/fo-nephew-pad.js` in marvelousempire/nephew
- Styles: `scripts/apple/resources/family-office-kit/fo-nephew-pad.css`
- Gitea projection: `deploy/gitea/custom/public/assets/js/fo-nephew-pad.js` (regenerate with `node scripts/sync-gitea-fo-kit-projection.mjs`)

## Rules

1. `window.FoNephewPad` is the public API. `window.NephewPadConfig` lets a host set apiBase, channel, defaultChips, detectSurface, onActDraft.
2. Session history is capped at 24 turns in sessionStorage.
3. The corner FAB was retired in Clinic 9958. Legacy `.fo-nephew-pad-fab` mounts are hidden by CSS. The floor Hello Nephew control (`#bc-floor-hello-nephew`) is the current opener.
4. Component id `briefcase.fab`, variant `fo-nephew-pad`.
5. It is a must-have: every Father console gets it by default.

## Relations

- operator-chrome-swap-bar (sibling)
- do-now-fab (sibling)
- fo-fab-stack (the mount point)
