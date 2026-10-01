<!-- markdownlint-disable -->

# Hardening Report: actions--github-script/v7.0.0

> This file was generated automatically by the hardening agent.

**Policy SHA:** `d636be7e43ef829af6e853da6b3c7566db9f72fe`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `2`

Action **actions--github-script/v7.0.0** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### unpinned-uses (severity: high)

The composite action references `actions/setup-node@v3`, which is a mutable tag reference rather than a pinned 40-character SHA commit hash. This means the action could silently change to a different (potentially malicious) version without any notice, creating a supply-chain risk.

Locations:

- `.github/actions/install-dependencies/action.yml:6`

## Iteration Notes

### Iteration 1

**Fixes applied:** unpinned-uses

**Notes:**

Replaced mutable tag reference `actions/setup-node@v3` with pinned SHA `actions/setup-node@3235b876344d2a9aa001b8d1453c930bba69e610 # v3` in `hardened/action/.github/actions/install-dependencies/action.yml` (line 6).

