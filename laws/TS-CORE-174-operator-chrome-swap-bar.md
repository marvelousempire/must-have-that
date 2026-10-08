# TS-CORE-174 — Operator chrome swap bar

**Status:** cleared, 2026-10-08

## What it is

A fixed bottom-right pill that swaps between the front site and wp-admin without signing in. On the front it shows Admin. On admin it shows View site. Guests get Sign in plus Admin. It hides the default WordPress admin bar so the pill is the only operator contract.

## Where it lives

- Source: `deploy/wp-shared/wp-family-door/includes/operator-chrome.php` in marvelousempire/nephew
- Copied into: `deploy/wp-single/wp-content/plugins/wp-family-door/` and `deploy/wp-multisite/wp-content/plugins/wp-family-door/`
- Test: `test/nephew-one-wordpress-admin.test.mjs`

## Rules

1. Renders only for logged-in users who can edit posts or manage options.
2. Multisite-safe: network admin gets network URLs.
3. The `nephew_operator_chrome_enabled` filter can disable it per surface.
4. Styles are inlined — no asset pipeline on lean factory stacks.
5. It is a must-have: every WordPress build gets it by default.

## Relations

- do-now-fab (sibling in the operator chrome family)
- call-nephew-fab (sibling in the operator chrome family)
- fleet-hud-card-toggle (the card's own front/admin toggle follows this pattern)
