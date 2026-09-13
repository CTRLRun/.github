<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/CTRLRun/ctrlrun/main/docs/assets/wordmark-dark.svg">
    <img src="https://raw.githubusercontent.com/CTRLRun/ctrlrun/main/docs/assets/wordmark-light.svg" alt="CTRLRun" width="260">
  </picture>
</p>

<p align="center">
  <strong>CTRLRun stops AI agents from taking wrong, restricted, or malicious actions in your workflows.</strong><br>
  Every action is checked against your rules before it runs. Allowed actions go through.<br>
  Sensitive ones wait for a person. Forbidden ones are blocked.
</p>

---

The ticket says refund €500. The agent asks for €5,000, one extra zero. The tool is in its list,
the arguments are well formed, and the model is completely confident. Without CTRLRun, nothing
checks the amount and the call goes through: €4,500 too much. With CTRLRun, your rule checks the
amount and the call never leaves: €0 wrongly paid.

The other failure is the one people forget. An agent refunds €500, the call commits at the
provider, and the reply is lost on the way back, so the agent sees an error and retries. The bug
is not the retry. It is that the agent had no way to tell **this failed** from **I do not know
what happened**. CTRLRun keeps them apart: a lost reply is `AMBIGUOUS`, never `FAILED`, and a
retry against an `AMBIGUOUS` effect is refused until a human, or a reconcile hook, says what
happened.

```bash
pip install ctrlrun && ctrlrun demo
```

Five ways an agent action goes wrong and what stops each one, in under a second, with no network.

### What we build

**[ctrlrun](https://github.com/CTRLRun/ctrlrun)**: execution safety for AI agents. A Python
library that sits between the decision to act and the call that acts. A consequential action
happens at most once, exactly as approved, and leaves a receipt. Apache-2.0.

Runs on a single SQLite file, or on Postgres across hosts. The core installs `pyyaml` and `click`
and nothing else. An MCP gateway puts the same check in front of agents you can't modify: WhatsApp,
Slack and Teams bots, ChatGPT, Cursor, Codex. Framework adapters, OpenTelemetry and JWT identity
ship as optional extras.

### Start here

- **[ctrlrun.dev](https://ctrlrun.dev)**: docs, and [why](https://ctrlrun.dev/docs/why) in 700 words
- **[Try it in the browser](https://ctrlrun.dev/docs/try-it)**: no Python; break a protected action in a tab
- **[The execution boundary](https://ctrlrun.dev/execution-boundary)**: follow one action through every check
- **[Where it stops](https://github.com/CTRLRun/ctrlrun#what-it-does)**: the limits, written down
- **[Discussions](https://github.com/CTRLRun/ctrlrun/discussions)** · **[Security policy](https://github.com/CTRLRun/ctrlrun/security/policy)**

<p align="center">
  Let agents act. <strong>Keep the consequences yours to decide.</strong>
</p>
