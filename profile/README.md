<img src="https://raw.githubusercontent.com/poly-creator/.github/main/profile/band.svg" width="100%" height="12" alt="PolyCreator brand band">

# PolyCreator

[![website](https://img.shields.io/badge/website-polycreator.si-7b2cff)](https://polycreator.si)
[![npm](https://img.shields.io/npm/v/@polycreator/plugin-sdk?color=7b2cff)](https://www.npmjs.com/package/@polycreator/plugin-sdk)

An infinite-canvas studio for AI-generated images, video and storyboards. The
application is closed source; the plugin SDK is not.

## Links

| | |
|---|---|
| **Website** | https://polycreator.si |
| **Download** | https://polycreator.si/download |
| **Plugin marketplace** | https://polycreator.si/plugins |

## Repositories

| Repository | What it is |
|---|---|
| [`plugin-sdk`](https://github.com/poly-creator/plugin-sdk) | Types and the base class plugin authors build against. On npm as [`@polycreator/plugin-sdk`](https://www.npmjs.com/package/@polycreator/plugin-sdk). |
| [`plugin-manifest`](https://github.com/poly-creator/plugin-manifest) | The manifest and registry schemas the app, the marketplace and the registry validator all share. On npm as [`@polycreator/plugin-manifest`](https://www.npmjs.com/package/@polycreator/plugin-manifest). |
| [`plugin-template`](https://github.com/poly-creator/plugin-template) | Fork this to start a plugin: `npm run pack` produces the three release assets the registry expects. |
| [`plugins`](https://github.com/poly-creator/plugins) | The registry — one `plugins.json`, plus the CI that validates every PR against it. |

## Build a plugin

1. **Fork [the template](https://github.com/poly-creator/plugin-template)** and replace its `TEMPLATE-REPLACE` placeholders.
2. `npm install && npm run build && npm run pack` — the packer validates your manifest and hashes your entry files exactly the way the app's installer will.
3. Tag `v*`: the release workflow attaches `<id>-<version>.zip`, the byte-identical `<id>.zip` alias and `manifest.json`.
4. Open one PR against [the registry](https://github.com/poly-creator/plugins) adding one entry. CI checks the release assets, their byte-consistency and the in-zip integrity hash; a human then reviews the code.

The API guides live next to the SDK: [plugin settings](https://github.com/poly-creator/plugin-sdk/blob/main/docs/plugin-settings.md) and [plugin node UI](https://github.com/poly-creator/plugin-sdk/blob/main/docs/plugin-node-ui.md).

## Questions and show-and-tell

[Discussions](https://github.com/poly-creator/plugin-sdk/discussions) — for questions about the plugin API, what you built, and ideas that are not yet a concrete issue. Bugs and changes belong on the repositories; [CONTRIBUTING](https://github.com/poly-creator/.github/blob/main/CONTRIBUTING.md) says which ones take direct pull requests.

## Licence

MIT unless a repository says otherwise.
