---
name: cursor-gtm-positioning
description: Bind a Cursor agent (including Grok Bot cloud sessions) to the gtm-positioning ContentPack.
---

# Cursor / gtm-positioning

Follow `docs/CURSOR.md` and `docs/GROK_BOT.md`.

1. Identity: `grok-bot/gtm-positioning` (or the operator-registered actor for this role).
2. Local Cursor may `/plugin install gtm-positioning` from the Spillwave marketplace.
3. Cloud Cursor on a knowledge tree: pack first, write only via pack scripts, isolate with `brain_session.py`.
4. Never document a private remote. Never write raw Markdown into the tree.
