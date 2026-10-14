<!-- Generated supporting document. -->

# EvAgent â€” Status and Limits

[â† Back to README](./README.md)

---

## Current state

| | |
|---|---|
| **Maturity** | **Available** |
| **Version** | 0.7.3 |
| **Public page** | [https://evsphere.vercel.app/evagent](https://evsphere.vercel.app/evagent) |
| **Machine-readable** | [llms.txt](https://evsphere.vercel.app/llms.txt) |

---

## What the maturity label means

| Label | Meaning |
|---|---|
| **Active** | An operating service or activity, running now. |
| **Available** | Usable by someone outside the team, under the stated conditions. |
| **Experimental** | A research prototype. Results are reported, not settled. |
| **In development** | Actively built. Capabilities can change without notice. |
| **Planned** | Intended direction, not implemented. |

EvAgent is currently **Available**.

---

## Known limits

- Version 0.x â€” interfaces and behaviour can change between releases
- Closed source. No open-source licence has been granted; npm reports UNLICENSED
- Setup downloads an embedding model of roughly 634 MB and needs network access
- Setup requires you to supply an embedding provider and deriver LLM credentials â€” EvSphere does not provide them
- Public documentation is thin; verify a capability against your installed release before relying on it

---

## What you need to run it

- Node.js 20 or newer
- An embedding provider for the memory service
- A deriver LLM base URL, API key and model name
- Roughly 700 MB of disk for the embedding model
- Network access during setup

---

## What is *not* claimed

- No accuracy, reliability or safety guarantee
- No user count, adoption figure or performance benchmark
- No endorsement, certification or independent review
- No timeline and no promise of a future release

EvAgent is not claimed to be finished, production-ready or commercially supported.

---

ðŸŒ [Website](https://evsphere.vercel.app) Â· [GitHub](https://github.com/evsphereofficial) Â· [npm](https://www.npmjs.com/~evsphere) Â· [LinkedIn](https://www.linkedin.com/company/evsphere) Â· [X](https://x.com/evsphereco)
