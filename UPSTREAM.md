# Upstream

This repository is the Mindaeon-owned fork of [higress-group/higress](https://github.com/higress-group/higress) (Apache-2.0).
The gateway of the platform (docs/05 C-02). Installed from the upstream chart at this version; Wasm plugins come from a registry of the deployment.

| | |
|---|---|
| Tracked line | `2.2` |
| Last merged tag | `v2.2.4` |
| Last merged commit | `58666ac985cee19a0a9a353421c63cead6d0cb47` (2026-08-13) |
| Recorded | 2026-10-03 |

## Branches

| Branch | Content |
|---|---|
| `upstream/2.2` | An exact mirror of the upstream tag above. Never committed to by hand |
| `mindaeon/2.2` | `upstream/2.2` plus the patches listed in [PATCHES.md](PATCHES.md). The branch that is built from |

Builds are tagged `<upstream version>-m.<n>`. Our changes live in new files, or in an upstream file between
`mindaeon_change start` and `mindaeon_change end` comments that give the reason.

## Taking a new upstream version

1. Fetch the upstream tag and fast-forward `upstream/2.2` to it.
2. Merge `upstream/2.2` into `mindaeon/2.2`; resolve patch by patch and drop a patch upstream now covers.
3. Run the licence check, the provenance gate, the security scan and the tests.
4. Update the table above and [PATCHES.md](PATCHES.md).
