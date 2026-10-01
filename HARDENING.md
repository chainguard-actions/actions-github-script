<!-- markdownlint-disable -->

# Hardening Report: actions--github-script/v7.0.1

> This file was generated automatically by the hardening agent.

**Policy SHA:** `d636be7e43ef829af6e853da6b3c7566db9f72fe`

**Test Policy SHA:** `843adf9e4b8f85d0c08b27b9d0b09dd094b54702`

**Harden Agent Version:** `2`

Action **actions--github-script/v7.0.1** was hardened automatically. 1 finding(s) were identified and resolved across 1 iteration(s).

## Findings Fixed

### unpinned-uses (severity: high)

The composite action at `.github/actions/install-dependencies/action.yml` references `actions/setup-node@v3`, which uses a mutable version tag instead of a pinned 40-character commit SHA. This exposes the action to supply-chain attacks if the tag is moved to point to malicious code. It should be pinned to a full SHA, e.g. `actions/setup-node@1a4442cacd436585916779262731d1f68a3d7ad1 # v3`.

Locations:

- `.github/actions/install-dependencies/action.yml:6`

## Iteration Notes

### Iteration 1

**Fixes applied:** unpinned-uses

**Notes:**

Pinned `actions/setup-node@v3` to its full commit SHA `actions/setup-node@3235b876344d2a9aa001b8d1453c930bba69e610 # v3` in `.github/actions/install-dependencies/action.yml`. The SHA was resolved using lookup_action_sha.

