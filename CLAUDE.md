# CLAUDE.md — refueler-multi-core
> **Version:** 1.0 | **Initialised:** CC-64 · 8 July 2026
> Load alongside `SESSIONS.md` at the start of every session on this repo.
> For platform-wide context, load the main `claude.md` + `Refueler_MasterContext_CC64.md`.

---

## What this repo is

`refueler-multi-core` is a BLAKE3-accelerated fork of esplora-electrs, optimised for ARM architecture and low-power hardware (Raspberry Pi, Umbrel, StartOS). It provides the Bitcoin indexing and streaming engine that underpins the Refueler platform's on-chain awareness.

**Local path:** `/Users/rajeshtaylor/Documents/refueler-multi-core/`
**GitHub:** `rajesh-taylor/refueler-multi-core` (public)
**Licence:** MIT (matches upstream esplora/electrs)

---

## Upstream lineage

| Project | Licence | Role |
|---|---|---|
| electrs | MIT | Electrum-compatible Bitcoin indexer |
| esplora | MIT | Block explorer and API layer |
| refueler-multi-core | MIT | BLAKE3-accelerated ARM fork of the above |

MIT licence chosen to match upstream — fork compatibility is clean.

---

## Locked decisions

- BLAKE3 replaces SHA256 for internal chunk verification and indexing — not for Bitcoin consensus (that remains unmodified).
- ARM/Raspberry Pi is the primary deployment target.
- Must not break compatibility with existing Electrum protocol clients.

---

## Session queue

See `SESSIONS.md`.

---

*"Nothing stops this train."*
