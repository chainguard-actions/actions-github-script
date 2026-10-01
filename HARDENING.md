<!-- markdownlint-disable -->

# Hardening Report: actions--github-script/v9.0.0

> This file was generated automatically by the hardening agent.

**Policy SHA:** `d636be7e43ef829af6e853da6b3c7566db9f72fe`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `2`

Action **actions--github-script/v9.0.0** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### unpinned-uses (severity: high)

The composite action at .github/actions/install-dependencies/action.yml uses `actions/setup-node@v4`, which is a mutable tag reference rather than a pinned full 40-character commit SHA. This means the action could be silently updated or compromised without the workflow noticing, enabling supply-chain attacks. It should be pinned to a specific commit SHA (e.g., `actions/setup-node@1d0ff469b4a3d2f5b32e7a95b2b6d5e6b5e6b5e6 # v4`).

Locations:

- `.github/actions/install-dependencies/action.yml:6`

## Iteration Notes

### Iteration 1

**Fixes applied:** unpinned-uses

**Notes:**

Pinned `actions/setup-node@v4` to its full commit SHA `49933ea5288caeca8642d1e84afbd3f7d6820020` in `.github/actions/install-dependencies/action.yml`, preserving `# v4` as a comment for readability.

