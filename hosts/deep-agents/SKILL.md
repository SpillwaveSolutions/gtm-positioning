---
name: deep-agents-gtm-positioning
description: Bind LangChain Deep Agents to the gtm-positioning ContentPack. Isolation, identity, deterministic writes.
---

# Deep Agents / Spillwave GTM

Follow `docs/LANG_CHAIN_DEEP_AGENTS.md`.

1. Identity: `deep-agents/gtm-positioning`
2. Load this pack with `skills=["./path/to/gtm-positioning/skills/"]` or SkillsMiddleware.
3. Open an isolation session (`scripts/brain_session.py open --host deep-agents`) unless `SECOND_BRAIN_ROOT` already points at a session worktree.
4. Pack 2 hops, then write owned types only via `scripts/gtm_common.py write --author`.
5. Close the session to PR. Report path + SHA.
6. Never document a private remote. Never write raw Markdown into the tree.
