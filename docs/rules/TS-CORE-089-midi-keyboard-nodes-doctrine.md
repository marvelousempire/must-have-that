# TS-CORE-089 — MIDI Keyboard Nodes Doctrine

**Status:** ACTIVE
**Owner:** ACT v2 / Motif / That App Studio
**Date:** 2026-10-07
**Provenance:** This conversation (A BROWN SANTA + Grok), 2026-10-07. Spoken doctrine, now written as agent instructions.

---

## 1. The core idea

Every micro-slice is its own **node** — a key on a MIDI keyboard. You push it in, you pull it out. The whole scale is the system. No node is permanently wired; every node is swappable.

## 2. Stationary code, swappable tokens

The bash code is **stationary** — it does not change. What changes are the **tokens**. The tokens are the nouns: the product name, the vendor, the logo path, the color, the slug. The stationary bash reads the tokens from the manifest and applies them.

This is the Quick Server rebirth pattern restored: one script, many manifests. The script is the piano. The manifests are the notes.

## 3. The noun-verb split

- **Motif** handles the nouns. Motif is the lens that carries color, spacing, shape, density, typography, motion — the visual and identity tokens. Motif is the noun authority.
- **That App Studio** handles the verbs. That App Studio identifies which app performs the verb (TS-CORE-082) and routes the action. That App Studio is the verb authority.

Nouns live in Motif. Verbs live in That App Studio. The MIDI keyboard nodes are where they meet: stationary bash code that reads noun-tokens from Motif and executes verb-actions from That App Studio.

## 4. The short codes

The short codes offered in the system are the nouns. They are the tokens the stationary bash swaps. A short code is not a command — it is a value. The command is the verb. The short code fills the slot.

## 5. Related rules

- TS-CORE-083: Bash-first microservice doctrine.
- TS-CORE-082: That App Studio verb-trigger doctrine.
- TS-CORE-088: Skeleton Closet cabinet and control center doctrine.
