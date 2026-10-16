# Security

## Reporting a vulnerability

Please **do not** open a public issue. Use GitHub's private vulnerability reporting on the
affected repository — the **Security** tab → **Report a vulnerability** — and we will confirm
receipt and keep you updated.

## What is in scope here

- `plugin-sdk` and `plugin-manifest` (the code plugin authors compile against),
- the `plugin-template` release workflow,
- the registry's validation gates in `plugins` — for example a plugin archive that passes CI
  but does not match what the application installs, or an entry that could make a third-party
  plugin look first-party.

The desktop application itself is not open source. A vulnerability in the application should be
reported through the same private channel on `plugin-sdk`; we will route it.
