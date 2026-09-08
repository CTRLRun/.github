# Contributing

This is the organisation-wide fallback. A repository that ships its own `CONTRIBUTING.md`
overrides it — [ctrlrun's](https://github.com/CTRLRun/ctrlrun/blob/main/CONTRIBUTING.md) is the
detailed one, and it is the model for the rest.

## The short version

- **Specification first.** A behaviour change is an amendment to the spec before it is code.
- **Tests first.** Write the failing test, then make it green. A red suite is the specification.
- **Every claim maps to a test.** If a document says the library does something, something
  proves it. Prose is not evidence.
- **Fail closed.** When a check cannot reach a confident answer, it refuses. No flag relaxes a
  check, and no setting makes a consequential action permissive by default.
- **Never map an unknown error to a definite failure.** If the code cannot observe that nothing
  happened, the outcome is unknown and is reported as unknown.

Small pull requests, one concern each. Discussion before a large change is welcome — open an
issue or start a [discussion](https://github.com/CTRLRun/ctrlrun/discussions).
