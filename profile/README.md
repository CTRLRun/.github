<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/CTRLRun/ctrlrun/main/docs/assets/wordmark-dark.svg">
    <img src="https://raw.githubusercontent.com/CTRLRun/ctrlrun/main/docs/assets/wordmark-light.svg" alt="CTRLRun" width="260">
  </picture>
</p>

<p align="center">
  <strong>The last check before an AI agent does something it can't undo.</strong><br>
  Autonomy belongs to the action, not the agent.
</p>

---

An agent refunds €500. The call commits at the provider. The reply is lost on the way back, so
the agent sees an error — and retries. The customer is refunded twice, and nothing in the stack
noticed.

The bug is not the retry. It is that the agent had no way to tell **this failed** from **I do not
know what happened**. Retry libraries, agent frameworks and tool loops collapse those two into one.

CTRLRun does not. A lost reply is `AMBIGUOUS`, never `FAILED`, and a retry against an `AMBIGUOUS`
effect is refused until a human — or a reconcile hook — says what happened.

```bash
pip install ctrlrun && ctrlrun demo
```

Five ways an agent action goes wrong and what stops each one, in under a second, with no network.

### What we build

**[ctrlrun](https://github.com/CTRLRun/ctrlrun)** — a Python library that sits between the
decision to act and the call that acts. A consequential action happens at most once, exactly as
approved, and leaves a receipt. Apache-2.0.

Runs on a single SQLite file, or on Postgres across hosts. The core installs `pyyaml` and `click`
and nothing else. Framework adapters, an MCP gateway, OpenTelemetry and JWT identity ship as
optional extras.

### Start here

- **[ctrlrun.dev](https://ctrlrun.dev)** — docs, and [why](https://ctrlrun.dev/docs/why) in 700 words
- **[Try it in the browser](https://ctrlrun.dev/docs/try-it)** — no Python; break a protected action in a tab
- **[What it guarantees, and what it can't](https://github.com/CTRLRun/ctrlrun#what-it-guarantees-and-what-it-cant)** — the limits, written down
- **[Discussions](https://github.com/CTRLRun/ctrlrun/discussions)** · **[Security policy](https://github.com/CTRLRun/ctrlrun/security/policy)**
