<!-- Generated supporting document. -->

# EvAgent â€” Conceptual Architecture

<p align="center"><a href="https://evsphere.vercel.app/evagent"><img src="https://img.shields.io/badge/EvSphere-EvAgent-0b0c0d?style=for-the-badge&logo=github&logoColor=white" alt="EvAgent" /></a></p>

> **Scope note.** This describes what each subsystem is *for* and how responsibility is divided. It is not an implementation specification, and internal design detail is deliberately not published. Nothing here is sufficient to reconstruct the system.

---

## One-line model

An agent harness and CLI that plans, dispatches to specialists, composes skills at runtime, and keeps memory across runs.

---

## Subsystems

| Subsystem | Responsibility |
|---|---|
| **Architect / Planner** | Understands the goal, decomposes it into sub-tasks, builds an execution plan, tracks progress. |
| **Skill Router** | Matches each sub-task to the skills and agents suited to it, and ranks candidates. |
| **Parallel Dispatch** | Fans work out to specialists concurrently, manages dependencies and collects partial results. |
| **Skill Generation** | Composes reusable capabilities when a task exceeds what is already registered. |
| **Skill Registry** | Holds built-in, learned and generated skills; new entries feed the next iteration. |
| **Specialist Agents** | A row of parallel executors â€” landscape, orchestration, memory, tool integration, analysis, dynamic creation. |
| **Result Merger** | Merges outputs, checks consistency, resolves conflicts, packages artifacts. |
| **Memory Service** | Reads and writes long-term context throughout the run. |
| **Tools & Systems** | Local execution, sandboxing, and access to external services. |

---

## Design principles

1. **Explicit boundaries.** Each subsystem has one job. Overlap between them is a defect, not a convenience.
2. **Composition over configuration.** Capabilities are assembled at runtime rather than hard-wired at build time.
3. **Observability before optimisation.** A subsystem that cannot be inspected cannot be trusted or improved.
4. **Local first.** Execution and data stay under the operator's control wherever that is possible.
5. **Honest failure.** If something does not work, it says so rather than degrading silently.

---

## What is deliberately not here

- Source code, prompts, configuration or infrastructure
- Endpoint, credential, key or connection detail of any kind
- Dataset contents or identifiers
- Anything about a specific client or engagement
- Internal design rationale that would assist copying or attack

If you need any of the above, [ask directly](https://evsphere.vercel.app/start).

---

## Further reading

| | |
|---|---|
| [README](./README.md) | Overview |
| [docs/HOW-IT-WORKS.md](./docs/HOW-IT-WORKS.md) | Stage by stage |
| [docs/STATUS.md](./docs/STATUS.md) | Maturity and limits |
| [docs/FAQ.md](./docs/FAQ.md) | Questions and honest answers |

---

ðŸŒ [Website](https://evsphere.vercel.app) Â· [GitHub](https://github.com/evsphereofficial) Â· [npm](https://www.npmjs.com/~evsphere) Â· [LinkedIn](https://www.linkedin.com/company/evsphere) Â· [X](https://x.com/evsphereco)
