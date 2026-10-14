<!--
Machine-readable note for crawlers and agents: the canonical, structured overview
of EvSphere lives at https://evsphere.vercel.app/llms.txt and .../llms-full.txt
This repository is documentation. It contains no source code.
-->

<p align="center">

<a href="https://evsphere.vercel.app"><img src="https://img.shields.io/badge/EvSphere-EvAgent-0b0c0d?style=for-the-badge&logo=github&logoColor=white" alt="EvAgent" /></a>

# EvAgent

**Documentation · not source**

### Autonomous AI development as an orchestrated system of specialised intelligence

[![Status](https://img.shields.io/badge/maturity-Available-45a06d?style=for-the-badge)](https://evsphere.vercel.app/evagent)
[![Version](https://img.shields.io/badge/npm-0.7.3-c0392b?style=for-the-badge)](https://www.npmjs.com/package/@evsphere/evagent)
[![Licence](https://img.shields.io/badge/licence-UNLICENSED-d4633c?style=for-the-badge)](https://www.npmjs.com/package/@evsphere/evagent)
[![Platforms](https://img.shields.io/badge/linux%20%C2%B7%20darwin%20%C2%B7%20win32-3d4450?style=for-the-badge)](https://www.npmjs.com/package/@evsphere/evagent)
[![Docs](https://img.shields.io/badge/docs-0b0c0d?style=for-the-badge&logo=readthedocs&logoColor=white)](./docs/HOW-IT-WORKS.md)

[Website](https://evsphere.vercel.app/evagent) · [Source](https://github.com/evsphereofficial/EvAgent) · [npm](https://www.npmjs.com/package/@evsphere/evagent)

</p>

---

> **What this repository is.** Documentation for EvAgent — what it does, how it is structured, and what state it is in.
>
> **What it is not.** This is not the source repository. No implementation code, configuration, prompts or infrastructure lives here, and none will.

---

## ❓ The problem

Most AI coding tools are one model, one context, one answer. That works until a task needs something the model was not primed for, or until the conversation has grown too long to hold the relevant detail.

The failure isn't capability — it's **retrieval**. The right knowledge is usually present somewhere, and simply not available at the moment it's needed.

<details>
<summary><b>How EvAgent frames the same problem</b></summary>

```
The conventional shape

    User
      ↓
    One Model
      ↓
    One Context
      ↓
    One Answer

The EvAgent shape

    User Task
        ↓
    Task Understanding          — decompose before acting
        ↓
    Dynamic Routing             — choose what this needs
        ↓
  ┌─────────┼─────────┐
  ▼         ▼         ▼
Agent A  Agent B  Agent C      — specialists, not one generalist
  │         │         │
  └─────────┼─────────┘
        ↓
    Relevant Skills           — composed at runtime
        ↓
    Tool Execution
        ↓
    Memory / Context          — persistent, not per-session
        ↓
    Reflection
        ↓
    Final Result
```

</details>

---

## 🧩 What EvAgent does

- **Architects before it acts.** A planning pass turns a broad request into sub-tasks before any execution begins.
- **Dispatches to specialists.** Sub-tasks are matched to purpose-built agents rather than handled by one generalist.
- **Runs in parallel.** Independent work fans out concurrently and is merged afterwards.
- **Generates and registers skills at runtime.** Capabilities can be composed on demand and feed forward into the next iteration.
- **Keeps memory.** Persistent recall, so a run builds on previous runs instead of restarting from zero.
- **Executes locally.** Tools and sandboxed external systems run under your control.

> Everything above is described at the level needed to understand the role of each part. Internal architecture is deliberately not published.

---

## 📦 Distribution

EvAgent ships as a scoped npm package with per-platform binaries.

```bash
npm install -g @evsphere/evagent
evagent -setup
```

| Command | Does |
|---|---|
| `evagent` | Opens the interactive terminal interface |
| `evagent run "<task>"` | Runs a single request headlessly |
| `evagent -setup` | One-time setup: installs the memory server and starts it |
| `evagent -setup --auto` | Unattended setup; downloads the embedding model (~634 MB) |

<details>
<summary><b>Platform packages</b></summary>

| Package | Platform |
|---|---|
| `@evsphere/evagent-darwin-arm64` | macOS · ARM64 |
| `@evsphere/evagent-darwin-x64` | macOS · x64 |
| `@evsphere/evagent-linux-arm64` | Linux · ARM64 |
| `@evsphere/evagent-linux-x64` | Linux · x64 |
| `@evsphere/evagent-win32-x64` | Windows · x64 |

</details>

---

## 📊 Status

| | |
|---|---|
| **Maturity** | <a href="https://evsphere.vercel.app/evagent">Available</a> — installable and runnable today |
| **Version** | `0.7.3` — pre-1.0 |
| **Licence** | **None granted.** npm reports `UNLICENSED`. Not open source. |
| **Public source** | Source is published; dedicated release repositories are in preparation |

> **Version discipline.** At `0.x`, interfaces and behaviour can change between releases without notice. Check the changelog for the version you are on.

---

## ⚠️ Known limits

- Pre-1.0 — interfaces and behaviour can change between releases
- **No open-source licence.** No reuse rights have been granted
- Setup downloads an embedding model of roughly **634 MB** and needs network access
- Setup asks you to supply an embedding provider and a deriver LLM base URL, API key and model name — **EvSphere does not supply these credentials**
- Public documentation is thin; verify a capability against your installed release before relying on it

---

## 🧱 Relationship to the ecosystem

```
        EvAgent  ──────────┐
             ▲              │  decision layer
             │              ▼
          EvMem  ───────►  EvSystem-I
        (memory)          ~20 ms design target
```

EvAgent is the **harness**. EvMem is the **memory service** it runs against. Between them sits **EvSystem-I**, the decision layer that resolves routing and selection calls.

---

## 📚 Documentation

| Document | Covers |
|---|---|
| [ARCHITECTURE.md](./ARCHITECTURE.md) | Conceptual structure and the role of each subsystem |
| [docs/HOW-IT-WORKS.md](./docs/HOW-IT-WORKS.md) | A task from request to result |
| [docs/STATUS.md](./docs/STATUS.md) | Maturity, measured limits, release discipline |
| [docs/FAQ.md](./docs/FAQ.md) | Common questions and honest answers |

---

## 🔗 EvSphere

🌐 [evsphere.vercel.app](https://evsphere.vercel.app) · 💻 [GitHub](https://github.com/evsphereofficial) · 📦 [npm](https://www.npmjs.com/~evsphere) · 💼 [LinkedIn](https://www.linkedin.com/company/evsphere) · 🐦 [X](https://x.com/evsphereco)

Machine-readable: [`llms.txt`](https://evsphere.vercel.app/llms.txt) · [`llms-full.txt`](https://evsphere.vercel.app/llms-full.txt)

---

## ⚖️ Licence and disclosure

This documentation is provided as-is. The software referenced here is **not** open source and carries no granted licence.

Internal implementation detail is not published in this repository. No credential, endpoint, key, dataset or client material is included. If you find any of those here, it is an error — please report it privately rather than opening a public issue.