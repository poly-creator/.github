# Contributing

Thanks for looking. A few things are worth knowing before you spend time on a change.

## Where things live

- **`plugin-sdk`, `plugin-manifest`** — generated repositories. They are exported from the
  source monorepo and their history starts at the current release. Everything in them is real
  and buildable (their CI proves it), but a commit made here would be overwritten by the next
  export.
- **`plugin-template`, `plugins`** — authored here. Ordinary pull requests are welcome.

## Issues

Always welcome, on any repository. A useful report carries the package version, what you
expected, what happened, and a minimal reproduction.

## Pull requests

- On `plugin-template` and `plugins`: send them as usual.
- On `plugin-sdk` and `plugin-manifest`: open an issue describing the change first. We will
  port your patch into the source monorepo, credit you in the commit, and it comes back out in
  the next export — slower than a direct merge, and the price of publishing generated trees
  without letting the published API and the application diverge.

## Releasing (maintainers)

`plugin-sdk` and `plugin-manifest` publish from their own repositories on `v*` tags,
authenticated with npm trusted publishing (OIDC) — **no npm token exists in either
repository**. The flow is: bump the version in the source monorepo → export the tree into a
checkout of the public repo → commit and push → tag `v<version>`. Both packages move together
on one version line.
