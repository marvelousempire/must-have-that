# Bash Conversion Backlog — Notification

**Status:** OPEN
**Owner:** ACT v2
**Date:** 2026-10-07
**Provenance:** This conversation (A BROWN SANTA + Grok), 2026-10-07.

---

## The notification

> **bash conversion pending** — Nothing in this system has been built in bash yet. All existing micro-slices are Node ports. Per TS-CORE-083, bash is the default implementation language. Every Node micro-slice must be revisited and converted to bash when the app is visited. This notification surfaces on every visit until the backlog is empty.

## The backlog

| # | Node artifact | Bash target | Status |
|---|--------------|-------------|--------|
| 1 | skeleton-closet.mjs (registry reader) | skeleton-closet.sh | OPEN |
| 2 | wordpress-plugin-processor.mjs | covered by skeleton-closet-rebirth.sh (canonical bash exists) | PARTIAL |
| 3 | gitea-customize-executor.mjs | gitea-customize.sh (canonical bash exists in nephew) | PARTIAL |
| 4 | generate-rebirth-bash.mjs (generator) | N/A — generator produces bash | N/A |
| 5 | ComfyUI bootstrap wiring | comfyui-bootstrap.sh | OPEN |

## The rule

Per TS-CORE-083: bash is the spine. Node ports are convenience wrappers. The canonical source of truth is always the bash version. This backlog tracks the conversion of every Node artifact into its bash canonical form.

When a bash canonical exists (items 2 and 3), the Node port is demoted to a wrapper. When no bash canonical exists (items 1 and 5), one must be written before the Node port is considered complete.
