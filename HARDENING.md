<!-- markdownlint-disable -->

# Hardening Report: actions--github-script/v8

> This file was generated automatically by the hardening agent.

**Policy SHA:** `d636be7e43ef829af6e853da6b3c7566db9f72fe`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `2`

Action **actions--github-script/v8** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### unpinned-uses (severity: high)

The composite action at .github/actions/install-dependencies/action.yml references `actions/setup-node@v4`, which is an unpinned mutable tag. If the tag is moved (e.g., by a supply-chain compromise), the action will silently execute different code. It should be pinned to a full 40-character commit SHA, e.g., `actions/setup-node@1d0ff469b12462b0c3dce7d4f4e4b5eef9f5b6e0 # v4`.

Locations:

- `.github/actions/install-dependencies/action.yml:6`

## Iteration Notes

### Iteration 1

**Fixes applied:** unpinned-uses

**Notes:**

Pinned `actions/setup-node@v4` to its full commit SHA `49933ea5288caeca8642d1e84afbd3f7d6820020` in `.github/actions/install-dependencies/action.yml`, preserving the `# v4` comment for readability.

