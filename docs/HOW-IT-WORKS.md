<!-- Generated supporting document. -->

# EvAgent â€” How It Works

[â† Back to README](./README.md)

---

- Architects a broad request into sub-tasks before executing anything
- Dispatches sub-tasks to purpose-built specialists rather than one generalist
- Fans independent work out in parallel and merges the results
- Generates and registers skills at runtime, feeding the next iteration
- Maintains persistent memory so runs build on previous runs
- Executes tools and sandboxed external systems locally, under your control

---

## Stage by stage

| # | Stage | What happens |
|---|---|---|
| **1. Request** | A task arrives. |
| **2. Understand** | The architect pass interprets the goal and decomposes it into sub-tasks. |
| **3. Route** | The skill router matches each sub-task to the capabilities suited to it. |
| **4. Dispatch** | Independent sub-tasks fan out to specialists in parallel. |
| **5. Extend** | If a needed capability is missing, a skill is generated and registered. |
| **6. Execute** | Specialists run their sub-tasks, using tools and reading memory as required. |
| **7. Merge** | Outputs are merged and checked for consistency; conflicts are resolved. |
| **8. Reflect** | The result is packaged, and feedback feeds skill generation for the next iteration. |

---

## Where the boundaries are

Each stage above hands something to the next one. Those hand-offs are the interesting part: they are where correctness is decided, and they are the first place to look when something misbehaves.

What is deliberately not documented: internal data structures, specific algorithms, thresholds, or the contents of any configuration. That is not an oversight â€” publishing them would make the system easier to copy or interfere with.

---

## Verifying behaviour yourself

The only honest way to judge EvAgent is to run it and observe. Claims in this repository are consistent with what the published artefacts show, but the artefacts are captures and schematics, not proofs.

- Maturity: **Available**
- Reference: [https://evsphere.vercel.app/evagent](https://evsphere.vercel.app/evagent)

---

ðŸŒ [Website](https://evsphere.vercel.app) Â· [GitHub](https://github.com/evsphereofficial) Â· [npm](https://www.npmjs.com/~evsphere) Â· [LinkedIn](https://www.linkedin.com/company/evsphere) Â· [X](https://x.com/evsphereco)
